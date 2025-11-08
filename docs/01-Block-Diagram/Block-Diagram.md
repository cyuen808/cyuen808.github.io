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
![Caleb Yuen: Master Controller (Hub) ](egr304-team204-block-diagram-hub.jpg)

**Microcontroller:** Microchip PIC18F57Q43 Curiosity Nano  

**Inputs:**
- CLAP_IN from Audio Board  
- FILTER_SIGNAL_IN  from Light Detector Board  
- FILTER_TOGGLE from Light Detector Board  

**Outputs:**
- FILTER_STATUS_LED to Filter/Light Detector Board  
- PWM_MOTOR to Distance Front-End  
- MOTOR_IN1, MOTOR_IN2, MOTOR_STBY to Distance Front-End  
- Heartbeat LED on Hub board  

**Communication:** Discrete GPIO over ribbon; no I²C in Rev 1.  
**Power:** 9 V DC in → 5 V (LM7805) → 3.3 V logic; common GND shared across all boards.

---

## Pin Assignment Table

| Pin | Signal              | Direction        | Source → Destination         | MCU Pin (PIC18F57Q43) | Voltage             | Notes |
|-----|---------------------|------------------|------------------------------|------------------------|---------------------|--------|
| 1   | GND                 | —                | —                            | —                      | 0 V                 | Common ground shared across all subsystems |
| 2   | +5V_SYS             | —                | Power → All Boards           | —                      | 5 V                 | Regulated output from LM7805 (VM → 5 V) |
| 3   | CLAP_IN             | Input            | Audio Board → Hub            | RB0                    | 3.3 V (via divider) | Digital clap detection signal |
| 4   | FILTER_SIGNAL_IN    | Input            | Light Detector → Hub         | RA0                    | 3.3 V (via divider) | Filtered threshold logic |
| 5   | FILTER_TOGGLE       | Input            | Light Detector → Hub         | RB1                    | 3.3 V (via divider) | Lamp toggle command |
| 6   | FILTER_STATUS_LED   | Output           | Hub → Light Detector Board   | RA2                    | 3.3 V               | Status indicator LED |
| 7   | PWM_MOTOR           | Output (PWM)     | Hub → Distance Front-End     | RB2 (PWM1)             | 3.3 V               | PWM control for motor/actuator |
| 8   | MOTOR_STBY          | Output           | Hub → Distance Front-End     | RA5                    | 3.3 V               | Enables H-Bridge (FAN8100N) |
| 9   | MOTOR_IN1           | Output           | Hub → Distance Front-End     | RB3                    | 3.3 V               | Motor direction A |
| 10  | MOTOR_IN2           | Output           | Hub → Distance Front-End     | RB4                    | 3.3 V               | Motor direction B |
| 11  | GND                 | —                | —                            | —                      | 0 V                 | Interleaved ground for noise reduction |
| 12  | UART_RX_FILTER      | Input (optional) | Light Detector → Hub (Debug) | RC7 (RX)               | 3.3 V               | Serial receive for debug |
| 13  | UART_TX_FILTER      | Output (optional)| Hub → Light Detector (Debug) | RC6 (TX)               | 3.3 V               | Serial transmit for debug |
| 14  | SPARE               | —                | —                            | —                      | —                   | Reserved for future expansion |

---

**Notes**

- All PIC18F57Q43 logic operates at **3.3 V**.  
- External 5 V signals from other boards are stepped down using 10 kΩ / 20 kΩ voltage dividers.  
- Only **+5V_SYS** and **GND** are shared between boards; interleave GND pins (1 and 11) to reduce EMI and noise.  
- UART pins (12–13) are optional for debugging with the Light Detector Board.  
- PWM, IN1, IN2, and STBY connect to the FAN8100N H-Bridge on the Distance Front-End to drive the DFRobot 6 V metal gear motor.
