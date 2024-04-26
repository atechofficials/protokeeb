# Protokeeb

![Protokeeb](https://i.imgur.com/RsSBoJg.jpg)

A 16-key (4 x 4) Keyboard/Numpad/Macropad/MIDI device designed by A-Tech Officials for easily getting started in the field of custom keyboards and open-source keyboard firmware.

Learn, build, and modify easily as the Protokeeb is an open-source hardware project.
The PCB is based on a Raspberry Pi Pico development board.
Designed for developers and enthusiasts who want to begin their journey in the world of custom keyboards and keyboard firmware.

## Features

- Per-key south-facing ARGB (WS2812B-2020) backlight LED.
- All anti-ghosting keys. It's a Mechanical Keyboard. Duh.
- N-Key Rollover
- ESD/EMI Protection on-board
- Rotary Encoder with push button.
- USB Type-C. Not a feature any more in 2024. #NoMoreMicroUSB
- Dedicated Bootselect and Reset Button.
- Supports different RP2040-based development boards that have similar SMD footprint and pinout to a Raspberry Pi Pico.
- 2MB/4MB Flash storage for all those feature-packed keyboard firmwares'.
- Keyboard Hardware supports QMK, KMK, and ZMK firmware.
- Support for both a Sandwich Style/Layered Case or a 3D printed Case.

## Supported Dev Boards

- Raspberry Pi Pico
- Raspberry Pi Pico W
- Waveshare RP2040-Plus

# Instructions/Guide

There are two options to get started with Protokeeb hardware:

- Option-1 either order the fully assembled/soldered PCB from [atechofficials](https://atechofficials.com/protokeeb.) (Work-in-progress)
- Option-2 or download the Gerber files and all the necessary files to order the PCB from your local/preferred PCB fabrication house/company and source all the required electronics components at per your convenience.

**Option-1** will be a straightforward plug and play option because each Protokeeb board comes flashed with QMK firmware and the default keymap. So, you can easily tinker around and customize without worrying too much about the electronics.

**Option-2** will be a DIY approach with detailed instructions for almost every step. So, that you can quickly start your custom keyboard journey filled with learning, development, and customization.

**Note:** Option-2 is not recommended for a person who is an absolute beginner in the field of electronics as this option requires a certain set of skills and basic electronics knowledge, not to mention good SMD soldering skills.

Follow this guide if you are ready to test your skills: [Assembly Instructions](https://github.com/atechofficials/protokeeb) (Work-in-progress)
