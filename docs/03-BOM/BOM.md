---
title: Bill of Materials
tags:
- tag1
- tag2
---

# Bill of Materials – ClapSense Hub (Caleb Yuen)

This Bill of Materials (BOM) lists all electronic components and hardware needed to build and prototype the **Master Controller (Hub)** subsystem of the ClapSense project.  
The Hub uses the **PIC18F57Q43 Curiosity Nano** as its core microcontroller and interfaces with other subsystems (Audio Front-End, Filter Board, Sensor Front-End) via an 8-pin ribbon connector.


## Component List


| Item | Component | Description | Example Part / Value | Quantity | Vendor | Vendor Link | Notes |
|------|------------|--------------|----------------------|-----------|---------|--------------|-------|
| 1 | PIC18F57Q43 Curiosity Nano | Main MCU Board | DM164150 | 1 | Microchip / Digi-Key | [Microchip Direct](https://www.microchipdirect.com/) | Master controller for entire system |
| 2 | 8-Pin Ribbon Connector | Hub-to-spoke communication | 3M 89109-0081 | 2 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/detail/3m/89109-0081) | Used to connect subsystems |
| 3 | Male Header (2×4) | Ribbon cable interface | M80-6100842 | 2 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/detail/harwin/M80-6100842) | Connects Hub to ribbon cable |
| 4 | N-MOSFET | Lamp driver transistor | IRLZ44N / AO3400A | 2 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/detail/IRLZ44N) | Controls high-current lamp |
| 5 | LED (RA2) | Indicator LED | 3mm Red LED | 2 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/filter/leds-discrete) | Status indicator |
| 6 | Resistor | For LED current limiting | 330 Ω (¼W) | 3 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/filter/resistors-fixed) | Limits LED current |
| 7 | Barrel Jack Connector | Power input | PJ-002AH | 1 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/detail/cui-devices/PJ-002AH) | Power jack for 9V input |
| 8 | Voltage Regulator | 9V → 5V conversion | LM7805 / AMS1117-5.0 | 2 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/detail/texas-instruments/LM7805CT) | Provides stable 5V rail |
| 9 | Capacitor | Power decoupling | 0.1 µF + 10 µF | 4 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/filter/ceramic-capacitors) | Noise filtering for MCU and regulator |
| 10 | Jumper Pins / Test Points | Debug and testing | TP001 | 4 | Digi-Key | [Digi-Key](https://www.digikey.com/en/products/detail/keystone-electronics/5019) | Used for debugging / voltage checks |
| 11 | Breadboard + Dupont Wires | Prototyping hardware | – | 1 set | Amazon | [Amazon](https://www.amazon.com/) | For circuit breadboard testing |
| 12 | USB Cable | For Nano power & programming | USB Micro-B | 1 | – | – | Standard USB cable |

---

## ⚙️ Ordering Notes

- Order **1 per breadboard prototype**, **1 per PCB instance**, plus **1–2 extras** for backup.  
- Verify availability and shipping time before submitting order forms.  
- Group items by vendor (Digi-Key, Microchip Direct, Amazon).  
- Use the [EGR-3x4 Purchase Request Template](https://www.dropbox.com/scl/fi/zhj1hgknkkmxri7umonv2/EGR-3x4-Purchase-Request-2021.xlsx?dl=0) to complete vendor order sheets.  
- Submit **.xlsx** purchase request via email to **Dr. Kevin Nichols (kwnicho@asu.edu)** and upload your **BOM page PDF + Excel form** to Canvas.

---

## 🧠 Design Reference

- **Microcontroller:** [PIC18F57Q43 Curiosity Nano User Guide](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/UserGuides/PIC18F57Q43-Curiosity-Nano-HW-UserGuide-DS40002186B.pdf)  
- **Subsystem Architecture:** Hub-and-Spoke system (Caleb = Hub)  
- **Power Input:** 9V Barrel Jack → 5V Regulator → PIC 3.3V Logic  

---