# Tamaguino 🐣 — Modified Arduino Tamagotchi Clone

This project is my custom, expanded, and personalized version of the original Tamaguino digital pet created by Alojz Jakob. His project includes the full game logic, UI, and animations.

Original project: [https://alojzjakob.github.io/Tamaguino/](https://alojzjakob.github.io/Tamaguino/)
All core logic, art, animations, and design belong to their respective creators.
My repo contains personal modifications and additions.

My version rebuilds the hardware using an Arduino Nano, adds a few new features, cleans up parts of the code, and includes my own custom 3D-printed Tamagotchi-style enclosure (basically the Tamagotchi I never had growing up).

---

## What I Changed / Added

### Hardware Changes

* Switched from Arduino Pro Mini → Arduino Nano (more memory + easier USB programming)
* Using the internal pull-up resistor version
* Cleaned up wiring for the OLED display and buttons
* Added a speaker for simple sound effects
* Added a light sensor (LDR + resistor) for potential brightness-based behavior or “sleep mode”
* Designed and 3D-printed my own enclosure inspired by classic Tamagotchis

### Software Changes

* Added a mood system (happy / neutral / sad) with matching animations
* Added a startup splash screen
* Improved button responsiveness on the Nano
* Cleaned up portions of the code structure
* Minor adjustments to OLED layout for clearer text spacing
* Added placeholders for future features:

  * EEPROM save/load
  * Mini-games
  * More animations
  * Sound upgrades

---

## Parts I Used

* 0.96" I2C OLED Display (128×64)
* 3× momentary push buttons
* Small speaker
* Slide switch
* 150mAh LiPo battery
* LiPo charging board
* 10k resistor
* 7×5 cm prototyping PCB
* Wires

---

## Wiring Summary

**OLED**

* VCC → 5V
* GND → GND
* SDA → A4
* SCL → A5

**Buttons**

* Connected to digital pins

**Light Sensor**

* LDR → A0
* LDR → 5V
* 10k resistor → A0 → GND

**Speaker**

* Connected to digital pin & GND

---

## Code Files in This Repo

* `Tamaguino.ino` — original version using external resistors
* `tamaguino-noInputResistor.ino` — my modified version using internal pull-ups (the one I used)
* `config.yml` — configuration file from the original project
* `docs/` — original documentation
* `images/` — UI + sprite assets and original images
