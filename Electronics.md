## Octopus Pro Guide

Guide [HERE](https://www.makenprint.uk/3d-printing/3d-printing-guides/3d-printer-mainboard-installation-guides/btt-octopus-guides/btt-octopus-pro-guide/)

## Octopus PinOut

[BTT Octopus Pro v1.0 F429](https://teamgloomy.github.io/btt_octopus_pro_1.0_f429_pins.html)

BTT Octopus Pro v1.0 F446/F429  
![BTT Octopus Pro Pins](https://github.com/gourmandos/VoronTrident300/blob/main/images/BIGTREETECH-Octopus-Pro-V1.0-Color-PIN.png?raw=true)

## Octopus Firmware Flashing

[Instructions](https://github.com/VoronDesign/Voron-Documentation/blob/main/build/software/octopus_klipper.md)

Use MicroSD method!

## Wiring

D2F Switch [Datasheet](/images/D2F_DS.pdf)

[Stepper motor](/images/4wireMotor.png)  
- don't forget to do continuity check to identify pairs
- pairs should have around 1.5 to 2.5 ohms
- if very loud, swap the 2 middle wires

You also can spin the motor by hand, and short pairs until it stalls. Then you know what’s what, and flip direction in software.

[Octopus Pro probe port](https://gadgetangel.org/build/electrical/OctopusPro_ProbePort)

[ 4-pin computer PWM fan on the BTT Octopus](https://www.nicksherlock.com/2022/01/driving-a-4-pin-computer-pwm-fan-on-the-btt-octopus-using-klipper/)

[Connecting a 4028 server fan](https://os.ratrig.com/docs/guides/4028/)

## Microswitch Z Endstop 

[GitHub Instructions / Design](https://github.com/VoronDesign/Voron-Hardware/tree/master/Microswitch_Z_Endstop) & [AliExpress PCB](https://www.aliexpress.com/item/1005005223120516.html)