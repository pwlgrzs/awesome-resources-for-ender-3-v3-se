<!-- omit in toc -->
# Klipper

- [Official site](https://www.klipper3d.org)
- [Discord](https://discord.klipper3d.org)

<!-- omit in toc -->
## ToC

- [Klipper on Ender 3 V3 SE](#klipper-on-ender-3-v3-se)
- [Installation and configuration](#installation-and-configuration)
- [Firmware](#firmware)
- [Configurations](#configurations)
- [Klipper extras](#klipper-extras)
- [Install instructions for 0xD34D Klipper fork](#install-instructions-for-0xd34d-klipper-fork)

### Klipper on Ender 3 V3 SE

While it is possible to flash klipper onto Ender 3 V3 SE board following features are not (yet) working or there are testing releases availabe from other code creators.

- automatic Z-offset probing
- screen (it is in the screensaver mode after flashing)

Opposed to Sonic Pad klipper "standard" installation on RPi board or else use USB-C connection.

### Installation and configuration

I won't be providing detailed information or step-by-step guide, these will be just bullet points to get thru.

If you don't like reading check this [awesome video](https://www.youtube.com/watch?v=LrBiwabN-Y8) by BootUse

1. Get a PC/RPi/whatever capable of running debian type system and prep it until you're SSH'ed into.
2. Get [KIAUH](https://github.com/dw-0/kiauh) and install klipper, moonraker, fluidd or mainsail.<br>
In short, you talk to fluidd, fluidd talks to moonraker and moonraker talks to klipper.
1. Get a klipper config from either of configuration repos and upload it to your controller.
2. In the terminal you'll need to compile klipper firmware.

```bash
cd ~/klipper/
make menuconfig
```
There select following settings:
```text
- Micro-controller architecture: STMicroelectronics STM32
- Processor model: STM32F103
- Bootloader offset: 28KiB
- Communication interface: Serial (on USART1 PA10/PA09)
``````

Quit and save. Then run:

```bash
make
```

Once completed you will find klipper.bin file in out folder. Copy it to SD card, place it in the printer and turn the printer on.

5. Wait 5 minutes and restart klipper service via your web interface. If you succeeded error will be gone and you'll be successfully connected to printer.

<<< **REMOVE THE SDCARD**  >>>

### Firmware

- [Development klipper fork with working automatic z-offset](https://github.com/0xD34D/klipper_ender3_v3_se)

\* See installation instructions [below](#install-instructions-for-0xd34d-klipper-fork), use at own risk.

### Configurations

- [xD34D](https://github.com/0xD34D/ender3-v3-se-klipper-config)
- [bootuz-dinamon](https://github.com/bootuz-dinamon/ender3-v3-se-full-klipper)

I recommend using 0xD34D configuration if you use his klipper fork.

### Klipper extras

- [CYD-Klipper](https://github.com/suchmememanyskill/CYD-Klipper)*
- [KAMP](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging)
- [Telegram bot](https://github.com/nlef/moonraker-telegram-bot)

\* Requires hardware purchase

### Install instructions for 0xD34D Klipper fork

I assume if you got here you may know what you're doing but I have to say that again, you're on your own and not me nor the 0xD34D would be responsible for your printer becoming a toast.

1. Run KIAUH and uninstall klipper (ONLY klipper)
2. In KIAUH folder create file named klipper_repos.txt and add these 2 lines:

```text
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

[Go back home](../README.md)
