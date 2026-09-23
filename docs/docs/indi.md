---

layout: page
title: INDI Drivers
subtitle: 'Drivers for AMSKY and AMFOC01 devices'
description: 'Installation and usage guide for AstroMeters INDI drivers – AMSKY01/AMSKY02 sky sensors and AMFOC01 focuser integration with KStars/Ekos.'
keywords: 'INDI drivers, AMSKY01, AMSKY02, AMFOC01, Astrometers, sky quality meter, cloud detection, focuser, KStars, Ekos, astronomy automation'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 3
hero_image: '/images/docs.webp'
---
The **indi-astrometers** package provides three INDI drivers for AstroMeters devices:

* **[AMSKY](/products/AMSKY02/)** (`indi_amsky01`) – Sky quality and cloud sensor (AMSKY01 / AMSKY02), direct serial connection
* **AMSKY Viewer API** (`indi_amsky01_api`) – HTTP API client of the [AMSKY Viewer](/docs/AMSKY/viewer/) GUI app
* **[AMFOC01](/products/AMFOC01/)** (`indi_amfoc01`) – Motorized focuser controller

All drivers are distributed in the [indi-astrometers GitHub repository](https://github.com/AstroMeters/indi-astrometers/).

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/AstroMeters/indi-astrometers.git
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

This will install all drivers (`indi_amsky01`, `indi_amsky01_api`, `indi_amfoc01`) into your system’s INDI driver path.

---

## Usage
The following examples show usage from the command line (CLI). It is also possible to use any INDI-compatible client, such as the graphical KStars/Ekos environment.

### AMSKY Driver

Run the driver manually:

```bash
indi_amsky01
```

Or start it via `indiserver`:

```bash
indiserver indi_amsky01
```

The driver communicates with the **AMSKY02** (or legacy **AMSKY01**) sensor via USB or RS-485. The driver name `indi_amsky01` is kept for compatibility and works with both sensor generations.
It provides the following features:

* Sky brightness measurement (SQM equivalent)
* Cloud detection using thermopile sensor
* Ambient temperature and humidity monitoring
* Full compatibility with INDI clients (KStars/Ekos, etc.)

### AMSKY Viewer API Driver

```bash
indiserver indi_amsky01_api
```

Instead of opening the serial port itself, this driver reads data from the HTTP API of the running [AMSKY Viewer](/docs/AMSKY/viewer/) application (by default `http://localhost:8080/data.json`, configurable). This lets the viewer GUI and INDI clients use the sensor at the same time.

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
[indi-astrometers GitHub repository](https://github.com/AstroMeters/indi-astrometers/)


