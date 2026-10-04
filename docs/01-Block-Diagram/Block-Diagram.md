---
title: Individal Block Diagram
tags:
- tag1
- tag2
---

### Subsystem Electrical Overview

#### Purpose of the Block Diagram
The purpose of this individual subsystem block diagram is to define the hardware layout, signal conditioning stages, and electrical interfaces for the light-sensing subsystem prior to schematic capture and PCB layout. It serves as a visual guide for component selection, pin mapping on the PIC18F57Q43 Curiosity Nano microcontroller, voltage management, and inter-board connectivity with teammates' hardware.

---

#### System Specifications & Key Features

* **Power Source & Supply Voltage:**  
  The subsystem is powered by a regulated **+5V DC** power domain capable of delivering up to **1.5A** via an LM7805 linear voltage regulator. This rail powers the microcontroller, analog signal conditioning components, and sensor interface.

* **Power Levels:**  
  All signal levels operating within this block maintain a nominal voltage range of **0 to 5V DC** across both analog input paths and digital serial communication lines.

* **Sensor & Signal Conditioning:**  
  * **Sensor:** A 5540 photoresistor configured in a voltage divider continuously measures ambient light levels.  
  * **Signal Conditioning:** The variable analog output from the photoresistor passes through a Microchip MCP6004 operational amplifier configured as a non-inverting buffer. This stage provides high input impedance to prevent loading on the sensor divider and low output impedance to cleanly drive the microcontroller's `RA0` ADC pin.

* **Team Connections & Communication Interfaces:**  
  Inter-board connectivity and system-wide integration are handled through standard ribbon cable connector **Connector 1**:
  * **Digital Serial (UART):** Transmit (`TX` on pin `RC2`) and Receive (`RX` on pin `RC3`) signals interface with teammates' boards via dedicated 5V UART lines at pins 2 and 3 of Connector 1.
  * **Shared Ground & Power:** Pin 8 of Connector 1 establishes a common ground (`GND`) across all team boards to maintain a consistent signal reference.
To get some initial formatting help, one can view ["here"](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/Appendix/basic-markdown-examples/) some basic techniques.


## Block Diagram 
![](IndividualBlockDiagram.drawio(1).png)
