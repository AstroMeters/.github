---
layout: page
title: AMSKY02 – Sky Quality and Cloud Sensor
subtitle: 'AMSKY02: Dual-sensor sky quality and cloud sensor'
description: 'AMSKY02 sky sensor documentation – setup, operation, and specifications. Dual sky brightness (SQM), cloud detection, temperature and humidity monitoring.'
keywords: 'AMSKY sensor, AMSKY01, AMSKY02, sky quality meter, cloud detection sensor, USB-C weather sensor, astronomical weather station, RS-485 sensor, SQM, sky monitoring, environmental sensor, observatory automation'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 2
hero_image: '/images/am_amsky_hero.jpg'
---

# AMSKY02 – Sky Quality and Cloud Sensor

The AMSKY02 is a compact, weatherproof sky sensor designed for astronomical and environmental applications. It combines multiple sensors in one unit:

- **Dual sky brightness sensors (SQM)** – 10° and 60° field of view, measuring sky brightness in mag/arcsec².
- **32×24 pixel infrared cloud sensor** – dual thermopile array for detailed sky temperature mapping (64×48 variant available).
- **Water-pooling resistant design** – sensor head geometry prevents water accumulation on optical surfaces.
- **Temperature and humidity sensor** – SHT41, monitors ambient air conditions.
- **USB-C and RS-485 interfaces** – for easy connection to PCs or automation systems.

<p align="center"><img width="400" alt="AMSKY02 sensor" src="/images/docs/AMSKY01/amsky02_product.png" /></p>

> **Note:** AMSKY02 is the successor to the original AMSKY01. Key improvements include dual SQM sensors (instead of a single one), a pair of IR thermopile arrays with redesigned mounting that doubles the resolution and field of view compared to AMSKY01, and an improved water-pooling resistant enclosure. Both models share the same software, protocol, and interfaces — the `amsky01` Python package and INDI driver work with both.

## Live Cloud Detection Example

The following video demonstrates real-time data from the AMSKY sensor as clouds pass through its field of view. The dual thermopile array with 32×24 pixel combined resolution provides detailed sky temperature mapping with 150°×110° field of view, allowing precise tracking of cloud coverage and movement patterns.

{% include youtube.html video="BXKVQVPBjso" time=26 %}


## How the Pixel Sensor Works

The infrared cloud sensor is based on a dual thermopile array with 32×24 pixel combined resolution (64×48 variant available), acting like a low-resolution thermal camera for the sky.

<p align="center">
  <img alt="AMSKY cloud visualization" src="/images/docs/AMSKY01/amsky_visualisation.jpg" width="100%">
  <p align="center" style="font-size:90%">
    Comparison of an optical image of the night sky with clouds from the AMASC01 allsky camera and the AMSKY thermopile pixel sensor.
    </p>
</p>

**Benefits of a pixel sensor:**

* **Spatial cloud detection:** See not only if clouds are present, but exactly where and how many.
* **Accurate sky background:** By averaging only the coldest pixels, the device can minimize the influence of warm objects (trees, chimneys, buildings) at the edge of the field of view.
* **Robust automation:** Algorithms can ignore local obstructions and focus on clear-sky regions, improving reliability for observatory control.
* **Real-time visualization:** Instantly visualize cloud structure and movement on the included GUI or in your own analysis scripts.


## Key Features

* Real-time **sky quality measurements** (SQM) to assess light pollution.
* Fast and reliable **cloud detection** using infrared sky temperature.
* Accurate **ambient temperature and humidity** monitoring.
* **USB-C (CDC Serial)** interface for plug-and-play operation with computers.
* **RS-485** interface for integration with observatory or building automation.
* **Open protocol** and API documentation for custom applications.
* Designed for **continuous outdoor use** in observatory conditions.


## Applications

- Light pollution monitoring.
- Automatic observatory control (e.g., dome closure during clouds).
- Weather condition logging for astronomical sites.
- Networked sky sensor systems and citizen science projects.
- Environmental data collection and automation.


## Technical Specifications

<table>
  <thead>
    <tr>
      <th>Parameter</th>
      <th>AMSKY01</th>
      <th>AMSKY02</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Cloud detection</strong></td>
      <td>Thermopile array 16×12 px<br>75°×110° FoV</td>
      <td>Dual thermopile array 32×24 px<br>150°×110° FoV<br><em>High-res variant: 64×48 px available</em></td>
    </tr>
    <tr>
      <td><strong>Sky brightness (SQM)</strong></td>
      <td>Single sensor (10° or 60° FoV, selectable)</td>
      <td>Dual sensor: 10° and 60° FoV<br>mag/arcsec²</td>
    </tr>
    <tr>
      <td><strong>Temperature</strong></td>
      <td>−15 °C to +50 °C</td>
      <td>−30 °C to +70 °C</td>
    </tr>
    <tr>
      <td><strong>Humidity</strong></td>
      <td colspan="2" style="text-align: center;">Relative humidity sensor</td>
    </tr>
    <tr>
      <td><strong>Interfaces</strong></td>
      <td colspan="2" style="text-align: center;">USB-C (CDC serial), RS-485</td>
    </tr>
    <tr>
      <td><strong>Power supply</strong></td>
      <td colspan="2" style="text-align: center;">USB bus power or external 8–13 V DC</td>
    </tr>
    <tr>
      <td><strong>Ingress protection</strong></td>
      <td colspan="2" style="text-align: center;">IP53W</td>
    </tr>
  </tbody>
</table>


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
