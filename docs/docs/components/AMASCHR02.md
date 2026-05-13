---
layout: page
title: AMASCHR02 AllSky Camera Heating Ring
subtitle: 'AMASCHR02: AstroMeters AllSky Camera Heating Ring'
description: 'AMASCHR02 autonomous heating ring for all-sky cameras, optimized for Raspberry Pi camera modules and direct module mounting.'
keywords: 'AMASCHR02, allsky camera heating ring, dew heater, Raspberry Pi camera module, autonomous heater ring'
menubar: docs_menu
show_sidebar: false
toc: false
hero_image: '/images/am_products_hero.jpg'
---

## AMASCHR02 Heating Ring

The AMASCHR02 is an AstroMeters AllSky camera heating ring designed for all-sky cameras and optimized for use with Raspberry Pi camera modules.

Its mechanical concept allows the ring to be mounted directly on the camera module, which simplifies integration and keeps the heating system compact and close to the glass dome that needs protection against condensation.

<figure style="text-align: center;">
  <img src="/images/docs/AMASCHR02/AMASCHR02-image.jpg" alt="AMASCHR02 autonomous heating ring for all-sky cameras" title="AMASCHR02 Heating Ring – autonomous heater for all-sky camera domes">
  <figcaption>AMASCHR02 Heating Ring – autonomous heater for all-sky camera domes</figcaption>
</figure>

## Autonomous Operation

The AMASCHR02 is designed as an autonomous heater ring, which means it does not require any software configuration during normal use. Thanks to the built-in auto-regulation, the heating ring is expected to be powered continuously (8–14 V recommended) throughout its entire operation.

The on-board control circuit uses a **PID controller** to regulate the **surface temperature** of the heating ring. The controller continuously measures the actual surface temperature and adjusts the heater output accordingly. This means the ring automatically adapts to changing conditions — for example, when the sun is warming the dome during the day, the heater reduces its output or turns off entirely. There is no need for any external software control loop.

On power-up, the on-board LED blinks twice to indicate successful initialization, then remains off for the rest of operation.

Controlled heating is important because it avoids unnecessary overheating of the camera assembly. Excess heating can increase the camera sensor's readout noise, which is undesirable for low-light imaging. At the same time, maintaining only the required temperature helps reduce unnecessary power consumption.

## Configuration

On the bottom side of the ring there are three solder jumpers (**J1**, **J2**, **J3**) used to select the target surface temperature. The jumpers form a 3-bit binary value that maps to a temperature preset:

<table style="margin: 0 auto; text-align: center;">
  <thead>
    <tr><th>J3</th><th>J2</th><th>J1</th><th>Value</th><th>Temperature</th></tr>
  </thead>
  <tbody>
    <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>5 °C</td></tr>
    <tr><td>0</td><td>0</td><td>1</td><td>1</td><td>10 °C</td></tr>
    <tr><td>0</td><td>1</td><td>0</td><td>2</td><td>15 °C</td></tr>
    <tr style="font-weight: bold;"><td>0</td><td>1</td><td>1</td><td>3</td><td>20 °C</td></tr>
    <tr><td>1</td><td>0</td><td>0</td><td>4</td><td>25 °C</td></tr>
    <tr><td>1</td><td>0</td><td>1</td><td>5</td><td>30 °C</td></tr>
    <tr><td>1</td><td>1</td><td>0</td><td>6</td><td>35 °C</td></tr>
    <tr><td>1</td><td>1</td><td>1</td><td>7</td><td>40 °C</td></tr>
  </tbody>
</table>

To set a jumper to **1**, bridge the corresponding solder pads. An open (unbridged) jumper represents **0**. The target temperature can be changed at any time by soldering or desoldering the jumper pads.

The default factory configuration is set to **20 °C** (J1 = 1, J2 = 1, J3 = 0), which has been identified as the optimal temperature for most use cases.

## Power Requirements

The heater ring requires only a simple external power supply:

- Supply voltage: 8–14 V
- Maximum heating power: **4 W**
- Power connector: 2-pin 2.54 mm header

> **Warning:** Pay attention to the correct polarity when connecting the power supply.

The 4 W maximum output is sufficient for normal anti-condensation operation. During cold nights or extreme weather, the ring may not reach the configured target temperature — this is expected and by design. In such conditions, the heater simply operates at its maximum power output, providing as much heating as possible. This is still sufficient to prevent condensation on the dome surface.

No separate software control loop is required for standard use.

## Intended Use

The AMASCHR02 is intended for applications where the user wants:

- compact heater integration directly at the camera module
- protection against dew and condensation on all-sky camera optics
- straightforward deployment without custom software setup
- stable operation with simple low-voltage power input
- DIY allsky camera setups

## Dimensions

- Inner diameter: 36 mm
- Outer diameter: 70 mm
- Mounting holes: 30 × 30 mm square pattern
- Drawing: *TBD / available on request*

## Comparison with AMASCHR01

Unlike the [AMASCHR01](/accessories/AMASCHR01/), which relies on external heating control provided by the host computer (e.g. in the [AMASC01](/products/AMASC01/) camera, where the heater is driven by the Raspberry Pi software), the AMASCHR02 is a fully autonomous solution. It contains its own temperature sensor and PID controller on-board, making it completely independent of any host system or control software.

## Schematic

*TBD*

## Compatibility

The design is optimized primarily for Raspberry Pi camera modules, especially where direct mounting to the camera assembly is preferred.

This compatibility statement refers primarily to mechanical compatibility such as overall dimensions and mounting hole positions.

It has also been verified that the ring is mechanically compatible with other camera modules sharing similar geometry and mounting patterns.

If you need custom dimensions (e.g. a different inner or outer disc diameter), please [contact us](/about/) to discuss your requirements.
