---
title: AMASCHR01
subtitle: Heater ring with integrated temperature sensor
description: 'AMASCHR01 – heater ring with integrated temperature sensor optimized for Raspberry Pi HQ camera. Simplifies wiring inside AllSky camera domes.'
product_code: AMASCHR01
keywords: 'AMASCHR01, AMASC01, heater ring, dome heater, dew heater, SHT4x, temperature sensor, Raspberry Pi HQ camera, allsky camera accessory, anti-fog, condensation prevention, PCB heater'
layout: product
image: ''
hero_image: '/images/am_products_hero.jpg'
price:
features:
    - label: SHT4x temperature & humidity sensor
      icon: fa-thermometer-half
    - label: Heating element integrated in PCB design
      icon: fa-fire
    - label: Optimized for Raspberry Pi HQ camera
      icon: fa-microchip
    - label: Short cable connections — no complex wiring
      icon: fa-plug
---

# AMASCHR01 – Heater Ring with Sensor

The **AMASCHR01** is a heater ring with an integrated **SHT4x** temperature and humidity sensor for precise closed-loop heating control, keeping the optical dome clear during cold and humid nights.

Optimized for use with **Raspberry Pi HQ cameras**, its design allows short, direct cable connections between the heater, sensor, and camera board — eliminating the need for complex wiring back to the Raspberry Pi.


## Key Features

* **SHT4x Temperature & Humidity Sensor:** Precision-calibrated sensor enables accurate dome monitoring and automatic heating regulation.
* **PCB-Integrated Heating Element:** The heater is part of the board design — no soldered resistors, resulting in even heat distribution and improved reliability.
* **Air Circulation Holes:** Board cutouts allow airflow around the camera module, helping maintain stable internal conditions.
* **Optimized for Raspberry Pi HQ Camera:** Designed to sit directly around the camera module, enabling smart and compact cable routing.
* **Simplified Wiring:** Short cable connections replace complex long-distance wiring to the Raspberry Pi, improving reliability and simplifying assembly.


## Specifications

### Sensor (SHT4x)

* **Supply voltage:** 3.3 V
* **Interface:** I²C
* **Connection:** Soldering tabs

> **Note:** Although the SHT4x is a temperature and humidity sensor, it is mounted directly on the heated surface. Therefore, it measures the **surface temperature of the heater ring**, not the ambient air temperature inside the dome. This is by design — it enables accurate closed-loop control of the heater output.

### Heating Element

* **Maximum supply voltage:** 12 V (with PWM/PID control), 5 V for permanent/continuous unregulated power
* **Resistance:** ~5.8 Ω
* **Maximum power at 12 V:** ~25 W
* **Power at 5 V:** ~4.3 W
* **Heating capability:** Up to ~40 °C surface temperature at full power (25 W), which is excessive for normal operation. **Recommended operating temperature is around 15 °C.**

### Recommended Control

Optimal heating control is achieved using **PWM with a PID controller**, using feedback from the on-board SHT4x sensor. This ensures stable, efficient dome heating without overshooting.

The heater ring itself does not contain any control logic. It requires a **host system** (e.g. Raspberry Pi) running the heating control software with the PID regulator. The host system reads the SHT4x sensor data and drives the heater via PWM output accordingly.


## Installation

<!-- TODO: Add installation instructions and photos -->


## Compatibility

Compatible with **Raspberry Pi HQ camera** modules and the [AMASC01 AllSky Camera](/products/AMASC01/).
