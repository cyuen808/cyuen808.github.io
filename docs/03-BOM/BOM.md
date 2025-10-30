---
title: Bill of Materials
tags:
- tag1
- tag2
---

# Bill of Materials – ClapSense Hub (Master Controller)

This Bill of Materials (BOM) lists all components used in the Hub Subsystem (Master Controller) for the ClapSense project.  
The hub interfaces with the Filter Board and Sensor Front-End using an 8-pin ribbon connector and drives the lamp actuator through the TB6612FNG motor driver.

---

## Electronic Components

| Item | Ref(s) | Component | Description / Value | Qty | Vendor | Part # / Link | Notes |
|------|---------|------------|---------------------|------|---------|-----------------------|-------|
| 1 | U1 | PIC18F57Q43-CY | Microcontroller (40-pin) | 1 | Microchip | [DM164150](https://www.microchipdirect.com/dev-tools/DM164150?allDevTools=true) | Main controller |
| 2 | U2 | TB6612FNG | Dual Motor Driver IC | 1 | Digi-Key | [TB6612FNG](https://www.digikey.com/en/products/detail/toshiba-semiconductor-and-storage/TB6612FNG-C-8-EL/1730070) | Controls lamp actuator |
| 3 | M2 | DC Motor | Actuator (load) | 1 | DFRobot | [FIT0495A](https://www.digikey.com/en/products/detail/dfrobot/FIT0495-A/7087178) | Lamp actuator motor |
| 4 | U3 | LM7805 TO-220 | Voltage Regulator (9 V → 5 V) | 1 | Digi-Key |LM7805CT| Generates +5 V rail (Provided by Peralta) |
| 5 | J1 | Barrel Jack Connector | Power input (9 V DC) | 1 | Digi-Key | PJ-002AH | 9 V adapter input (Provided by Peralta)|
| 6 | F1 | Fuse | 1 A resettable fuse | 1 | Digi-Key | [RXE010](https://www.digikey.com/en/products/detail/littelfuse-inc/RXEF010/5015919) | Power protection |
| 7 | J2, J3, J5 | 2×4 Header (8-Pin Ribbon) | Subsystem connectors | 3 | Digi-Key | M80-6100842 | Connects Hub to other boards (Provided by Peralta) |
| 8 | R1 | 220 Ω | Sensor bias resistor | 1 | Digi-Key | CF14JT220R | Light sensor filter (Provided by Peralta) |
| 9 | R2, R5 | 10 kΩ | Signal pull-down resistors | 2 | Digi-Key | CF14JT10K0 | For CLAP and FILTER inputs (Provided by Peralta) |
| 10 | R3 | 1 kΩ | LED current-limit | 1 | Digi-Key | CF14JT1K00 | RA2 status LED (Provided by Peralta) |
| 11 | R4 | 10 kΩ | Standby pull-down (TB6612FNG) | 1 | Digi-Key | CF14JT10K0 | Motor STBY control (Provided by Peralta) |
| 12 | C2, C4, C6, C7 | 0.1 µF | Decoupling capacitors | 4 | Digi-Key | CL21B104KBCNNNC | Noise suppression (Provided by Peralta) |
| 13 | C3 | 33 µF Electrolytic | Regulator input filter | 1 | Digi-Key | [EEU-FR1V330] (https://www.digikey.com/en/products/detail/panasonic-electronic-components/EEU-FR1V330/2433568) | Power stability |
| 14 | C5 | 47 µF Electrolytic | Regulator output filter | 1 | Digi-Key | [EEU-FR1V470] (https://www.digikey.com/en/products/detail/panasonic-electronic-components/EEU-FR1H470/9921029?gclsrc=aw.ds&gad_source=1&gad_campaignid=17922795960&gbraid=0AAAAADrbLlj2h-acRt6FR1rtV1C0-9vJ5&gclid=Cj0KCQjwmYzIBhC6ARIsAHA3IkRSNUjJ9bi6Rt_rW5wY0YCjNidS_U1EfIxTJpT5dkVRykROFs4YhKUaAp1HEALw_wcB) | Output smoothing |
| 15 | D1 | LED (Red 3 mm) | Indicator LED | 1 | Digi-Key | WP710A10ID | RA2 status indicator (Provided by Peralta) |
| 16 | Breadboard / Jumper Wires | Prototyping accessory | – | 1 set | Peralta | – | For breadboard testing (Provided by Peralta) |
| 17 | USB Cable (Micro-B) | Programming & Power | – | 1 | Peralta | – | For Curiosity Nano |

---

## System Notes
- Power Input: 9 V DC via barrel jack → LM7805 → +5 V rail.  
- Logic Level: 3.3 V I/O (compatible with Curiosity Nano).  
- Inter-Board Connection: 8-pin ribbon standard (+5 V, GND, signals).  
- Safety: 1 A fuse + decoupling capacitors at each subsystem.  
