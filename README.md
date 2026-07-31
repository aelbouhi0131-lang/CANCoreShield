<div align="center">

# CANCore Shield

A professional **Arduino UNO CAN-Bus Shield** designed in **Altium Designer**, featuring CAN communication, microSD storage, power management, and hardware improvements over existing open-source designs.

![Altium Designer](https://img.shields.io/badge/Altium-Designer-A5915F?style=for-the-badge)
![Arduino UNO](https://img.shields.io/badge/Arduino-UNO-00979D?style=for-the-badge)
![CAN Bus](https://img.shields.io/badge/CAN-Bus-red?style=for-the-badge)
![PCB](https://img.shields.io/badge/PCB-2_Layers-success?style=for-the-badge)
![DRC](https://img.shields.io/badge/DRC-0_Errors-brightgreen?style=for-the-badge)
![Gerbers](https://img.shields.io/badge/Gerbers-Ready-blue?style=for-the-badge)
![Open Hardware](https://img.shields.io/badge/Open-Hardware-orange?style=for-the-badge)
![Embedded Systems](https://img.shields.io/badge/Embedded-Systems-blueviolet?style=for-the-badge)

---

Designed by **Ayoub ELBOUHI**

Electrical Engineering & Embedded Systems Student

ENSA Marrakech

</div>

---

# Overview

CANCore Shield is a compact **Arduino UNO expansion board** developed for **CAN-Bus communication** and **embedded system applications**.

The project was inspired by existing open-hardware CAN shields (including the Seeed Studio CAN-BUS Shield) but redesigned from scratch with several improvements focused on:

- Hardware reliability
- Power management
- SD card compatibility
- PCB organization
- Ease of debugging
- Manufacturing readiness

The entire project was designed using **Altium Designer**, following professional PCB design practices and successfully verified with **0 Design Rule Check (DRC) errors**.

---

# Key Features

- Arduino UNO Shield Form Factor
- MCP2515 CAN Controller
- TJA1050 CAN Transceiver
- SPI microSD Card Interface
- Bidirectional Logic Level Translator
- Dedicated Power Management Circuit
- ON/OFF Power Switch
- Power & Status LEDs
- Optimized Ground Planes
- Two-Layer PCB
- STEP 3D Model Included
- Manufacturing Ready
- Fully DRC Verified

---

# Design Improvements

Unlike the reference open-source designs, this project introduces several hardware enhancements.

## Power Management

A dedicated **ON/OFF switch** allows complete control of the shield power without unplugging the Arduino board.

Benefits:

- Easier testing
- Faster debugging
- Better user experience

---

## Safer microSD Interface

A **bidirectional logic level translator** was added between the Arduino (5V) and the microSD card (3.3V).

Benefits:

- Protects the SD card
- Improves compatibility
- Reliable SPI communication
- Safe voltage conversion

---

## Visual Status Indicators

Dedicated LEDs provide immediate visual feedback regarding board operation.

Useful for:

- Power verification
- Debugging
- Development

---

## PCB Layout Optimization

The PCB was completely redesigned instead of copying an existing layout.

Improvements include:

- Cleaner routing
- Better component placement
- Optimized SPI routing
- Improved CAN signal organization
- Large continuous ground pours
- Easier maintenance

---

## Manufacturing Ready

The board has been fully verified using Altium Designer DRC.

Included manufacturing outputs:

- Gerber Files
- NC Drill Files
- STEP Mechanical Model

Ready for fabrication using:

- JLCPCB
- PCBWay
- Seeed Fusion
- Aisler

---

# PCB Preview

## Top Layer

![PCB Top](Images/PCB_Top.png)

---

## Bottom Layer

![PCB Bottom](Images/PCB_Back.png)

---

## 3D View

![PCB 3D](Images/PCB_3D.png)

---

# Project Architecture

```
                       Arduino UNO
                            │
        ┌───────────────────┼────────────────────┐
        │                   │                    │
        ▼                   ▼                    ▼
   MCP2515 CAN         microSD Interface     Power Supply
   Controller          + Level Translator     + Switch
        │
        ▼
   TJA1050 CAN
   Transceiver
        │
        ▼
   CAN Bus Connector
```

---

# Repository Structure

```
CANCoreShield
│
├── Images
│   ├── PCB_3D.png
│   ├── PCB_Back.png
│   ├── PCB_Top.png
│
├── Manufacturing
│   └── CANCoreShield_Gerbers.zip
│
├── Schematics
│   ├── TOP_Sheet.SchDoc
│   ├── 01_Arduino_IO.SchDoc
│   ├── 02_CAN.SchDoc
│   ├── 03_SD_Card.SchDoc
│   └── 04_Power.SchDoc
│
├── CANCore Shield.PcbDoc
├── CANCore Shield.PrjPcb
├── CANCore Shield.OutJob
├── CANCore Shield 3D View.step
└── CANCore Shield.pdf
```

---

# Schematics

The hardware is divided into four functional hierarchical sheets:

| Sheet | Description |
|-------|-------------|
| 01 | Arduino Interface |
| 02 | CAN Communication |
| 03 | microSD Interface |
| 04 | Power Supply |

The complete PDF schematic is included in:

```
CANCore Shield.pdf
```

---

# PCB Design

Designed using **Altium Designer**.

Main design stages:

- Schematic Capture
- Component Placement
- Manual Routing
- Copper Pours
- 3D Verification
- Design Rule Check

Final Status

**0 DRC Errors**

---

# Manufacturing Files

Located in:

```
Manufacturing/
```

Included:

- Gerbers
- NC Drill
- Ready for fabrication

---

# 3D Model

A complete STEP model is provided for mechanical integration.

```
CANCore Shield 3D View.step
```

---

# Software

- Altium Designer
- CAMtastic
- Design Rule Check (DRC)

---

# Future Improvements

Possible future versions may include:

- CAN FD Support
- ESD Protection
- Reverse Polarity Protection
- Power Monitoring
- Additional Status LEDs
- Isolated CAN Interface

---

# Acknowledgments

This project was inspired by several open-hardware CAN shield designs, particularly the **Seeed Studio CAN-BUS Shield**, while introducing multiple hardware and PCB improvements tailored for educational and embedded system applications.

---

# Author

**Ayoub ELBOUHI**

Electrical Engineering & Embedded Systems Student

ENSA Marrakech

GitHub:

https://github.com/aelbouhi0131

---

If you found this project useful, consider giving it a ⭐ on GitHub.
