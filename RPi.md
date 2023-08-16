# Physical mods

## PWM Fan on GPIO



## Momentary switch ON/OFF

Connect a switch between PIN 5 (GPIO 3) and 6 (ground) for ON/OFF deep sleep function.  SSH in and type:

```
sudo nano /boot/config.txt
```

Add the following above the **ALL** section

```
dtoverlay=gpio-shutdown
```

---

[Cable, pinout & instructions](https://shop.inux3d.com/en/home/143-218-terrapi-power-button-.html#/11-color-black)

[LED status](https://embeddedcomputing.com/technology/open-source/development-kits/raspberry-pi-power-up-and-shutdown-with-a-physical-button)

## SSD instead of MicroSD



## Setup a RPi directory as a network shared folder to easily upload prints

Guide [HERE](https://pimylifeup.com/raspberry-pi-samba/)
