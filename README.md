# GB Proton Pack

A Ghostbusters-inspired proton pack build based on the Arduino-driven design from the original Proton Pack project by Mike Simone (@MikeS11/ProtonPack).

This repository is a simplified, movie-accurate variant focused on the look and behavior seen in the first Ghostbusters film, while keeping the DFPlayer-based music functionality active.

## Overview

This build is designed to emulate the original movie-style proton pack behavior rather than the expanded multi-theme / overheat variant found in some other builds. In this version:

- Theme-based color variation is intentionally disabled
- Overheat / warning escalation logic is intentionally disabled
- The pack behaves as a straightforward first-movie-style prop
- Music playback remains enabled through the DFPlayer module

This repository retains the original LED and sound architecture while reducing the feature set to match the intended movie aesthetic.

## Original credit

This project is based on the original work by Mike Simone and the ProtonPack project at:

- GitHub: https://github.com/MikeS11/ProtonPack
- Author: @MikeS11 / Mike Simone

The code in this repository builds on that original design, adapted for this specific movie-accurate build.

## Repository structure

- `Code/` - Arduino source and supporting libraries
  - `Code/Proton_pack_noVentLights/Proton_pack_noVentLights.ino` - main firmware
  - `Code/Libraries/GBLEDPatterns/GBLEDPatternsJewel.h` - custom LED sequencing logic
  - `Code/Libraries/GB_Bargraph_Sequence/` - bargraph animation routines
  - `Code/Libraries/ht16k33-arduino-master/` - HT16K33 support library
- `GBSounds/` - DFPlayer sound files used for startup, firing, idle, tail, and warning effects
- `Diagrams/` - build diagrams and reference images
- `Parts List/` - list of parts and BOM materials
- `README.md` - repository documentation

## Behavior notes

This version is intentionally tuned to function in a way that matches the movie appearance and feel from Ghostbusters (1984), while still preserving the sound system used in the original build.

Key behavioral choices in this branch:

- Movie-style operation only
- Theme switching disabled
- Overheat behavior disabled
- Music / sound playback retained
- Pack startup and firing logic remains active

## Hardware used

This project uses the same type of hardware common to the original Proton Pack build:

- Arduino-compatible microcontroller
- NeoPixel LED strips / jewel modules
- DFPlayer Mini audio board
- Custom bargraph display and wand lighting
- Pack and wand control switches
- Audio amplifier / speaker output as needed

## Main firmware

The primary firmware is located here:

`Code/Proton_pack_noVentLights/Proton_pack_noVentLights.ino`

This file contains the logic for:

- boot sequence
- idle behavior
- firing animation timing
- wand LED control
- DFPlayer sound playback
- power down and shutdown routines

## Audio

The `GBSounds/` folder contains the sound assets used by the DFPlayer. These are selected by the firmware and can be used to recreate the movie-inspired sound and music feel for the prop.

## Build notes

1. Open the Arduino sketch in `Code/Proton_pack_noVentLights/`.
2. Install the required libraries from `Code/Libraries/`.
3. Ensure your wiring matches the pin definitions in the sketch.
4. Load the matching sound files onto the DFPlayer in the proper order.
5. Test startup, idle, firing, venting, and shutdown behaviors before final assembly.

## Credit and inspiration

- Original project: Mike Simone / MikeS11/ProtonPack
- This fork adapts that work toward a simpler movie-style build with disabled theme and overheat logic

## License

This repository does not currently include a separate license file. Please check the upstream project and original authorship before reusing or redistributing commercially.

## Notes

This project is a fan-made prop build inspired by Ghostbusters and is intended for personal and hobbyist use. It is not an official licensed prop or commercial product.
