# PCB Design Documentation

## Subsystem Overview
This custom 2-layer printed circuit board (PCB) was designed for the PIC18F57Q43 Curiosity Nano subsystem. The board features standard $0.2\text{ mm}$ signal traces, $0.4\text{ mm}$ $+5\text{V}$ power distribution rails, dual top and bottom ground planes (`F.Cu` and `B.Cu`), and custom knockout copper text for top/bottom layer identification and compliance.

---

## Technical Specifications & Manufacturing Rules
* **Board Dimensions:** $100\text{ mm} \times 100\text{ mm}$ (Max Envelope)
* **Layer Count:** 2-Layer ($0.5\text{ oz}$ Copper Weight)
* **Minimum Drill / Pad Size:** $1.0\text{ mm}$ Drill / $1.7\text{ mm}$ Pad Diameter
* **Trace Widths:** $0.2\text{ mm}$ Signal Netclass | $0.4\text{ mm}$ Power (`+5V`) Netclass
* **Clearance:** $0.25\text{ mm}$ Minimum Spacing
* **Text & Markings:** "Knockout" text on `F.Cu` and mirrored "Knockout" text on `B.Cu`

---

## PCB Layout Views

### Top Layer (`F.Cu`)
![PCB Top Layout Image]()

### Bottom Layer (`B.Cu`)
![PCB Bottom Layout Image]()

---

## Design Rule Check (DRC) Verification
The completed layout was verified using KiCad's Design Rules Checker with zone refills enabled, confirming **0 Errors** and **0 Warnings**.

![DRC Verification Screenshot]()
