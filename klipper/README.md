<!-- omit in toc -->
# Klipper on Ender 3 V3 SE

<!-- omit in toc -->
## ToC

- [Why this page even exists?](#why-this-page-even-exists)
- [Why even bother?](#why-even-bother)
- [Should you continue?](#should-you-continue)
- [What do you need?](#what-do-you-need)
- [Installation and configuration](#installation-and-configuration)


### Why this page even exists?

Me being complete n00b with my first 3D printer ever on the table had to spent quite some time searching why klipper, what do, how do. This is short excerpt for other noobs to get klipping.

### Why even bother?

Well, I don't know, I just like customize stuff and I typically root and hack any device that can be rooted or hacked. Like my vacuum cleaner speaking GLaDOS voice.

With klipper one can expand printer capabilities and add functions like Telegram or Discord notifications. Read more on [Klipper site](https://klipper3d.org).

### Should you continue?

If you have some linux knowledge, know how to use terminal, how to resolve packages dependencies, love to customize things to your needs and you're not afraid of breaking stuff I guess that's a thing for you.

If not, stay stock or buy [Sonic Pad](../README.md#sonic-pad) to get rough idea about klipper. Or watch something on YouTube.

Note: Klipper is totally reversible to stock.

### What do you need?

There are 2 parts to klipper, one is firmware that you will install on the printer, other is the "controller" to that firmware that must run on a device connected to printer. That device can be Raspberry Pi (or other board running debian or clones), that could be a thin client like Fujitsu S920 or even a VM on your own PC with USB connected to virtual port on said VM. Choice is yours.

Raspberry Pi Zero 2W is cheap and will do (may be lacking firepower if you decide to run a FHD camera to watch the prints).

Additionally you need a USB-C cable to connect klipper controller to the printer, maybe a USB hub if you want camera.

Note that I am probably offending half of the internet using word klipper controller but that's what makes most sense imho.

### Installation and configuration

I won't be providing detailed information or step-by-step guide, these will be just bullet points to get thru.

1. Get a PC/RPi/whatever capable of running debian type system and prep it until you're SSH'ed into.
2. Get [KIAUH](https://github.com/dw-0/kiauh) and install klipper, moonraker, fluidd or mainsail.<br>
In short, you talk to fluidd, fluidd talks to moonraker and moonraker talks to klipper.
3. Get a klipper config from either of [repos](../README.md#configurations) and upload it to your controller.
4. In the terminal you'll need to compile klipper firmware.
```bash
cd ~/klipper/
make menuconfig
```
There select following settings:
```text
- Micro-controller architecture: STMicroelectronics STM32
- Processor model: STM32F103
- Bootloader offset: 28KiB
- Communication interface: Serial (onUSART1 PA10/PA09)
``````
Quit and save. Then run:
```bash
make
```

Once completed you will find klipper.bin file in out folder. Copy it to SD card, place it in the printer and turn the printer on.

5. Wait 5 minutes and restart klipper service via your web interface. If you succeeded error will be gone and you'll be successfully connected to printer.

Great job, you're now klipperized. Go Google the rest.

[Go back home](../README.md)