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

**Submission: October 31, 2025**
</center>

## Introduction
This datasheet explains the design and setup of my part of the project, the Master Controller or Hub, for the Team 204 Clap Activated Smart Light. It shows how my board connects with the Audio, Filter, and Sensor Front End boards, and how it controls the main actuator, which is the lamp that turns on and off when a valid clap is detected.  

The goal of this project is to create a smart lighting system that reacts only to real user input while staying simple to set up and safe to use with low voltage power.  



### Project Summary

Clapsense is built around a single Microchip PIC18F57Q43 Curiosity Nano that serves as the Master Controller. The Audio Front End detects claps, the Filter Board manages user inputs and status lights, and the Sensor Front End measures room brightness to help the system perform better.  

The Master Controller processes all inputs and sends a command to the lamp actuator, turning the light on or off at the right time.  
This project combines key embedded system concepts—signal processing, sensor integration, and actuator control—to create a reliable and hands-free lighting experience.

*[ClapSense Team Report.](https://asu-egr304-2025-f-204.github.io/)


### My Contribution
As the Team Lead and Master Controller (Hub) designer for the ClapSense project, Caleb developed the main subsystem that coordinates all communication between the Audio Front-End, Filter Board, and Sensor Front-End. His board, built around the Microchip PIC18F57Q43 Curiosity Nano, manages signal flow, initialization, and decision-making for the entire system.

He designed the schematic for the Hub circuit, selected and justified key components such as the TB6612FNG H-Bridge and FIT0495-A DC motor, and documented how the 3.3 V logic, 5 V power regulation, and actuator control integrate safely within the team’s modular 8-pin ribbon interface.

Beyond technical design, he ensured consistent documentation, power and logic standardization across all boards, and led coordination between team members during report development and website integration.

