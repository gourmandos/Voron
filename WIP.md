# WIP

Just my own tracking, no public relevance.

## Physical mods

---

- ~~Inverted electronics~~
- ~~Rama idlers~~
- Carbon fibre X extrusion
- Sleeves & cable management
---

- ~~DB / Sherpa SLS~~
- ~~RKE~~

>Note the rk-rearmount with the little 'hook' that holds the Z chain away from the ribbon, only for v2.4  
If ribbon is drooping, use 2x rk-frontmount swivels on X rail, instead of 1 + fence.  
See [discord pictures](https://discord.com/channels/712144492563791922/888001568568393820/1070332922583859272)  
Alternatively, use [bearing swivels](https://github.com/MakerBogans/roadkill/tree/main/usermods/Usernametaken/Bearing-Shaft) with 2 x f623 bearings, a .5mm shim, m3 nut and an m3 BHCS (length to be adjusted as required).
- ~~Eureka~~

---

- ~~Y support~~
- ~~K3 Door~~
- ~~Panel clips~~

---

- Purge bucket / scrubber
- ~~Chamber thermistor~~
- Air circulation
- Air filtration
- Driver cooling

---

- ~~LED~~
- ~~LED diffusers~~
- ~~Internal spool~~

## Electronics

- ~~Pi Klipperscreen~~
- ~~Config autobackup~~
- Nevermore if ABS...
- Heatsoak macro
- Skirt buttons (light 30% to 100%, up/down babystep, momentary ON/OFF, pause)

## Klipper

- Go over ALL the .cfg  
Use official references such as [Sherpa_Micro](https://github.com/Annex-Engineering/ANNEX-Printer-Firmware/blob/main/Klipper_and_Klipper_Derivatives/Sherpa_Micro/Klipper_Config_Block.txt) when possible

- Virtual Z Endstop:
(When using the probe as the Z endstop)

    Enter ``Z_OFFSET_APPLY_PROBE*``
    This will apply your new offset to your probe’s z_offset.  
    Enter ``SAVE_CONFIG``.


## Potential

- Insulation
- AWD
- Squash ball feet
- 4040 frame
- Belted Z
- [Filametrix](https://github.com/sorted01/Filametrix) with TradRack

## To be sorted

[MEASURE_AXES_NOISE numpy error](https://www.reddit.com/r/klippers/comments/t7dfz0/measure_axes_noise_numpy_error/)

[Sync PS profiles with GitHub](https://forum.prusa3d.com/forum/prusaslicer/prusa-slicer-cloud-settings-sync-settings-between-pcs/)