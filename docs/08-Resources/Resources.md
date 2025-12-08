---
title: Resources
---

## ** Microcontroller Code ** 


## Team Code
This firmware controls the ClapSense Hub by combining motor control, clap detection, light-sensor gating, distance-based LED brightness, and UART logging into one integrated state machine. The program reads Aaron’s clap input on RA0 to determine toggle events, checks Quinn’s light sensor on RA1 to ensure the motor only runs when the sensor is covered, and converts Roshan’s distance sensor readings on RA3 into a smooth LED fade using the DAC. A three-state motor controller manages OFF and ON behavior based on clap toggles, while a brightness lookup table maps distance values into six intensity levels that transition smoothly using a weighted average filter. Throughout operation, the system logs ADC distance measurements over UART and updates motor and LED outputs every 50 ms, producing a responsive and stable embedded system that synchronizes all three subsystem inputs into coordinated motor and LED behavior.


### Downloads  
- [Team Subsystem Hardware Functionality project ZIP](C.Yuen.PrototypeTest.v1.zip)


## Individual Code
This program implements a reliable single-button control system for driving a motor using the PIC18F57Q43 Curiosity Nano. The on-board pushbutton (RB4) is used to detect single-press, double-press, and long-press input, each mapped to a different motor action. A single press runs the motor forward with a solid LED indicator, a double press reverses the motor with a blinking LED, and a long press stops the system entirely. To ensure accurate input recognition, the code includes a custom debouncing and timing engine that filters noise and distinguishes between press types. This creates a smooth, intuitive control interface that operates safely and consistently, demonstrating robust embedded design and state-based motor control.


### Downloads  
- [ Individual Hub Hardware Functionality project ZIP](C.Yuen.PrototypeTest.v2.zip)
