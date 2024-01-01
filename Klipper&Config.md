## Back up printer configuration files to GitHub

Guide [HERE](https://docs.vorondesign.com/community/howto/EricZimmerman/BackupConfigToGithub.html) & alternate guide [HERE](https://lazarofilm.gitbook.io/3d-printing/creating-a-github-backup-for-klipper)

## Autocommit config changes to github

Guide [here](https://github.com/th33xitus/kiauh/wiki/How-to-autocommit-config-changes-to-github%3F)

## Sonar - network pinger

Keep the WiFi connection alive by pinging at interval, instructions [HERE](https://github.com/mainsail-crew/sonar)

## Auto Z Calibration

Repo [HERE](https://github.com/protoloft/klipper_z_calibration)

## A better print_start macro

Repo [HERE](https://github.com/PrintStructor/A-better-print_start-macro)

## Setup a BTT Smart Filament Sensor

Set the sensitivity to 10 minimum

[Setup a BTT Smart Filament Sensor](zhttps://docs.vorondesign.com/community/howto/samwiseg0/btt_smart_filament_sensor.html#setup-a-btt-smart-filament-sensor)

## Automated probe accuracy testing

Instructions [HERE](https://github.com/sporkus/probe_accuracy_tests)

## LED

[Rainbow barf logo for SB](https://github.com/tanaes/whopping_Voron_mods/tree/main/LEDs/Rainbow_Barf_Logo_LED)

[LED Effects for Klipper](https://github.com/julianschill/klipper-led_effect)

## Klipper Estimator

Repo [HERE](https://github.com/Annex-Engineering/klipper_estimator)

## Adaptive Bedmesh

[KAMP](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging)

[Klippain](https://github.com/Frix-x/klipper-voron-V2/blob/main/doc/features/adaptive_bed_mesh.md)

## Driver Tuning

[Klipper TMC Autotune](https://github.com/andrewmcgr/klipper_tmc_autotune)  
`WARNING` if sensorless homing, `sg4_thrs` and/or `sgt` values need to be readjusted

[DrGhetto's guide for Klipper](https://github.com/MakerBogans/docs/wiki/TMC-Driver-Tuning)

## Useful sets of macros

[Ellis](https://ellis3dp.com/Print-Tuning-Guide/articles/index_useful_macros.html)

[The-Conglomerate](https://github.com/The-Conglomerate/Voron-Klipper-Common/)

[jschuh](https://github.com/jschuh/klipper-macros/tree/main)

## SS PLA Profile

[Example](https://gist.githubusercontent.com/cmidgley/d6bb5e894def0794fa3e1f154e794aaa/raw/723e58910d8efdbd86f0f36f43d770f766422ba4/Voron%252024%2520SuperSlicer.ini)

## PA per nozzle

```
; Set pressure advance per-filament for different nozzle sizes
{if nozzle_diameter[0]==0.4}SET_PRESSURE_ADVANCE ADVANCE=0.04  SMOOTH_TIME=0.02
{elsif nozzle_diameter[0]==0.5}SET_PRESSURE_ADVANCE ADVANCE=0.03 SMOOTH_TIME=0.02
{elsif nozzle_diameter[0]==0.6}SET_PRESSURE_ADVANCE ADVANCE=0.01  SMOOTH_TIME=0.02
{elsif nozzle_diameter[0]==0.8}SET_PRESSURE_ADVANCE ADVANCE=0.01 SMOOTH_TIME=0.02
{endif}
```

## Extrusion roles - Fast Infill

Discord Message [HERE](https://discord.com/channels/712144492563791922/712144816707731456/1080119195158708276)

## KlipperScreen

Change KlipperScreen background [Instructions](https://www.teamfdm.com/files/file/690-klipper-screen-blue-hexes/)

RPi BUSTER [Instructions](/other/Pi%20Buster%20KlipperScreen%20Instructions)

No TouchScreen FIX [Instructions](/other/No%20touchscreen%20fix)

## TailScale

For Mainsail: MUST add the IP of the device intending to connect with in Moonraker.conf

[Source](https://www.teamfdm.com/forums/topic/1594-tailscale-vpn-and-mobile-raker/)

[Example](https://github.com/ihrapsa/KlipperWrt/issues/21)

## Syncing slicer profiles

**SUPERSLICER**

[Youtube tutorial](https://www.youtube.com/watch?v=n_8kIZWBjhY&t=195s)

add the `--datadir c:/my/local/dir` parameter to **SS.exe** shortcut

**PRUSASLICER**

Tutorial [HERE](https://adambyram.com/2023/01/29/syncing-prusaslicer-configuration/)