---
title: Microcontroller Code
---

## Overview
This program implements a reliable single-button control system for driving a motor using the PIC18F57Q43 Curiosity Nano. The on-board pushbutton (RB4) is used to detect single-press, double-press, and long-press input, each mapped to a different motor action. A single press runs the motor forward with a solid LED indicator, a double press reverses the motor with a blinking LED, and a long press stops the system entirely. To ensure accurate input recognition, the code includes a custom debouncing and timing engine that filters noise and distinguishes between press types. This creates a smooth, intuitive control interface that operates safely and consistently, demonstrating robust embedded design and state-based motor control.


### Downloads  
- [Download KiCad project ZIP](C.Yuen.PrototypeTest.v2.zip)






