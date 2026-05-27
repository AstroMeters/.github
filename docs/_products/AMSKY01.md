---
title: AMSKY01
subtitle: Sky Quality, Cloud & Environment Sensor
description: 'Dual-sensor sky quality (SQM), cloud detection, and environmental sensor with USB-C and RS485 interfaces for observatories and automation.'
product_code: AMSKY01
keywords: 'AMSKY01, sky quality meter, SQM sensor, cloud detection, sky brightness measurement, environmental sensor, temperature humidity sensor, RS485 interface, USB-C sensor, observatory automation, light pollution monitoring, thermal IR sensor'
layout: product
hero_image: '/images/am_amsky_hero.png'
image: '/images/products/AMSKY01_bbq.jpg'
price: 378 EUR
features:
    - label: Dual SQM sensors – 10° and 60° field of view
      icon: fa-moon
    - label: 32×24 pixel IR cloud sensor (64×48 available)
      icon: fa-cloud
    - label: Water-pooling resistant sensor design
      icon: fa-tint-slash
    - label: Precision temperature & humidity sensor
      icon: fa-thermometer-half
    - label: Dual interface USB-C & RS485
      icon: fa-plug
    - label: ASCII protocol for easy integration
      icon: fa-terminal
    - label: Designed for autonomous observatories
      icon: fa-satellite-dish
buttons:
  - url: /docs/AMSKY01/
    text: Docs
    icon_class: fas fa-book
  - url: mailto:info@astrometers.eu?subject=AMSKY01%20offer%20request
    text: Get offer
    icon_class: fas fa-envelope
#shop_url: https://lectronz.com/products/amsky01
#shop_icon: https://lectronz-images.b-cdn.net/static/badges/buy-it-on-lectronz-medium.png
---

AMSKY01 is a professional sky quality sensor designed specifically for autonomous and remotely operated observatories. It is built around a **dual-sensor architecture** that combines two independent SQM channels with a pixel-array infrared cloud detector.

Unlike traditional single-point cloud detectors, AMSKY01 features a **32×24 pixel MLX9064x thermopile array** that provides detailed sky temperature mapping for precise cloud detection and sky clarity assessment. Combined with **two sky brightness sensors** (10° narrow-field and 60° wide-field, both outputting lux and mag/arcsec²) and SHT41 environmental sensor, it delivers comprehensive weather monitoring in a single compact unit. A high-resolution 64×48 pixel variant is also available for enhanced spatial analysis. The enclosure is engineered to prevent water pooling on the sensor surface.

With dual connectivity options (USB-C CDC serial and RS485) and an ASCII text-based protocol, AMSKY01 integrates seamlessly into observatory automation systems, SCADA networks, and custom monitoring solutions.


## Key Features

**Dual-Sensor Technology**
Two independent sky brightness (SQM) sensors with different fields of view — 10° narrow-angle for precise zenith measurement and 60° wide-angle for broader sky coverage — provide redundant and complementary light pollution data.

**Pixel Matrix Thermopile Array (MLX9064x)**
Advanced 32×24 pixel IR sensor (64×48 variant available) provides detailed sky temperature mapping for superior cloud detection compared to single-point sensors. Enables spatial analysis of cloud coverage and sky conditions.

**Optical Sky Brightness Measurement**
Both SQM channels deliver real-time readings in lux and mag/arcsec² for standardized sky quality assessment and light pollution monitoring.

**SHT41 Environmental Sensor**
Precision-calibrated temperature and humidity measurement for comprehensive meteorological data collection.

**Flexible Power & Connectivity**
USB-C (5V bus-powered) or external 8-13V DC supply. Dual interface: USB CDC serial for plug-and-play operation, or RS485 for industrial-grade long-distance communication.

**ASCII Text Protocol**
Simple, human-readable command structure enables rapid integration into existing automation systems without complex parsing libraries.

**Outdoor-Rated Design**
Weatherproof enclosure engineered for continuous 24/7 operation in permanent observatory installations. The sensor head geometry is specifically designed to prevent water pooling on optical surfaces.


## Cloud Detection in Action

The following video shows real-time data from the AMSKY01 sensor as cloud coverage develops overhead. The 32×24 pixel thermopile array captures detailed sky temperature distribution across its 150°×110° field of view, enabling precise detection of cloud movement and coverage patterns. Watch how the sensor responds to changing atmospheric conditions in real-time.

{% include youtube.html video="BXKVQVPBjso" time=26 %}

## Typical Applications

 * **Autonomous observatory control** – automated dome closure and equipment protection based on real-time cloud detection and weather conditions
 * **Sky quality monitoring networks** – standardized mag/arcsec² measurements for light pollution documentation and research
 * **Remote telescope operations** – reliable weather monitoring for unattended observing sessions
 * **SCADA/BMS integration** – RS485 connectivity for building automation and facility management systems
 * **Research and development** – detailed sky temperature mapping data for atmospheric and meteorological studies
