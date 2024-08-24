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

Spacebar cluster supports 3x1U and 1x3U layouts. Stabilizers are not currently supported on the v0.1 PCB or Plate, but can be substituted with loose switches (like Cherry) to the side, or raw dog it without stabilizers and use a well-supported box-style switch in the center.

Arrow cluster supports 4 or 6 keys, although most of the top cases in this repo will cover up 2 of them. Still, the switches are there if you prefer to have them.

### Keymap

This is my keymap, note that with VIAL firmware some setup will be manual in the VIAL application

```
Default Layer:
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┐┌───────┬───────┬───────┐
│   Q (TAB) W   │   E   │   R   │   T   │   Y   │   U   ││   I   │   O (DEL) P   │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┘├───────┼───────┼───────┤
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┐│   K   │   L (ENT) ;   │
│   A (ESC) S   │   D   │   F   │   G   │   H   │   J   │└───────┴───────┴───────┘
├───────┼───────┼───────┼───────┼───────┼───────┼───────┤┌       ┌───────┐       ┐
│  Z(⇧) │   X   │   C   │   V   │   B   │   N   │  M(⇧) │  PG DN │   Up  │ PG UP
├───────┼───────┼───────┼───────┼───────┼───────┼───────┤┌───────┼───────┼───────┐
│   ⌥   │   ⌘   │         Space         │   ,   │   .   ││  Left │  Down │ Right │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┘└───────┴───────┴───────┘

Raise Layer:
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┐┌───────┬───────┬───────┐
│   1  (`)  2   │   3   │   4   │   -   │   +   │       ││   [   │   ]   |   '   │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┘├───────┼───────┼───────┤
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┐│   (   │   )   |       │
│   4   |   5   │   6   │   0   │   /   │   *   │   =   │└───────┴───────┴───────┘
├───────┼───────┼───────┼───────┼───────┼───────┼───────┤┌       ┌───────┐       ┐
│  7(⇧) │   8   │   9   │   .   │   |   │   &   │   ?   │        │   ⇧   │       
├───────┼───────┼───────┼───────┼───────┼───────┼───────┤┌───────┼───────┼───────┐
│   ⌥   │  0(⌘) │                       │       │       ││   <   │   ⌃   │   >   │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┘└───────┴───────┴───────┘
```

Key Overrides I use:
* `Shift` + `,` = `!`
* `Shift` + `.` = `?`
* `Shift` + `/` = `\`
* `Cmd` + `Q` = `Cmd` + `Tab` (quit too many apps adapting to this layout lol)

### PCB

Version 0.1 - First PCBA ordered from JLCPCB, it works!

### Firmware

Vial firmware is compiled [here](vial/)

QMK firmware source will be added soon

### Case

Can be 3D printed or CNC'd

Case Parts
* Plate - 1.5mm, can be laser cut
* Top Case (multiple options)
  * Angled slot for iPad Mini (6th gen)
  * todo
* Bottom Case
* 4x M2.5 12mm counter sunk screws
* (if 3D printing) 4x M2.5 5mm hex standoffs or similar nut
* Feet/bumpons

## What's Next

I'm quite satisfied with getting this working, and I had to order a minimum of 5 PCBs so I don't plan on making more for a while. But if you find this and use it as an example, here are some ideas of what could be added or improved:
* Layouts
  * Support for more spacebar layouts like 2u in between the existing keys
  * Clip-in stabilizer support
* PCB design
  * Cluster or consolidate the Reset and Boot pins. I was more concerned with finding a place they fit and were easy to route, but it's quite odd especially now that I know you have to either press them both simultaneously or hold Boot while plugging in the USB (which I put on opposite sides).
  * Improve routing and reduce PCB "forehead". But I kind of like the look.
  * Try another MCU. The Raspberry Pi is totally fine, but there are other MCUs that have more packaged features like flash and crystal, so that would be fewer parts to order, and easier to route.
* Other features
  * Add more hardware features like LEDs, ESD, etc.
  * Breakout pins to add hardware features or a daughter board later

## Thanks to

For excellent custom keyboard and PCB tutorials (highly recommend starting here if you are interested): [Noah Kiser](https://www.youtube.com/@noahkiser), [Joe Scotto](https://www.youtube.com/@joe_scotto)

For layout inspiration: Zicodia ("LMAO"), tominabox1 and whydobearsxplod ("QAZ"), Jack Humbert ("Planck")

## Disclaimer

**Offered without warranty or liability! Use/modify/order at your own risk. No customer support.**

For a first attempt, and as a hobby project, it turned out quite well! But this was just for fun and not made with the rigor or intent to commercialize it (for now...) so it isn't perfect.

Feel free to use this repository under the license provided. If it helps you make something cool, I want to see it!