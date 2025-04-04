# Ortho 4x10 TKL v0.1

![](images/ortho4x10tkl-photo.jpeg)

### Summary

An open-source custom mechanical keyboard featuring
* 4x10 ortholinear 'tenkeyless' style layout
* Raspberry Pi RP2040 integrated microcontroller
* USB-C
* Hotswap sockets
* Fully factory-assembled PCBA
* QMK Vial firmware

### Goals

The goals of this project were:
1. Learn how to make a working PCBA mechanical keyboard
2. Keep hardware features to the minimum (no LEDs, OLED, encoders, etc.)
3. Fun and delighful > practical
4. Companion for iPad Mini (6th gen)

### Layout

![](images/ortho4x10tkl-layout.png)

Spacebar cluster supports 3x1U and 1x3U layouts. Stabilizers are not currently supported but can be substituted with loose switches if desired.

Arrow cluster supports 4 or 6 keys, although the top cases in this repo will cover up 2 of them. Still, the switches are there if you prefer to have them.

### Keymap

This is my keymap, note that with VIAL firmware some setup will be manual in the VIAL application or loaded from a saved layout

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

Vial firmware is compiled in [here](vial/), along with saved keymaps (including combos and settings that could not be baked into the firmware) which can be loaded from the Vial application.

QMK firmware source will be added soon

### Case & Parts

Can be 3D printed or CNC'd. The 3D printed variants simply have hex holes to fit a standoff, which can be glued in and act as the thread for the screws. The CNC files will work for 3D printing as well if the holes on the top case are tapped manually.

| Part                                      |                          Note                           |
|-------------------------------------------|:-------------------------------------------------------:|
| PCBA                                      |                    [PCB files](PCB/)                    |
| Plate                                     | [Laser Cut Plate](Case/)<br/>1.5mm brass / steel / etc. |
| Top Case                                  |                [Multiple options](Case/)                |
| Bottom Case                               |                  [STL or STEP](Case/)                   |
| Screws                                    |                4x M2.5 10mm counter sunk                |
| Hex standoffs or nuts<br>(if 3D printing) |                       4x M2.5 5mm                       |
| Rubber feet/bumpons                       |                           4x                            |
| Switches and keycaps                      |                      36 to 40 each                      |

## What's Next

I'm quite satisfied with getting this working, and I had to order a minimum of 5 PCBs so I don't plan on making more for a while. But if you find this and use it as an example, here are some ideas of what could be added or improved:
* Layouts
  * Support for more spacebar layouts like 2u in between the existing keys
  * Clip-in stabilizer support
* PCB design
  * Move the USB - since the iPad plugs in on the right it could be nice and compact to put the USB on the right edge of the case
  * Cluster or consolidate the Reset and Boot pins. I was more concerned with finding a place they fit and were easy to route, but it's quite odd especially now that I know you have to either press them both simultaneously or hold Boot while plugging in the USB (which I put on opposite sides).
  * Improve routing and reduce PCB "forehead". But I kind of like the look.
  * Try another MCU. The Raspberry Pi is totally fine, but there are other MCUs that have more packaged features like flash and crystal, so that would be fewer parts to order, and easier to route.
* Other hardware features
  * Add more hardware features like LEDs, ESD, etc.
  * Breakout pins to add hardware features or a daughter board later
* Case
  * Support for more devices
  * Perfect the USB-C cutout
  * Design out of a single piece of aluminum to reduce cost

## Thanks to

For excellent custom keyboard and PCB tutorials (highly recommend starting here if you are interested): [Noah Kiser](https://www.youtube.com/@noahkiser), [Joe Scotto](https://www.youtube.com/@joe_scotto)

For layout inspiration: Zicodia ("LMAO"), tominabox1 and whydobearsxplod ("QAZ"), Jack Humbert ("Planck")

## Disclaimer

**Offered without warranty or liability! Use / modify / order at your own risk. No customer support.**

For a first attempt, and as a hobby project, it turned out quite well! But this was just for fun and not made with the rigor or intent to commercialize it (for now...) so it isn't perfect.

Feel free to use this repository under the license provided. If it helps you make something cool, I would be happy to see it!