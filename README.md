# Ortho 4x10 TKL

### Summary

An open-source custom mechanical keyboard featuring
* 4x10 ortholinear 'tenkeyless' style layout
* Raspberry Pi RP2040 integrated microcontroller
* USB-C
* Hotswap sockets
* Fully factory-assembled PCBA
* QMK and Vial firmware

### Goals

The goals of this project were:
1. Learn how to make a working PCBA mechanical keyboard
2. Keep hardware features to the minimum (no LEDs, OLED, encoders, etc.)
3. Fun and delighful > practical

### Photo

todo

### Layout

![](images/ortho4x10tkl.png)

### PCB

Version 0.1 - First PCBA ordered from JLCPCB, it works!

### Firmware

Vial firmware is compiled [here](vial/)

QMK firmware source will be added soon

### Case

todo

## What's Next

I'm quite satisfied with getting this working, and I had to order a minimum of 5 PCBs so I don't plan on making more for a while. But if you find this and use it as an example, here are some ideas of what could be added or improved:
* Cluster or consolidate the Reset and Boot pins. I was more concerned with finding a place they fit and were easy to route, but it's quite odd especially now that I know you have to either press them both simultaneously or hold Boot while plugging in the USB (which I put on opposite sides).
* Improve routing and reduce PCB "forehead". Although I kind of like the look.
* Support for more spacebar layouts like 2u
* Add more hardware features like LEDs, ESD, etc.
* Breakout pins to add hardware features or a daughterboard later
* Try a different MCU. The Raspberry Pi is totally fine, but there are other MCUs that have more packaged features like flash and crystal, so that would be less parts required and easier to route.

## Thanks to

For excellent custom keyboard and PCB tutorials: [Noah Kiser](https://www.youtube.com/@noahkiser), [Joe Scotto](https://www.youtube.com/@joe_scotto)

For layout inspiration: Zicodia ("LMAO"), tominabox1 and whydobearsxplod ("QAZ"), Jack Humbert ("Planck")

## Disclaimer

**Offered without warranty or liability! Use/modify/order at your own risk.**

This is my first PCB and for a first attempt it turned out pretty good, but it definitely isn't perfect or thoroughly tested yet.

No customer support, but simple questions/suggestions/improvements may be considered.

If you want to know _how_ or _why_ I did something (especially PCB related) tutorials online can explain it better than I can, so I suggest looking elsewhere.
