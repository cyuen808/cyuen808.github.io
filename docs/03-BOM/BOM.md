---
title: Bill of Materials
tags:
- tag1
- tag2
---

# Bill of Materials – ClapSense Hub (Master Controller)

This Bill of Materials (BOM) lists all components used in the **Hub Subsystem (Master Controller)** for the ClapSense project.  
The hub interfaces with the **Filter Board** and **Sensor Front-End** using an 8-pin ribbon connector and drives the **lamp actuator** through the TB6612FNG motor driver.

---

## Electronic Components

| Item | Ref(s) | Component | Description / Value | Qty | Vendor | Example Part # / Link | Notes |
|------|---------|------------|---------------------|------|---------|-----------------------|-------|
| 1 | U1 | PIC18F57Q43-CY | Microcontroller (40-pin) | 1 | Microchip | [DM164150](https://www.microchipdirect.com/) | Main controller |
| 2 | U2 | TB6612FNG | Dual Motor Driver IC | 1 | Digi-Key | [TB6612FNG](https://www.digikey.com/en/products/detail/toshiba/TB6612FNG) | Controls lamp actuator |
| 3 | M2 | DC Motor | Actuator (load) | 1 | DFRobot | [FIT0495A](https://www.dfrobot.com/product-535.html) | Lamp actuator motor |
| 4 | U3 | LM7805 TO-220 | Voltage Regulator (9 V → 5 V) | 1 | Digi-Key | [LM7805CT](https://www.digikey.com/en/products/detail/texas-instruments/LM7805CT) | Generates +5 V rail |
| 5 | J1 | Barrel Jack Connector | Power input (9 V DC) | 1 | Digi-Key | [PJ-002AH](https://www.digikey.com/en/products/detail/cui-devices/PJ-002AH) | 9 V adapter input |
| 6 | F1 | Fuse | 1 A resettable fuse | 1 | Digi-Key | [RXE010](https://www.digikey.com/en/products/detail/littelfuse/RXE010) | Power protection |
| 7 | J2, J3, J5 | 2×4 Header (8-Pin Ribbon) | Subsystem connectors | 3 | Digi-Key | [M80-6100842](https://www.digikey.com/en/products/detail/harwin/M80-6100842) | Connects Hub to other boards |
| 8 | R1 | 220 Ω | Sensor bias resistor | 1 | Digi-Key | CF14JT220R | Light sensor filter |
| 9 | R2, R5 | 10 kΩ | Signal pull-down resistors | 2 | Digi-Key | CF14JT10K0 | For CLAP and FILTER inputs |
| 10 | R3 | 1 kΩ | LED current-limit | 1 | Digi-Key | CF14JT1K00 | RA2 status LED |
| 11 | R4 | 10 kΩ | Standby pull-down (TB6612FNG) | 1 | Digi-Key | CF14JT10K0 | Motor STBY control |
| 12 | C2, C4, C6, C7 | 0.1 µF | Decoupling capacitors | 4 | Digi-Key | CL21B104KBCNNNC | Noise suppression |
| 13 | C3 | 33 µF Electrolytic | Regulator input filter | 1 | Digi-Key | EEU-FR1V330 | Power stability |
| 14 | C5 | 47 µF Electrolytic | Regulator output filter | 1 | Digi-Key | EEU-FR1V470 | Output smoothing |
| 15 | D1 | LED (Red 3 mm) | Indicator LED | 1 | Digi-Key | WP710A10ID | RA2 status indicator |
| 16 | Breadboard / Jumper Wires | Prototyping accessory | – | 1 set | Amazon | – | For breadboard testing |
| 17 | USB Cable (Micro-B) | Programming & Power | – | 1 | – | – | For Curiosity Nano |

---

## System Notes
- Power Input: 9 V DC via barrel jack → LM7805 → +5 V rail.  
- Logic Level: 3.3 V I/O (compatible with Curiosity Nano).  
- Inter-Board Connection: 8-pin ribbon standard (+5 V, GND, signals).  
- Safety: 1 A fuse + decoupling capacitors at each subsystem.  

---

## Order Submission Instructions
1. Group parts by vendor (Digi-Key, Microchip, DFRobot, etc.).  
2. Fill out the [EGR-3x4 Purchase Request Form](https://www.dropbox.com/scl/fi/zhj1hgknkkmxri7umonv2/EGR-3x4-Purchase-Request-2021.xlsx?dl=0).  
3. Email your .xlsx file to **Dr. Kevin Nichols (kwnicho@asu.edu)** for approval.  
4. Submit to Canvas along with this Markdown page exported as PDF.  

---

*Last Updated: October 30, 2025*  
*Author: Caleb Yuen — Hub Subsystem (Master Controller)*