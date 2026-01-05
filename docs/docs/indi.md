---

layout: page
title: INDI Astrometers Drivers
subtitle: 'Drivers for AMSKY01 and AMFOC01 devices'
description: 'Installation and usage guide for INDI drivers developed by Astrometers. Covers AMSKY01 (sky quality & cloud sensor) and AMFOC01 (focuser) drivers with step-by-step instructions for building, installation, and operation with INDI/Ekos.'
keywords: 'INDI drivers, AMSKY01, AMFOC01, Astrometers, sky quality meter, cloud detection, focuser, KStars, Ekos, astronomy automation'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 3
hero_image: '/images/docs.jpg'
---

# INDI Astrometers Drivers

The **indi-astrometers** package provides two INDI drivers for Astrometers devices:

* **[AMSKY01](/products/AMSKY01)** – All-in-one sky quality and cloud sensor
* **[AMSKY01 - API](/products/AMSKY01)** - API interface of [AMSKY01-viwer](./../AMSKY01/viewer/) GUI app
* **[AMFOC01](/products/AMFOC01)** – Motorized focuser controller

Both drivers are distributed in the [indi-astrometers GitHub repository](https://github.com/roman-dvorak/indi-astrometers/).

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/roman-dvorak/indi-astrometers.git
cd indi-astrometers
```

### 2. Build the drivers

Make sure **CMake** and the **INDI Core library** are installed on your system.

```bash
mkdir build && cd build
cmake ..
make -j4
```

### 3. Install

```bash
sudo make install
sudo ldconfig
```

This will install both drivers (`indi_amsky01`, `indi_amfoc01`) into your system’s INDI driver path.

---

## Usage
The following examples show usage from the command line (CLI). It is also possible to use any INDI-compatible client, such as the graphical KStars/Ekos environment.

### AMSKY01 Driver

Run the driver manually:

```bash
indi_amsky01
```

Or start it via `indiserver`:

```bash
indiserver indi_amsky01
```

The driver communicates with the **AMSKY01 sensor** (via USB or RS-485).
It provides the following features:

* Sky brightness measurement (SQM equivalent)
* Cloud detection using thermopile sensor
* Ambient temperature and humidity monitoring
* Full compatibility with INDI clients (KStars/Ekos, etc.)

---

### AMFOC01 Driver

Run the driver manually:

```bash
indi_amfoc01
```

Or start it via `indiserver`:

```bash
indiserver indi_amfoc01
```

The driver supports the **AMFOC01 focuser** with features:

* Absolute/relative position control
* Stepper motor driver integration
* Temperature compensation
* Full compatibility with INDI/Ekos focusing tools

---

## Testing the installation

You can verify the installation by listing drivers:

```bash
indiserver -v indi_amsky01 indi_amfoc01
```

Connect your devices, then open **KStars/Ekos**, add the drivers, and check communication in the INDI Control Panel.

---

## Repository & Issues

For source code, updates, and bug reports:
[indi-astrometers GitHub repository](https://github.com/roman-dvorak/indi-astrometers/)


