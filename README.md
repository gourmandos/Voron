# VoronTrident300
...
# 
...
## Things to print

Visit the folder [stl-3mf](/stl-3mf)
[Moroday Cutting Jigs](https://drive.google.com/drive/folders/1XE-0ez0jTqmz-vkzLz3cSLpAuZJ_NZnz)



## Mods

###

https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Empusas/BTT_Filament_Motion_Sensor_Mount
https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/falo/magnetic_grill_cover

### K3 Door
https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/Redoubt/BeunHaas34-Annex_Door

### Purge & Scrub
In combination:
- https://www.teamfdm.com/files/file/617-trident-decontaminator_mount_rightstl/
- Double Wiper Decontaminator (Trident 300mm) https://drive.google.com/drive/u/0/folders/1z-9KpVIce1BrdW45PiMQcnK1v2ausvbj

### Panel Clips
https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/All_Printers/annex_dev-Panel_2020_Clips_and_Hinges
OR 
https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/richardjm/snap-latch-2020

### Electronic bay
https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/slitte/ssd_bracket - TO BE MODIFED
https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/samwiseg0/lrs_screw_terminal_cover

### Skirts
https://www.youtube.com/watch?v=K6sHfXldK4k

### LEDs
https://github.com/VoronDesign/VoronUsers/blob/master/printer_mods/eddie/LED_Bar_Clip/LED_Bar_Clip_Misumi_version2.stl
https://github.com/Ramalama2/Voron-2-Mods/tree/main/Deprecated/Misumi_Led_Corners

### Doomy ETC
https://github.com/3DPrintingMods/VoronTrident-Sidepack


## Accessories

### Filter
https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Misc/Rebreather/Kirby-RebreatherXL
WITH: https://drive.google.com/drive/folders/1Z5R5iSrDxx-fSL647MQqjwC_a0YF4xba
ALTERNATIVES:
https://github.com/Annex-Engineering/Rebreather
https://github.com/nateb16/VoronUsers/tree/master/printer_mods/nateb16/THE_FILTER
https://github.com/yasuoki/ActivatedCarbonFilter7530

### Nozzle torque wrench
https://www.thingiverse.com/thing:4738816
https://www.thingiverse.com/thing:4332963

### GoopPenClip
https://github.com/MakerBogans/BoganParts/tree/main/killcode/GoopPenClip

## Electronics

### Octopus Pro Guide
https://www.makenprint.uk/3d-printing/3d-printing-guides/3d-printer-mainboard-installation-guides/btt-octopus-guides/btt-octopus-pro-guide/

### Octopus PinOut
![BTT Octopus Pro Pins](https://github.com/gourmandos/VoronTrident300/blob/main/images/btt_octopus_pro_1.0_pins.png?raw=true)
https://teamgloomy.github.io/btt_octopus_pro_1.0_f429_pins.html

### Octopus Firmware Flashing
https://github.com/VoronDesign/Voron-Documentation/blob/main/build/software/octopus_klipper.md


## Pi Stuff

### Rpi stop button
https://shop.inux3d.com/en/home/143-218-terrapi-power-button-.html#/11-color-black
https://embeddedcomputing.com/technology/open-source/development-kits/raspberry-pi-power-up-and-shutdown-with-a-physical-button

## Config Stuff

### Config MB
https://github.com/Susheii/VT.577_Config

### Klipper Estimator
https://github.com/Annex-Engineering/klipper_estimator

### Adaptive Bedmesh
https://github.com/Frix-x/klipper-voron-V2/blob/main/doc/features/adaptive_bed_mesh.md
https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging

### SS PLA Profile example
https://gist.githubusercontent.com/cmidgley/d6bb5e894def0794fa3e1f154e794aaa/raw/723e58910d8efdbd86f0f36f43d770f766422ba4/Voron%252024%2520SuperSlicer.ini

### Fast infill
https://github.com/RomRider/klipper-FastGyroidInfill

### Easy Sensorless homing
https://github.com/kyleisah/EZ-Sensorless-Homing

### PA per nozzle
; Set pressure advance per-filament for different nozzle sizes
{if nozzle_diameter[0]==0.4}SET_PRESSURE_ADVANCE ADVANCE=0.04  SMOOTH_TIME=0.02
{elsif nozzle_diameter[0]==0.5}SET_PRESSURE_ADVANCE ADVANCE=0.03 SMOOTH_TIME=0.02
{elsif nozzle_diameter[0]==0.6}SET_PRESSURE_ADVANCE ADVANCE=0.01  SMOOTH_TIME=0.02
{elsif nozzle_diameter[0]==0.8}SET_PRESSURE_ADVANCE ADVANCE=0.01 SMOOTH_TIME=0.02
{endif}

### Extrusion roles - Fast Infill
https://discord.com/channels/712144492563791922/712144816707731456/1080119195158708276

### Chamber Temperature & Exhaust Fan
https://github.com/eddietheengineer/VoronDocs/blob/master/setup/additional/chamber_temperature_exhaust_fan.md

## Yet to be understood
https://github.com/MakerBogans/dirtybird/tree/main/usermods/Sushei/Sushei's%20Version

