---
title: Schematic
---

## Overview

This schematic shows my PIC18F57Q43 Curiosity Nano controlling a TB6612FNG motor-driver circuit with a 6 V metal gearmotor (FIT0495A). It includes a 9V → 5 V LM7805 regulator, fuse protection, 3.3 V logic interface, and all system connections defined in our team block diagram.



### Schematic Preview  
![C_Yuen_Hub_Schematic](C_Yuen_Hub_Schematic.png)

### Downloads  
- [View full PDF schematic](C_Yuen_Hub_Schematic.pdf)  
- [Download KiCad project ZIP](C_Yuen_Hub_Project.zip)


### Notes  
- Logic = 3.3 V (VTG from PIC)  
- Motor rail = 6 V external  
- Input 9V DC → Fuse → LM7805 → +5 V rail  
- TB6612FNG internal MOSFET diodes handle motor back-EMF  

_Last updated on 2025-10-18_