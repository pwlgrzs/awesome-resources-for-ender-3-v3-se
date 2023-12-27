<!-- omit in toc -->
# [DISCONTINUED!]

This page is now discontinued and [moved here](https://pblvsky.gitbook.io/ender3v3se/).
[GitHub repo for PR/Issues.](https://github.com/pwlgrzs/ender3-v3-se-gitbook)

<!-- omit in toc -->
## ToC

- [Community](#community)
- [Hardware, parts, mods](#hardware-parts-mods)
  - [Mods](#mods)
    - [Not-printable](#not-printable)
    - [Printable](#printable)
- [Slicers](#slicers)
  - [Slicer profiles](#slicer-profiles)
- [Remote controlling your printer](#remote-controlling-your-printer)
  - [Camera](#camera)
  - [Sonic Pad](#sonic-pad)
- [Other 3D printing useful info](#other-3d-printing-useful-info)
  - [Models sites](#models-sites)
  - [3D printing guides](#3d-printing-guides)
- [Other stuff](#other-stuff)
- [Contribution](#contribution)
- [Credits](#credits)

## Community

- [Creality /r](https://www.reddit.com/r/Creality/)
- [Ender 3 V3 SE /r (unofficial)](https://www.reddit.com/r/Ender3V3SE/)
- [Discord (unofficial)](https://discord.gg/gYyN3zJEW6)
- [Facebook group (unofficial)](https://www.facebook.com/groups/347538964267031)

## Hardware, parts, mods

### Mods

#### Not-printable

All items below were either purchased by someone in the community or purchased by myself. No wilding.

- [PEI bed](https://www.aliexpress.com/item/1005005815144081.html)
- [Heat bed spacer spring replacement](https://www.aliexpress.com/item/33000090210.html)
- Bed spring upgrade
- [Sonic Pad](https://www.aliexpress.com/item/1005005573923853.html)
- [Sonic Pad G-Sensor and Serial Cable*](https://www.aliexpress.com/item/1005005135181819.html)

\* Serial cable is currently required to connect SonicPad to V3 SE, USB-C connection does not work. Please refer to Sonic Pad section for more information.

#### Printable

I figured it will take a lot of scrolling to list all possible mods for Ender 3 V3 SE so this section will only contain a link to mods in the Printables collection.

[Have a look and print!](https://www.printables.com/@pblvsk_1037476/collections/998458)

If you want to contribute please open and issue with links to models you'd like to add.

## Slicers

### Slicer profiles

- [Prusa profile](https://github.com/suchmememanyskill/PrusaSlicer-Ender3-v3-SE-Config) - both stock and klipper
- Cura - Profile is already in the code and will be released with next Cura version (5.6.0 currently in beta).
- Orca - Yet to find working Orca profile...

## Remote controlling your printer

Here you have 2 options: Klipper or OctoPrint.

Read more in [How to remote control Ender 3 V3 SE](/remote-control/README.md).

### Camera

Go for Logitech C270 (1280x720) or Logitech C920 (FHD).
These 2 have greatest number of available printed mods, I think C270 even more that G920. IMO C270 is more than enough for job monitoring.

### Sonic Pad

Sonic Pad is Creality T800 AllWinner tablet with preinstalled and customized Klipper. The OS is pretty much closed (even if rooted) and does not allow for any modifications outside what can be seen in the webUI (no KAMP, no Telegram bot, nothing).

The only plus I currently see in owning one is that it has device specific configurations that community is currently struggling to replicate (such as pytouch_v2 implementation - note there is a pytouch_v1 working version of klipper).

Does it work? Yes. Do you need it? That depends. You can refer to the table below.

| + + +                                   | - - -                                               |
|---------------------------------------- |---------------------------------------------------- |
| Creality customized profiles            | Closed OS                                           |
| No in-depth klipper knowledge required  | No Klipper addons/plugins                           |
| Simple to use from touch screen         | Device is slow                                      |
| Easy calibration from the UI            | Touch screens seems laggy                           |
| Adds WiFi capability to the printer     | Requires separate serial cable to connect to V3 SE  |
| Built-in G-Sensor calibration           | Slicer profiles may not have compatibile commands   |

You can buy one here: [Aliexpress](https://www.aliexpress.com/item/1005005573923853.html).
My purchase from the link above came with serial cable and G-Sensor however it was noted that not all boxes had these cables included. Links to these cables is listed above.

## Other 3D printing useful info

### Models sites

- [printables.com](https://www.printables.com/) - model site by Prusa
- [thingverse.com](https://www.thingiverse.com/)
- [makerworld.com/en](https://makerworld.com/en) - model site by Bambu Labs
- [yeggi.com](https://www.yeggi.com/) - this is an aggregator from various sites
- [thangs.com](https://thangs.com/) - same as above

### 3D printing guides

- [all3dp.com](https://all3dp.com/)
- [teachingtechyt](https://teachingtechyt.github.io) - guides on how to calibrate printer
- [ellis3dp.com](https://ellis3dp.com)

## Other stuff

## Contribution

Want to add your resources? Sure thing, open an issue or send a PR.

## Credits

Thanks to

- [suchmememanyskill](https://github.com/suchmememanyskill)
- [0xD34D](https://github.com/0xD34D)
- [bootuz-dinamon](https://github.com/bootuz-dinamon)
- everyone not mentioned here

for their awesome contribution to Ender 3 V3 SE community!
