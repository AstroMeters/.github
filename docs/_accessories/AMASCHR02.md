---
title: AMASCHR02
subtitle: Autonomous AllSky Camera Heating Ring
description: 'AMASCHR02 autonomous heating ring for all-sky camera domes with built-in PID regulation and selectable target temperature.'
product_code: AMASCHR02
keywords: 'AMASCHR02, allsky camera heating ring, autonomous dew heater, dome heater, Raspberry Pi camera heater, anti-condensation heater, PID heater ring, telescope camera accessory'
layout: product
image: '/images/docs/AMASCHR02/AMASCHR02-image.jpg'
hero_image: '/images/am_products_hero.jpg'
price: 83 Eur
features:
    - label: Autonomous PID-controlled heating
      icon: fa-fire
    - label: Selectable 5-40 C target temperature
      icon: fa-thermometer-half
    - label: 8-14 V low-voltage power input
      icon: fa-plug
    - label: Compact direct camera-module mounting
      icon: fa-camera
buttons:
  - url: /docs/components/AMASCHR02/
    text: Docs
    icon_class: fas fa-book
  - url: mailto:info@astrometers.eu?subject=AMASCHR02%20offer%20request
    text: Get offer
    icon_class: fas fa-envelope
---

# AMASCHR02 - Autonomous AllSky Camera Heating Ring

The **AMASCHR02** is a compact heating ring for all-sky camera domes. It is designed to mount directly around the camera module, keeping the heater close to the optical dome surface where dew and condensation need to be prevented.

Unlike a simple passive heater, AMASCHR02 includes its own temperature sensing and regulation electronics. The ring can be powered continuously from a low-voltage supply and regulates its heating output automatically, without software setup or an external controller.

<figure style="text-align: center;">
  <img src="/images/docs/AMASCHR02/AMASCHR02-image.jpg" alt="AMASCHR02 autonomous heating ring for all-sky cameras" title="AMASCHR02 autonomous heating ring">
  <figcaption>AMASCHR02 autonomous heater for all-sky camera domes.</figcaption>
</figure>

## Key Features

* **Autonomous operation:** Built-in control electronics regulate the heater output automatically during normal operation.
* **PID temperature control:** The ring measures its own surface temperature and adjusts heating power to maintain the selected target.
* **Configurable setpoint:** Three solder jumpers select target temperatures from 5 C to 40 C. The factory default is 20 C.
* **Simple power input:** Operates from an 8-14 V supply with a maximum heating power of 4 W.
* **Camera-module mounting:** The mechanical layout is optimized for compact all-sky camera assemblies and Raspberry Pi camera modules.

## Power and Control

AMASCHR02 is intended to stay powered during operation. When the dome or camera assembly is already warm, the controller reduces or stops heating automatically. In colder conditions, it increases the heater output up to the available 4 W maximum.

No host software, PWM output, or custom control loop is required. The only external requirement is a correctly polarized low-voltage power supply.

## Typical Applications

* DIY all-sky cameras
* Anti-dew heating for small optical domes
* Raspberry Pi camera based sky monitoring systems
* Compact observatory and weather-camera builds

## Specifications

* **Supply voltage:** 8-14 V DC
* **Maximum heating power:** 4 W
* **Temperature presets:** 5 C, 10 C, 15 C, 20 C, 25 C, 30 C, 35 C, 40 C
* **Default preset:** 20 C
* **Power connector:** 2-pin 2.54 mm header
* **Inner diameter:** 36 mm
* **Outer diameter:** 70 mm
* **Mounting holes:** 30 x 30 mm square pattern

## Documentation

Detailed configuration, jumper settings, compatibility notes, and operating guidance are available in the [AMASCHR02 documentation](/docs/components/AMASCHR02/).
