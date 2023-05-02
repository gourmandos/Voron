# Resources

## Guides

[Learn GIT](https://learngitbranching.js.org/)

[Formatting on github](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

[Getting started](https://www.markdownguide.org/getting-started/)

---

## Bed adhesive / release agent

[General Goop recipe](https://github.com/MakerBogans/docs/wiki/Printer-goop)

50% water, 50% ipa/metho, 1% pvp/pa by weight

---

## TMC driver tuning

[DrGhetto's guide for Klipper](https://github.com/MakerBogans/docs/wiki/TMC-Driver-Tuning)

Quick formula for stepper motor maximum voltage:

```
run_current = motor_peak_current * 0.707 * 0.80
```

## Setup 

### Rotation_distance on extruders

>initial_mark_distance = initial mark on filament from the intake of the extruder body
subsequent_mark_distance = distance of mark on filament after extruding 100mm
actual_extrude_distance = <initial_mark_distance> - <subsequent_mark_distance>
actual_extrude_distance = 120mm - 20mm

```
rotation_distance = <previous_rotation_distance> * <actual_extrude_distance> / <requested_extrude_distance>

rotation_distance = 200 * 20mm / 100mm
```
---

[Chamber Temperature & Exhaust Fan](https://github.com/eddietheengineer/VoronDocs/blob/master/setup/additional/chamber_temperature_exhaust_fan.md)

[Filament Runout Sensor](https://github.com/eddietheengineer/VoronDocs/blob/master/setup/additional/filament_runout_sensor.md)

[Fast infill](https://github.com/RomRider/klipper-FastGyroidInfill)

---

## Calibration 

[Advance resonance tuning](https://github.com/SnakeOilXY/SnakeOil-XY/blob/master/Doc/Manual/advance-resonance-tuning.md)

[Flow Calculator macros](https://github.com/agentk/klipper_macros/tree/main/FlowCalculator)

[Extrusion system Benchmark](https://github.com/CNCKitchen/ExtrusionSystemBenchmark)

---




### Easy Sensorless homing
https://github.com/kyleisah/EZ-Sensorless-Homing
https://www.klipper3d.org/TMC_Drivers.html#configure-printercfg-for-sensorless-homing
https://docs.vorondesign.com/community/howto/clee/sensorless_xy_homing.html