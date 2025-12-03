---
title: Bill of Materials
tags:
- tag1
- tag2
---

# Bill of Materials – ClapSense Hub (Master Controller)

This Bill of Materials (BOM) lists all components used in the Hub subsystem (Master Controller) for the ClapSense project.  
The Hub interfaces with the Audio Front-End, Light Detector Board, and Distance Front-End through 8-pin ribbon connectors and drives the lamp actuator using the FAN8100N H-Bridge motor driver.






---

## Electronic Components

| Item | Ref(s) | Component | Description / Value | Qty | Vendor | Part # / Link | Notes |
|------|---------|------------|---------------------|------|---------|-----------------------|-------|
| 1 | U2 | PIC18F57Q43-CY | Microcontroller (40-pin) | 1 | Microchip | [DM164150](https://www.microchipdirect.com/dev-tools/DM164150?allDevTools=true) | Main controller |
| 2 | U4 | FAN8100N | Motor Driver Bipolar Parallel 12-DIP | 1 | Digi-Key | [FAN8100N](https://www.digikey.com/en/products/detail/fairchild-semiconductor/FAN8100N/11558200) | Controls LED actuator |
| 3 | M1 | DC Motor | Actuator (load) | 1 | DFRobot | [FIT0495A](https://www.digikey.com/en/products/detail/dfrobot/FIT0495-A/7087178) | Lamp actuator motor |
| 4 | U1 | LM7805 TO-220 | Voltage Regulator (9 V → 5 V) | 1 | Digi-Key |LM7805CT| Generates +5 V rail (Provided by Peralta) |
| 5 | J1 | Barrel Jack Connector | Power input (9 V DC) | 1 | Digi-Key | PJ-002AH | 9 V adapter input (Provided by Peralta)|
| 6 | F1 | Fuse | 1 A resettable fuse | 1 | Digi-Key | [RXE010](https://www.digikey.com/en/products/detail/littelfuse-inc/RXEF010/5015919) | Power protection |
| 7 | J2, J3, J9 | 2×4 Header (8-Pin Ribbon) | Subsystem connectors | 3 | Digi-Key | M80-6100842 | Connects Hub to other boards (Provided by Peralta) |
| 8 | R2 | 220 Ω | Sensor bias resistor | 1 | Digi-Key | CF14JT220R | Light sensor filter (Provided by Peralta) |
| 9 | R1 | 10 kΩ | Signal pull-down resistors | 2 | Digi-Key | CF14JT10K0 | For CLAP and FILTER inputs (Provided by Peralta) |
| 10 | R4 | 1 kΩ | LED current-limit | 1 | Digi-Key | CF14JT1K00 | RA2 status LED (Provided by Peralta) |
| 11 | R6, R7 | 10 kΩ | Standby pull-down (FAN8100N) | 1 | Digi-Key | CF14JT10K0 | Motor STBY control (Provided by Peralta) |
| 12 | C3, C7, C8, Cnano1 | 0.1 µF | Decoupling capacitors | 4 | Digi-Key | CL21B104KBCNNNC | Noise suppression (Provided by Peralta) |
| 13 | Cnano2 | 4.7 µF | Decoupling capacitors | 1 | Digi-Key | CL21B104KBCNNNC | Noise suppression (Provided by Peralta) |
| 14 | C3 | 10 µF Electrolytic | Regulator input filter | 1 | Digi-Key | Provided by Peralta | Power stability |
| 15 | C6 | 100 µF Electrolytic |  Decoupling capacitors | 1 | Digi-Key | Provided by Peralta | Power stability |
| 16 | D1 | LED (Red 3 mm) | Indicator LED | 1 | Digi-Key | WP710A10ID | RA2 status indicator (Provided by Peralta) |
| 17 | Breadboard / Jumper Wires | Prototyping accessory | – | 1 set | Peralta | – | For breadboard testing (Provided by Peralta) |
| 18 | USB Cable (Micro-B) | Programming & Power | – | 1 | Peralta | – | For Curiosity Nano |
| 19| J2, J3, J9 | 8-Pin IDC Ribbon Cable | Standard 8-conductor ribbon cable with connectors attached (2×4 pin) | 3 | Peralta | – | Cable that connects Hub ↔ Filter ↔ Sensors |


---

## System Notes
- Power Input: 9 V DC via barrel jack → LM7805 → +5 V rail.  
- Logic Level: 5 V I/O (compatible with Curiosity Nano).  
- Inter-Board Connection: 8-pin ribbon standard (+5 V, GND, signals).  
- Safety: 1 A fuse + decoupling capacitors at each subsystem.  
