# ESP_game
> A custom-built, story-driven 3D Raycaster First-Person Shooter & Retro Game Engine designed for a DIY handheld console powered by an ESP32 microcontroller.

---

## Overview
**ESP_game** is an open-source, high-performance retro gaming platform built from scratch for resource-constrained microcontrollers. Leveraging a dual-core ESP32, `TFT_eSPI` graphics acceleration, and optimized fixed-point DDA raycasting, this project delivers a smooth 3D first-person shooter experience (Wolfenstein 3D / DOOM style) complete with textured walls, sprite-based enemies, weapons, dual-analog stick controls, and image-driven story cutscenes—all running locally on a tiny 1.8-inch TFT display.

---

## Hardware Specifications & Pinout

### Microcontroller & Power
* **MCU:** ESP32-S3 DevKit-N16R8 Board
* **Power Management:** TP4056 charging module + 3.7v lipo battery + slide switch.
* **Audio:** I2S Audio Breakout - MAX98357A + 8Ω speaker.

---

## Journal

So, one day sitting in class, I was looking at the kids playing in gaming consoles inside the class. I remembered I once had a gaming consoles with TETRIS, and a few more games. In my childhood, when I was 8-10 years old, I've seen many of my friends get a game setup, but I never had mine. So I started thinking, what if I can make myself a gaming console. 
Pretty much, we all use AI for some random intrusive thoughts. I typed in AI, can I make one, with these parts I've, and surely, it said "I can". So without any delay. I started finding the stuffs I require at the minimum, not high-end ones, but the ones which can satisfy a gamers **"Thrist"**.
So yea, doing that, I found the stuffs I've listed above. and also I'd provide the BOM below, dw ;)))

***HURDELS***
Finding the BOM, wasn't that time consuming. But the most time consuming was making the game, and till now, I've never made a game. 
And since, making a game to Run in a PC is different than making it run in a microcontroller with so limited space and processing power.
Cause, you know, no matter how potato the PC is, its still more powerful than a ESP32 (now I'm not talking about the 80s computers lol).

So once again, I went to the AI knowing what can I do, so it gave me a bunch of games which can be played in ESP32, but none satisfied me, cause they we're all like Flappy bird or snake and ladder. I wanted something immersive, something which can attract people. 
Then, after discussing with some of my elder brothers, I came up with this.
* Pseudo-3D Raycasting: Of heavy 3D graphics processors Pseudo-3D Raycasting uses fast 2D grid math, similar, to classic Wolfenstein 3D to fake 3D walls and corridors.
* Flash Storage (PROGMEM): All wall textures, enemy sprites and map data are stored directly in the ESP32s 4MB Flash memory, which saves the 320KB RAM.
* RAM Buffering: The game builds each frame in a lightweight memory buffer, called TFT_eSprite. Dumps it to the screen all at once which completely eliminates screen flicker.
* Direct Hardware Polling: Your joysticks and buttons are read via low‑overhead ADC and digital pin checks, which gives zero input lag.

So hey, one big problem solved.  :))

So, this all took me, more than 2 days to figure out, but hey!! I only worked for couple of hour or so, cause 24hrs of the day, I obviously wasn't working :p



Then came the Designing part. I drew this... Crazy huh! ;p

---

<img width="1280" height="823" alt="WhatsApp Image 2026-11-09 at 6 45 23 PM" src="https://github.com/user-attachments/assets/5f6731ed-e19a-48b2-a8be-43873600fe96" />

With the Drawing being done. I Quickly started doing the 3d model, which was very very basic, cause I'm a absolute beginner.

![Screenshot 2026-11-09 at 7 01 18 PM](https://github.com/user-attachments/assets/9a10e7a9-4a30-4b67-a48a-2d0ff530f51a)


Just tried to keep it as simple as I could, with a bit of grips. :))

### The BOM


| Part | Description | Qty | Unit Price | Total Price |
| :--- | :--- | :---: | :---: | :---: |
| **1.8" TFT SPI display** | The main Display | 1 | $3.29 | $3.29 | 
| **Joystick modules** | Controls | 1 | $2.23 | $2.23 |
| **TP4056** | Charging module | 1 | $1.09 | $1.09 | 
| **I2S Audio Breakout - MAX98357A** | The audio output | 1 | $2.07 | $2.07 |
| **ESP32-S3 DevKit-N16R8 Board** | The Brain | 1 | $10.42 | $10.42 |
| **3.7v 2000mAh Battery** | The power Source | 1 | $4.23 | $4.23 | 
| **FP6291 Boost Module** | To power the ESP32 stably | 1 | $1.59 | $1.59 |
| *Tax & shipping* | *for the whole order* | *-* | *-* | *$2.00* |
| **TOTAL** | **Estimated Project Cost** | **7** | — | **$26.92** |

The links for the seller is already given in the BOM.csv, so please go check it out. :)


### PCB
Yes, I'm definitely not making PCB, because, PCB delivery to my place would take up the whole budget. It's delivery charge costs me 25$ 
