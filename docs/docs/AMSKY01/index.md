---
layout: page
title: AstroMeters documentation page
subtitle: 'AMSKY01: All-in-one sky quality and cloud sensor'
description: 'Complete AMSKY01 sensor documentation covering installation, operation, features, and technical specifications. Learn how to use this outdoor sky sensor with brightness, cloud detection, temperature, and humidity monitoring for astronomical and environmental observation. Compatible with USB-C and RS-485 interfaces.'
keywords: 'AMSKY01 sensor, sky quality meter, cloud detection sensor, USB-C weather sensor, astronomical weather station, RS-485 sensor, SQM, sky monitoring, environmental sensor, observatory automation'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 2
hero_image: '/images/docs.jpg'
---

# AMSKY01 – All-in-one Sky Quality and Cloud Sensor

The AMSKY01 is a compact, weatherproof sky sensor designed for astronomical and environmental applications. It combines multiple sensors in one unit:

- **Sky brightness sensor (SQM)** – measures sky brightness in mag/arcsec².
- **Infrared cloud sensor** – detects cloud presence by measuring sky temperature.
- **Temperature and humidity sensor** – monitors ambient air conditions.
- **USB-C and RS-485 interfaces** – for easy connection to PCs or automation systems.

<img width="600" alt="AMSKY01 sensor" src="https://github.com/user-attachments/assets/d425eac0-dab1-45b2-90b5-168619107dd3" />

## Live Cloud Detection Example

The following video demonstrates real-time data from the AMSKY01 sensor as clouds pass through its field of view. The 16×12 pixel thermopile array provides detailed sky temperature mapping with 110° field of view, allowing precise tracking of cloud coverage and movement patterns.

{% include youtube.html video="BXKVQVPBjso" time=26 %}


## Key Features

* Real-time **sky quality measurements** (SQM) to assess light pollution.
* Fast and reliable **cloud detection** using infrared sky temperature.
* Accurate **ambient temperature and humidity** monitoring.
* **USB-C (CDC Serial)** interface for plug-and-play operation with computers.
* **RS-485** interface for integration with observatory or building automation.
* **Open protocol** and API documentation for custom applications.
* Designed for **continuous outdoor use** in observatory conditions.

## How the Pixel Sensor Works: Detailed cloud Mapping

AMSKY01’s infrared cloud sensor is based on a 16×12 (optionally 32x24) pixel thermopile array, which acts like a low-resolution thermal camera for the sky. Each pixel measures the temperature in a specific direction, producing a real-time “thermal image” of the sky dome.


<p align="center">
  <img alt="AMFOC01 Top" src="/images/docs/AMSKY01/amsky_visualisation.jpg" width="100%">
  <p align="center" style="font-size:90%">
    Here is a comparison of an optical image of the night sky with clouds from the AMASC01 allsky camera and the AMSKY01 thermopile pixel sensor.
    </p>
</p>


**What are the benefits of a pixel sensor?**

* **Spatial cloud detection:** See not only if clouds are present, but exactly where and how many.
* **Accurate sky background:** By averaging only the coldest pixels, the device can minimize the influence of warm objects (trees, chimneys, buildings) at the edge of the field of view.
* **Robust automation:** Algorithms can ignore local obstructions and focus on clear-sky regions, improving reliability for observatory control.
* **Real-time visualization:** Instantly visualize cloud structure and movement on the included GUI or in your own analysis scripts.

The pixel array transforms AMSKY01 from a simple cloud sensor into a powerful tool for detailed, real-time monitoring and automation. This makes it ideal for demanding applications like robotic observatories or advanced weather research.
## Applications

- Light pollution monitoring.
- Automatic observatory control (e.g., dome closure during clouds).
- Weather condition logging for astronomical sites.
- Networked sky sensor systems and citizen science projects.
- Environmental data collection and automation.

## Technical Specifications

| Parameter               | Specification                              |
|-------------------------|---------------------------------------------|
| **Sky brightness (SQM)**| Measured in mag/arcsec²                     |
| **Cloud detection**     | Infrared sky temperature sensor             |
| **Temperature**         | High-accuracy ambient air temperature       |
| **Humidity**            | Relative humidity sensor                    |
| **Interfaces**          | USB-C (CDC serial), RS-485                  |
| **Power supply**        | USB bus power or external 8-12V  power      |
| **Operating temperature**| −20 °C to +60 °C (estimated)                |
| **Ingress protection**  | IP-rated outdoor enclosure (TBD)            |

## Interfaces

### USB-C (CDC Serial)

- Virtual serial port communication.
- Outputs real-time sensor data in ASCII or structured format.

### RS-485

- Industrial interface for robust long-distance communication.
- Suitable for integration into SCADA or observatory control systems.

### Communication Protocol

- Open protocol with documented commands and responses.
- Available API and example code for integration.
