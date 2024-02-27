## Cooling

PWM Fan on GPIO guide [HERE](https://forums.raspberrypi.com/viewtopic.php?t=194621)

**ALTERNATIVELY**: Comment out

```
[temperature_sensor RPi]
sensor_type: temperature_host

[temperature_sensor MCU]
sensor_type: temperature_mcu
```

And add

```
[temperature_fan RPi_Fan] 
pin: POPULATE THE CORRECT PIN
max_power: 1.0
shutdown_speed: 1.0
kick_start_time: 0.2
off_below: 0.15
cycle_time: 0.010
sensor_type: temperature_host
control: watermark
min_temp: 0
max_temp: 70
target_temp: 40.0
min_speed: 0.5

[temperature_fan MCU_Fan] 
pin: POPULATE THE CORRECT PIN
max_power: 1.0
shutdown_speed: 1.0
kick_start_time: 0.2
off_below: 0.15
cycle_time: 0.010
sensor_type: temperature_mcu
control: watermark
min_temp: 0
max_temp: 70
target_temp: 35.0
min_speed: 0.5
```

Tmeperatures will remain displayed as standard and the fans are now temperature triggered

## Momentary switch ON/OFF

Connect a switch between PIN 5 (GPIO 3) and 6 (ground) for ON/OFF deep sleep function.  SSH in and type:

```
sudo nano /boot/config.txt
```

Add the following above the **ALL** section at the very end

```
dtoverlay=gpio-shutdown
```

If the Rpi turns ON but not OFF when pressing the push button, try this [solution](https://www.machinistblog.com/raspberry-pi-gpio-power-switch-not-working-solved/)
---

[GPIO 21 & various shutdown behaviours script](https://github.com/maz0r/rpi-shutdown)

[Cable, pinout & instructions](https://shop.inux3d.com/en/home/143-218-terrapi-power-button-.html#/11-color-black)

[LED status](https://embeddedcomputing.com/technology/open-source/development-kits/raspberry-pi-power-up-and-shutdown-with-a-physical-button)

## SSD instead of MicroSD

Guide [HERE](https://www.makeuseof.com/how-to-boot-raspberry-pi-ssd-permanent-storage/)

## Setup a RPi directory as a network shared folder to easily upload prints

Guide [HERE](https://pimylifeup.com/raspberry-pi-samba/)
