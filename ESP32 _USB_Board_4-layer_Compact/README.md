# ESP32 USB Development Board (4-Layer, Compact)

Compact ESP32 development board designed using a **4-layer PCB stackup** with a **breadboard-compatible form factor**, enabling easy prototyping while maintaining good power integrity and layout quality.

<img src="renders/esp32_usb_dev_4layer_compact_front.png" width="500">

---

# Overview

This board integrates:

- **ESP32-WROOM-32E module**
- **CP2102N USB-to-UART bridge**
- **3.3V LDO regulator**
- **Auto-program circuit**
- Breadboard-compatible expansion headers

The board is powered directly from **USB-C (5V)** and exposes common ESP32 interfaces including **SPI, I²C, ADC, and GPIO**.

This design focuses on a **compact, usable development board layout** while maintaining solid multi-layer design practices.

---

# Key Improvements (Compact Version)

- Breadboard-compatible header spacing (**700 mil row spacing**)
- Reduced board size and improved component density
- More efficient routing and placement
- Cleaner separation of functional blocks
- Improved usability for prototyping

---

# Electrical Specifications

Input voltage
5V via USB-C

Regulated voltage
3.3V

Programming interface
USB-UART bridge (CP2102N)

Auto-program support
Yes (DTR / RTS circuit)

Typical current capability
≈500 mA (Wi-Fi burst dependent)

---

# PCB Specifications

Layers
4

Board thickness
1.6 mm

Copper weight
1 oz

Form factor
Breadboard-compatible (2.54 mm pitch, 700 mil width)

---

# PCB Stackup

L1 – Components / Signals
L2 – Solid Ground Plane
L3 – 3.3V Power Plane
L4 – Signals / Ground Pour

This stackup provides:

- low impedance ground return paths
- stable power distribution
- reduced EMI
- efficient routing in a compact layout

---

# Main Components

ESP32 module
ESP32-WROOM-32E

USB-UART bridge
CP2102N

Voltage regulator
LDL212 3.3V LDO

Auto-program transistors
SS8050 (Q1, Q2)

USB ESD protection
USBLC6-2SC6

USB input fuse
Resettable fuse (0603)

---

# Features

- ESP32 Wi-Fi / Bluetooth module
- USB-C programming interface
- CP2102N USB-UART bridge
- 3.3V on-board LDO regulator
- Automatic programming circuit
- USB input protection (fuse + ESD)
- Breadboard-compatible headers
- SPI, I²C, ADC, and GPIO breakout
- Dedicated power and test points

---

# I/O Access

All ESP32 GPIOs are broken out through dual-row headers in a compact, breadboard-compatible layout.

Pins include access to:

- GPIO (digital I/O)
- ADC inputs
- SPI signals (VSPI)
- I²C signals
- Power rails (3V3, 5V, GND)

Silkscreen labels are provided on the PCB for easy identification.

---

# Power Architecture

Power enters through the **USB-C connector (5V)**.

Power path:

1. USB-C connector
2. Input fuse
3. ESD protection
4. LDL212 3.3V LDO regulator
5. Local decoupling network

The **Layer 3 (3.3V plane)** distributes power across the board.

The **Layer 2 ground plane** provides a continuous return path.

---

# Programming

Firmware is uploaded through the **CP2102N USB-UART bridge**.

Auto-program circuit:

- DTR → EN (reset)
- RTS → IO0 (boot mode)

Compatible with:

- ESP-IDF
- Arduino IDE
- PlatformIO

---

# Design Highlights

- Compact 4-layer PCB layout
- Breadboard-compatible form factor
- Internal ground plane for signal integrity
- Internal 3.3V plane for power distribution
- ESP32 antenna extends beyond board edge (no copper underneath)
- Controlled and short USB differential routing
- Clean functional block placement (USB → UART → MCU)
- Decoupling placed close to power pins
- Auto-program circuit located near ESP32

---

# Tools

Designed using:

KiCad PCB Design Suite

---

# Notes

The ESP32 antenna is positioned **outside the PCB edge**, eliminating copper underneath and improving RF performance.

The compact layout demonstrates:

- practical constraint-driven design
- efficient routing in limited space
- integration of usability (breadboard compatibility) with electrical performance

This project represents a **compact, practical ESP32 development board suitable for embedded prototyping and learning multi-layer PCB design**.
