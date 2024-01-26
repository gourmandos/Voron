Credits to Deutherius V2.818 (VORONDesing Discord)

[Source](https://discord.com/channels/460117602945990666/1021908552702505051/1129498299272011866)


Main idea is to tell klipper that those bed fans are actually a chamber heater.  
Spicy fans usually work with a constant fan and switching heater. This is similar, but in reverse - bed heater makes sure that the bed itself stays at a constant temperature and fans get PWMed to draw varying amount of heat from the bed heater.

```
[heater_generic heater_chamber]
heater_pin: z:P2.5
sensor_type: ATC Semitec 104NT-4-R025H42G
sensor_pin: P0.25
control: pid
pid_Kp: 61.470837
pid_Ki: 0.5
pid_Kd: 0
pwm_cycle_time: 0.3
min_temp: -273.15
max_temp: 75

[verify_heater heater_chamber]
max_error: 120
check_gain_time: 120
hysteresis: 50
heating_gain: 1

[gcode_macro SET_CHAMBER]
gcode:
  {% set chamber_target = params.CHAMBER_TEMP|default(0)|float %}
  SET_HEATER_TEMPERATURE heater=heater_chamber target={chamber_target}
  ```

**heater_pin** is what the bed fans plug into  
**sensor_pin** is a thermistor somewhere in the chamber, preferably shielded from things that can influence local chamber temp (part cooling fan being the most obvious)  
**verify_heater** section is there so that klipper doesn't die when chamber temp gets set while the bed is cold or heating up (heater not heating at expected rate error). Do not play with this code block for any other heater, it's a real fire hazard. Here it's safe because nothing can really thermally run away (bed heater is controlled separately by a different PID loop). Worst that can happen is that the bed fans can overpower the bed heater and cause a thermal runaway shutdown - you can set a lower max "heater" (fan) power for your specific system to combat that issue.

You can try automatic PID tuning for the system, but I wouldn't bother - it took me something close to 4 hours and the values didn't work really well - the super high D value (>4700) caused the bed fans PWM to be extra jumpy, going +-30% PWM multiple times a second. Values I ended up with should be relatively robust and the PWM changes are steady.

This is the relevant part of my print_start:

```
    {% set CHAMBER_TEMP = params.CHAMBER_TEMP|default(0)|float %}

        ...

        STATUS_HEATING

        M140 S{BED_TEMP|int} ;start heating up bed

        {% if FILAMENT_TYPE == "ABS" or FILAMENT_TYPE == "ASA" or FILAMENT_TYPE == "PC" %}
            SET_FAN_SPEED FAN=Nevermore_micro SPEED=0.6
            SET_FAN_SPEED FAN=Exhaust SPEED=0.25   
        {% endif %}

        M104 S150 #start heating up nozzle

        {% if CHAMBER_TEMP > 0 and not printer["heater_generic heater_chamber"].temperature >= CHAMBER_TEMP|float%} #wait for chamber temps
            SET_CHAMBER CHAMBER_TEMP={CHAMBER_TEMP+1} #+1 °C for faster temp target arrival
            CENTER
            M106 S204 #part cooling fan 80%
            TEMPERATURE_WAIT SENSOR="heater_generic heater_chamber" MINIMUM={CHAMBER_TEMP-0.1} #wait until chamber temp is very nearly reached
            SET_CHAMBER CHAMBER_TEMP={CHAMBER_TEMP} #set correct chamber target and let PID do its magic
            STATUS_CLEANING
            CLEAN_NOZZLE
        {% endif %}

        #in case chamber was already heated
        {% if CHAMBER_TEMP > 0 %}
            SET_CHAMBER CHAMBER_TEMP={CHAMBER_TEMP} 
        {% endif %}
        
        M107 #part cooling fan off
        #make sure hotend and bed are up to temp in all cases
        M109 S150
        M190 S{BED_TEMP|int}
```

and of course pass the chamber temp parameter from slicer, e.g. in superslicer

```print_start EXTRUDER_TEMP=[first_layer_temperature] BED_TEMP=[first_layer_bed_temperature] CHAMBER_TEMP=[chamber_temperature] FILAMENT_TYPE={filament_type[0]}```

EDIT: If you are using the mini12864 display with lcd_tweaks.cfg for a chamber temperature icon on the display, you can modify the cfg file to get the chamber temp readout back by swapping this line  
```{% set chamber = printer['temperature_sensor chamber'] %}```  
for  
```{% set chamber = printer['heater_generic heater_chamber'] %}```