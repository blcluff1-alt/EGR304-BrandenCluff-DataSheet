---
title: Schematic
---

# Individual Schematic Design: Light-Sensing Subsystem

## Overview
This repository contains the individual ECAD schematic design for the **Light-Sensing Subsystem** developed using **KiCad** for the EGR 304 engineering design project. The subsystem integrates power regulation, microcontroller interfacing, analog signal conditioning, and debugging hardware around a PIC18F57Q43 Curiosity Nano platform.

---

## Functional Subsystems

* **Power Regulation Subsystem**
  * Accepts external input ($9\text{V}$–$12\text{V}$) via a through-hole Barrel Jack (`J2`) protected by a 500 mA inline fuse (`F1`).
  * Utilizes input ($0.33\text{ }\mu\text{F}$) and output ($0.1\text{ }\mu\text{F}$) filtering capacitors alongside an LM7805 linear regulator (`U3`) and a 100 $\Omega$ preload resistor (`R3`) to establish a stable $5\text{ V}$ rail.

* **Microcontroller Unit (MCU)**
  * Implemented using a custom-designed PIC18F57Q43 Curiosity Nano symbol (`U1`) featuring proper decoupling capacitance (`C3`) and dedicated UART communication routing (`CDC_RX`, `CDC_TX`) for upstream/downstream interfacing.

* **Light Sensor & Signal Conditioning Subsystem**
  * Employs a photoresistor voltage divider (`R1`, `R2`) to detect ambient light.
  * Conditions the analog signal through an MCP6004 quad operational amplifier configured as a unity-gain buffer (`U2A`), with unused channels safely terminated.

* **User Interface & Debugging Subsystem**
  * Includes a power-status indicator LED (`D1`, $330\text{ }\Omega$ resistor `R6`) and a microcontroller-driven debug LED (`D2` on `RA1`, $330\text{ }\Omega$ resistor `R7`).
  * Features an active-low pushbutton (`SW1` on `RA2`) with a $10\text{ k}\Omega$ pull-up resistor (`R8`) for testing and user input.
  * Interfaces with external hardware and signals via a dedicated ribbon cable connector (`J1`).

---

## Project Files & Documentation



![Schematic Overview](../304circuitschm.png)



## Resouces

The schematic as a PDF download is available [*here*](304circuit.pdf), and the Zip folder of the project schematic [*here*](dummyZip.zip). also the custom symbol library [*here*](Custom_Libraries.zip)
