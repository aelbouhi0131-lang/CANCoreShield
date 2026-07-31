# CANCore Shield

![Altium Designer](https://img.shields.io/badge/Altium-Designer-A5915F?style=for-the-badge)
![PCB](https://img.shields.io/badge/PCB-2_Layers-success?style=for-the-badge)
![DRC](https://img.shields.io/badge/DRC-0_Errors-brightgreen?style=for-the-badge)
![Gerbers](https://img.shields.io/badge/Gerbers-Ready-blue?style=for-the-badge)
![License](https://img.shields.io/badge/Open_Hardware-Project-orange?style=for-the-badge)

---

# Overview

**CANCore Shield** is a professional two-layer Arduino UNO CAN-Bus Shield designed in **Altium Designer** for embedded systems, industrial automation, robotics and automotive communication.

The project was inspired by well-known open hardware CAN shields such as the **Seeed Studio CAN-BUS Shield**, while introducing several hardware improvements focused on reliability, protection, debugging, thermal performance and manufacturability.

The repository contains everything required to understand, reproduce and manufacture the board.

---

# Project Features

- Arduino UNO Shield Compatible
- MCP2515 CAN Controller
- MCP2562 Automotive CAN Transceiver
- microSD Card Interface
- Grove UART Connector
- Grove I²C Connector
- Configurable 120Ω CAN Termination
- Advanced Power Protection
- Logic Level Translation
- Hardware Debug LEDs
- Optimized Ground Planes
- Thermal Management
- Complete 3D Model
- Manufacturing Ready Gerbers
- DRC Verified (0 Errors)

---

# Design Improvements

Unlike conventional Arduino CAN-Bus shields available online, this design introduces several hardware enhancements intended to improve robustness, safety and usability.

## Advanced Power Protection

One of the largest improvements in this project is the complete redesign of the power stage.

Instead of using only a voltage regulator, the board integrates a professional protection front-end including:

- TPS26620 eFuse
- SI7465 External MOSFET
- Over-Voltage Protection (OVP)
- Under-Voltage Protection (UVLO)
- Current Limiting
- TVS Protection
- Zener Protection
- Ferrite Bead Filtering
- Power Filtering Capacitors

This greatly increases board reliability and protects both the Arduino and external peripherals against electrical faults.

---

## Improved microSD Interface

A dedicated **SN74LVC125A** logic level translator was added between the Arduino (5V) and the microSD card (3.3V).

Benefits:

- Safe voltage translation
- Improved communication reliability
- Protects the SD card from direct 5V signals
- Better compatibility with high-speed SPI communication

---

## Modern Automotive CAN Transceiver

Instead of the older **MCP2551** commonly found on legacy shields, this project uses:

**Microchip MCP2562**

Advantages:

- Automotive qualified
- Improved EMC performance
- Lower power consumption
- Higher robustness

---

## Extended Hardware Debugging

Additional hardware status LEDs were integrated for easier debugging.

The board provides visual indication for:

- Power Status
- UART TX
- UART RX
- CAN TX
- CAN RX
- CAN Interrupt Activity

These indicators simplify debugging without requiring external measurement equipment.

---

## Configurable CAN Bus Termination

The shield includes a selectable **120 Ω termination resistor** using a jumper.

This allows the board to be configured as:

- End node
- Intermediate node

making it suitable for various CAN network topologies.

---

## Improved Connectivity

Additional expansion connectors were integrated:

- Grove UART
- Grove I²C

These connectors simplify sensor integration and rapid prototyping.

---

## PCB Layout Optimization

Special attention was given to PCB layout quality.

Improvements include:

- Optimized component placement
- Reduced routing complexity
- Large GND copper pours
- Better return current paths
- Improved signal integrity
- Reduced electrical noise

---

## Thermal Optimization

To improve heat dissipation, thermal optimization techniques were implemented:

- Thermal vias around power devices
- Improved copper distribution
- Better heat spreading through ground planes

This helps maintain lower operating temperatures during extended operation.

---

## Manufacturing Optimization

The PCB has been completely verified before release.

Final verification includes:

- Design Rule Check (DRC)
- Copper Pour Verification
- 3D Mechanical Verification
- Gerber Generation
- NC Drill Generation

Final Status:

**0 DRC Errors**

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

# Repository Structure

```
CANCoreShield
│
├── Images
│   ├── PCB_3D.png
│   ├── PCB_Back.png
│   ├── PCB_Top.png
│   └── README.md
│
├── Manufacturing
│   ├── CANCoreShield_Gerbers.zip
│   └── .gitkeep
│
├── Schematics
│   ├── TOP_Sheet.SchDoc
│   ├── 01_Arduino_IO.SchDoc
│   ├── 02_CAN.SchDoc
│   ├── 03_SD_Card.SchDoc
│   ├── 04_Power.SchDoc
│   └── README.md
│
├── CANCore Shield 3D View.step
├── CANCore Shield.OutJob
├── CANCore Shield.PcbDoc
├── CANCore Shield.PrjPcb
└── CANCore Shield.pdf
```

---

# Schematics

The project schematic is organized into four functional blocks:

### 01 — Arduino I/O

Contains:

- Arduino UNO interface
- SPI connections
- UART interface
- I²C interface
- Expansion headers

---

### 02 — CAN Communication

Contains:

- MCP2515 CAN Controller
- MCP2562 CAN Transceiver
- CAN Bus Protection
- CAN Termination Network
- DB9 Connector
- Screw Terminal

---

### 03 — microSD Card

Contains:

- microSD Socket
- SN74LVC125A Logic Level Translator
- SPI Routing
- Filtering Components

---

### 04 — Power Supply

Contains:

- TPS26620 eFuse
- SI7465 MOSFET
- Protection Circuit
- Voltage Regulation
- Filtering Network
- Power Switch

All source schematic files are available inside:

```
Schematics/
```

---

# PCB Design

Designed using **Altium Designer**.

Main design stages:

- Schematic Capture
- Component Placement
- Interactive Routing
- Copper Pour
- Thermal Optimization
- 3D Mechanical Verification
- DRC Verification

Final DRC Result:

✅ **0 Errors**

---

# Manufacturing

Fabrication files are available inside:

```
Manufacturing/
```

Included:

- Gerber Files
- NC Drill Files

Compatible with manufacturers such as:

- JLCPCB
- PCBWay
- Seeed Fusion
- ALLPCB

---

# 3D Model

A complete STEP model is provided for mechanical integration.

```
CANCore Shield 3D View.step
```

Compatible with:

- SolidWorks
- Fusion 360
- FreeCAD
- Inventor

---

# Documentation

The complete project documentation is available in:

```
CANCore Shield.pdf
```

The document includes:

- Complete Schematics
- PCB Layout
- Component Placement
- Design Overview

---

# Software Used

- Altium Designer
- CAMtastic
- Design Rule Check (DRC)

---

# Future Improvements

Potential future enhancements include:

- CAN FD Support
- USB-C Power Input
- Reverse Polarity Protection
- Automotive Diagnostic Connector
- Isolated CAN Interface
- On-board Power Monitoring

---

# Author

**Ayoub ELBOUHI**

Electrical Engineering & Embedded Systems Student

ENSA Marrakech

GitHub:

https://github.com/aelbouhi0131

---

If you found this project useful, consider giving the repository a ⭐.
