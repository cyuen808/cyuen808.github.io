---
title: Welcome
tags:
- tag1
- tag2
---
<center>
<font size= "6"> Caleb Yuen's Datasheet</font><br>
as part of<br>
<font size= "8"> ClapSense </font><br>
for<br>
<font size= "5"> Team 204 </font><br>

**Submission: December 1, 2025**
</center>

## Introduction

This datasheet explains the design and setup of my subsystem, the Master Controller (Hub), for Team 204’s ClapSense Smart Light. It shows how my board interfaces with the Audio Front-End, Light Sensor Board, and Sensor Front-End, and how it controls the actuator system using a FAN8100N H-Bridge to toggle the lamp when a valid clap is detected.  

The goal of this project is to create a smart lighting system that responds only to intentional user input while remaining safe, modular, and easy to set up through a low-voltage 9 V → 5 V regulated power design.




### Project Summary

ClapSense is built around a single Microchip PIC18F57Q43 Curiosity Nano that serves as the Master Controller (Hub). The Audio Front-End detects claps, the Light Sensor Board senses outside light to automatically shut off system, and the Sensor Front-End measures ambient light levels for adaptive brightness.  

The Master Controller processes all inputs, filters valid clap patterns, and sends control signals through the FAN8100N H-Bridge to the 6 V DC motor, creating precise and safe actuation.  
This project integrates key embedded system principles such as signal processing, sensor feedback, power regulation, and actuator control to deliver a reliable, low-voltage, and hands-free smart lighting experience.

*[ClapSense Team Report.](https://asu-egr304-2025-f-204.github.io/)


### My Contribution

As the Team Lead and Master Controller (Hub) designer for the ClapSense project, Caleb developed the main subsystem that coordinates all communication between the Audio Front-End, Light Sensor Board, and Sensor Front-End.

I designed the schematic and PCB for the Hub circuit, selected and justified key components such as the FAN8100N H-Bridge and DFRobot FIT0495-A DC motor, and documented how the 5 V logic, 5 V power regulation, and actuator control integrate safely within the team’s modular 8-pin ribbon interface. 

Beyond technical design, he ensured consistent documentation, power and logic standardization across all boards, and led coordination between team members during schematic review, PCB layout, and website integration for Team 204’s final submission.

