---
title: Branden Cluff  
tags:  
- tag1  
- tag2  
---
<center>
<font size= "6">Branden Cluff Datasheet</font><br>
as part of<br>
<font size= "8">EGR 304 Course Project</font><br>
for<br>
<font size= "5"> Team 202 </font><br>

**Submission: month, DD, YYYY**
</center>

# Low-Power Environmental Monitoring System

## Introduction

This datasheet documents the hardware design, PCB layout, component selection, and embedded C firmware for a low-power environmental monitoring node. It serves as a clear technical guide for building, programming, and testing the system.

---

### Project Summary

This repository contains my individual subsystem for our team's EGR304 Embedded Systems Design project. My system monitors real-time environmental data—including atmospheric pressure, relative humidity, and ambient light levels—using a PIC18F57Q43 Curiosity Nano microcontroller. 

The module processes sensor data, displays values on an LCD screen, and sends live data over UART to a central display. It runs on a custom regulated power circuit designed for efficiency and reliable operation.

For full context on how this node integrates into our overall system, see our [Team Report](https://embedded-systems-design.github.io/EGR304TeamTemplate/).

---

### My Contribution

I designed and built this subsystem from circuit concept to hardware testing. Key contributions include:

* **Schematic Design:** Created KiCad schematics using US symbol standards for the power regulator, sensors, and display interfaces.
* **PCB Layout:** Completed component placement, signal routing, DRC verification, and Gerber file generation for manufacturing.
* **Firmware Development:** Wrote C code in MPLAB X IDE for the PIC18F57Q43, featuring a multi-sample rolling buffer for digital signal smoothing and UART data output.
* **Hardware Validation:** Tested power rails and verified sensor data output using an oscilloscope and digital multimeter.

