# <div align="center">🚀 **OmniRange C5**

### Multifunction Wireless Platform for Flipper Zero & Standalone Operation

</div>
<div align="center">

📡 **Wi-Fi (2.4G + 5G)** • 📶 **Sub-GHz 433 MHz** • 🛰 **GPS** • 🔋 **800mAh Battery** • 🖥 **2.8" Display**

**Dual-Mode — Standalone Wireless Toolkit + Flipper Zero Expansion Module**

---

[](#)

[](#)  

</div>

---

# 📘 **Table of Contents**

- 1. Introduction

- 2. Features

- 3. Operating Modes
  - 3.1 Standalone Mode
  
  - 3.2 Flipper Zero Expansion Mode

- 4. Hardware Overview

- 5. Flipper Zero Configuration
  - GPS
  
  - 433mhz-sub-ghz
  
  - wifi-esp32-c5

- 6. Flashing Firmware

- 7. Enclosure / STL Files

- 8. Screenshots

- 9. License

---

# 1. **Introduction**

**OmniRange C5** is a next-generation multifunction wireless platform designed for:

- Wireless security research

- RF protocol analysis

- Field engineering

- Signal scanning & geolocation

- IoT device testing

- Flipper Zero wireless expansion

It operates in **two modes**:

1. **Standalone Mode** (runs ESP32 Marauder natively)

2. **Flipper Zero Expansion Mode** (adds Wi-Fi + Sub-GHz + GPS capabilities)

---

# 2. **Features**

### 🔹 Dual-Mode Wireless Platform

- Standalone toolkit or Flipper Zero expansion board

### 🔹 Multiple Radio Technologies

- **Wi-Fi (2.4 GHz + 5 GHz)** via ESP32-C5

- **Sub-GHz 433 MHz** (CC1101)

- **Built-in GPS** (UBlox / ATGM)

### 🔹 Portable Design

- 2.8-inch LCD

- 800 mAh rechargeable battery

- USB-C interface

### 🔹 Native Software Support

- Runs **ESP32 Marauder** out-of-the-box

- Compatible with Momentum Flipper Zero firmware

- Supports external RF modules

---

# 3. **Operating Modes**

---

## 3.1 **Standalone Mode**

The OmniRange C5 includes:

- **ESP32-S2 main MCU**

- **2.8" color LCD**

- **800 mAh battery**

Runs **ESP32 Marauder** natively with full scanning/testing features.

🔗 ESP32 Marauder releases:  
https://github.com/justcallmekoko/ESP32Marauder/releases

---

## 3.2 **Flipper Zero Expansion Mode**

When connected to a Flipper Zero, the C5 unlocks:

- **Dual-band Wi-Fi (2.4G + 5G)**

- **433 MHz Sub-GHz Radio**

- **GPS positioning**

- **Extended scanning & capture tools**

Perfect for:

- Packet capture

- WiFi attacks & testing

- RF protocol experiments

- Geolocation tools

- Custom firmware development

---

# 4. **Hardware Overview**

| Component            | Description                      |
| -------------------- | -------------------------------- |
| **ESP32-S2**         | Standalone controller (Marauder) |
| **ESP32-C5**         | Dual-band Wi-Fi for Flipper      |
| **CC1101**           | 433 MHz Sub-GHz module           |
| **GPS (UBlox/ATGM)** | Positioning                      |
| **2.8" LCD**         | Onboard display                  |
| **800 mAh Li-ion**   | Internal battery                 |
| **USB-C Port**       | Charging & firmware              |

---

# 5. **Flipper Zero Configuration**

> Tested on Momentum firmware **MNTM-011 (02-02-2025)**  
> Other versions may vary slightly.

---

## **Open Menu**

`Momentum → Protocol Settings → GPIO Pin Mapping`

---

## GPS Mapping

`GPS TX → GPIO 13 GPS RX → GPIO 14`

---

## 433 MHz Sub-GHz Mapping

- Default CC1101 (4-wire SPI)

- No change required

If using **external Sub-GHz module**:

<details>
<summary>Expand steps</summary>

1. Insert external 433 MHz module

2. Open **Sub-GHz** menu

3. Enter **Advanced Settings**

4. Set: **Use Module → External**

</details>

---

## Dual-Band Wi-Fi (ESP32-C5) Mapping

`ESP32 TX → GPIO 15 ESP32 RX → GPIO 16`

---

# 6. **Flashing Firmware**

### For ESP32-S2 (Standalone Marauder)

`esptool.py write_flash 0x0 firmware.bin`

### For ESP32-C5 (Wi-Fi Module)

Same procedure as ESP32-S3 devices.  
(Upload your dedicated .bin in `/firmware/` folder)

---

# 7. **Enclosure / STL Files**

3D-printable open-source enclosure files (STL) will be provided in:

`/enclosure/`

---

# 8. **Screenshots**

*(Add your product photos here)*

`/images/   product_front.jpg   product_back.jpg   ui_marauder.jpg   flipper_menu.jpg`

---

# 9. **License**

This project is released under the **MIT License**.  
You are free to modify, distribute, and use it for personal or commercial purposes.
