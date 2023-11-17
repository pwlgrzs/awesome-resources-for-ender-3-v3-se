# Your one-stop-shop for everything related to: 
# ***Ender 3 V3 SE!***

## Community
* [Creality /r](https://www.reddit.com/r/Creality/)
* [Ender 3 V3 SE /r (unofficial)](https://www.reddit.com/r/Ender3V3SE/)
* [Discord](https://discord.gg/mbCpbSv9)

## Hardware and parts

### Mods

#### Not-printable

All items below were either purchased by someone in the community or purchased by myself. No wilding.

* [PEI bed](https://www.aliexpress.com/item/1005005815144081.html)
* [Heat bed spacer spring replacement](https://www.aliexpress.com/item/33000090210.html)
* [Sonic Pad](https://www.aliexpress.com/item/1005005573923853.html)
* [Sonic Pad G-Sensor and Serial Cable*](https://www.aliexpress.com/item/1005005135181819.html)

\* Serial cable is currently required to connect SonicPad to V3 SE, USB-C connection does not work.

#### Printable

* [Ender 3 V3 SE 4010 Fan Shroud ](https://www.printables.com/model/595397-ender-3-v3-se-4010-fan-shroud) by iambengraham

#### Other 3D printing useful stuff

WIP

## Slicers

### Slicer profiles

* [Prusa profile](https://github.com/suchmememanyskill/PrusaSlicer-Ender3-v3-SE-Config) by [suchmememanyskills](https://github.com/suchmememanyskill)

## Klipper

* [Official site](https://www.klipper3d.org)
* [Discord](https://discord.klipper3d.org/})

### Firmware

* [Klipper fork with working automatic z-offset](https://github.com/0xD34D/klipper_ender3_v3_se) by [0xD34D](https://github.com/0xD34D)*

\* See installation instructions below, use at own risk
### Configurations

* [Klipper configuration](https://github.com/0xD34D/ender3-v3-se-klipper-config) by [0xD34D](https://github.com/0xD34D)
* [Klipper configuration](https://github.com/bootuz-dinamon/ender3-v3-se-full-klipper) by [bootuz-dinamon](https://github.com/bootuz-dinamon)

### SonicPad

WIP

## Other stuff

#### Install instructions for 0xD34D Klipper fork

1. Run KIAUH and uninstall klipper (ONLY klipper)
2. In KIAUH folder create file named klipper_repos.txt and add these 2 lines:

```
https://github.com/Klipper3d/klipper
https://github.com/0xD34D/klipper_ender3_v3_se
```
3. Then in KIAUH settings change klipper repo to 0xD34D's
4. Install klipper in KIAUH as usual
5. Once installed build firmware as usual from the klipper folder
6. Flash the firmware to printer
7. Create prtouch.cfg with contents from [0xD34D](https://github.com/0xD34D/ender3-v3-se-klipper-config/blob/main/prtouch.cfg)
8. In existing printer.cfg add line [include prtouch.cfg]
9. Restart klipper service
10. PRTOUCH_PROBE_ZOFFSET should now work and return Z-offset in the end of printer.cfg