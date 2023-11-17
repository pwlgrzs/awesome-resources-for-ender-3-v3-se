# Your one-stop-shop for everything related to:<br>***Ender 3 V3 SE!***

## Community
* [Creality /r](https://www.reddit.com/r/Creality/)
* [Ender 3 V3 SE /r (unofficial)](https://www.reddit.com/r/Ender3V3SE/)
* [Discord](https://discord.gg/mbCpbSv9)
* [Facebook group](https://www.facebook.com/groups/347538964267031)

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

![Alt text](/assets/img/example-printed-shroud.jpg "Shroud")

## Slicers

### Slicer profiles

* [Prusa profile](https://github.com/suchmememanyskill/PrusaSlicer-Ender3-v3-SE-Config) by [suchmememanyskill](https://github.com/suchmememanyskill)

Cura profile is already in the code and will be released with next Cura version (5.6.0 currently in beta).

## Klipper

* [Official site](https://www.klipper3d.org)
* [Discord](https://discord.klipper3d.org/})

### Firmware

* [Klipper fork with working automatic z-offset](https://github.com/0xD34D/klipper_ender3_v3_se) by [0xD34D](https://github.com/0xD34D)*

\* See installation instructions [below](https://github.com/pwlgrzs/awesome-resources-for-ender-3-v3-se#other-stuff), use at own risk.
### Configurations

* [Klipper configuration](https://github.com/0xD34D/ender3-v3-se-klipper-config) by [0xD34D](https://github.com/0xD34D)
* [Klipper configuration](https://github.com/bootuz-dinamon/ender3-v3-se-full-klipper) by [bootuz-dinamon](https://github.com/bootuz-dinamon)

I recommend using 0xD34D configuration if you use his klipper fork.

### Klipper extras

* [CYD-Klipper](https://github.com/suchmememanyskill/CYD-Klipper)
* [KAMP](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging)
* [Telegram bot](https://github.com/nlef/moonraker-telegram-bot)

### SonicPad

Sonic Pad is Creality T800 AllWinner tablet with preinstalled and customized Klipper. The OS is pretty much closed (even if rooted) and does not allow for any modifications outside what can be seen in the webUI (no KAMP, no Telegram bot, nothing).

The only plus I currently see in owning one is that it has device specific configurations that community is currently struggling to replicate (such as pytouch_v2 implementation - note there is a pytouch_v1 working version of klipper).

Does it work? Yes. Do you need it? That depends. You can refer to the table below.

| + + +                                  	| - - -                                              	|
|----------------------------------------	|----------------------------------------------------	|
| Creality customized profiles           	| Closed OS                                          	|
| No in-depth klipper knowledge required 	| No Klipper addons/plugins                          	|
| Simple to use from touch screen        	| Device is slow                                     	|
| Easy calibration from the UI           	| Touch screens seems laggy                          	|
| Adds WiFi capability to the printer    	| Requires separate serial cable to connect to V3 SE 	|

You can buy one here: [Aliexpress](https://www.aliexpress.com/item/1005005573923853.html).
My purchase from the link above came with serial cable and G-Sensor however it was noted that not all boxes had these cables included. Links to these cables is listed above.

## Other 3D printing useful info

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