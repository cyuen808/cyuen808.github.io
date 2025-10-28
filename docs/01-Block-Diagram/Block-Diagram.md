---
title: Individual Block Diagram
tags:
- tag1
- tag2
---

**Team 204 – Clap-Activated Smart Light**  
**Caleb Yuen – Master Controller (Hub)**  


## Overview
This page describes the hardware layout of my subsystem (Hub) for the team clap-activated light project. The Master Controller (PIC18F57Q43 Curiosity Nano) processes sensor data from the Audio, Filter, and Sensor Front-End boards, then drives the actuator to control the lamp output. The design uses an 8-pin ribbon-cable standard for consistent power and signal connections across all subsystems.


## Block Diagram 
![Caleb Yuen: Master Controller (Hub) ](HubController.png)
**Microcontroller:** Microchip PIC18F57Q43 Curiosity Nano  

**Inputs:**  
- Clap Signal (from Audio Board)  
- Potentiometer Input (from Filter Board)  
- Light Sensor (from Sensor Front-End)  

**Outputs:**  
- Lamp (Actuator) – toggles ON/OFF based on clap detection  
- Status LEDs (to Filter Board)  

**Communication:** Discrete GPIO over ribbon; no I²C in Rev 1. 
**Power:** “9 V DC in → 5 V (LM7805) → 3.3 V logic; common GND shared across all boards  

## Pin Assignment Table
| Connector | Pin | Signal | Direction | MCU Pin | Voltage |
|:-----------|:---:|:--------|:-----------|:---------|:---------|
| Filter Board | 1 | Potentiometer Input | Filter → Hub | RA1 | 3.3 V |
| Filter Board | 6 | Status LEDs | Hub → Filter | RB2 | 3.3 V |
| Audio Board | 3 | Clap Signal | Audio → Hub | RD0 | 3.3 V |
| Sensor Front-End | 3 | Light Sensor | Sensor → Hub | RD1 | 3.3 V |
| Actuator (Lamp) | — | Lamp Control | Hub → Lamp | RD2 | 3.3 V |


