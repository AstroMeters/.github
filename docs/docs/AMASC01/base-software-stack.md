---
layout: page
title: AMASC01 AllskyTeam/allsky Stack
subtitle: 'AMASC01: AllskyTeam/allsky Stack'
description: 'AMASC01 base software stack documentation – pre-installed Allsky software, web interface, imaging pipeline, and hardware management integration.'
keywords: 'AMASC01 software, AllskyTeam allsky, all-sky camera software, web interface, imaging pipeline, dome heating control, ventilation control'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 4
hero_image: '/images/products/AMASC01/amasc01_hero.webp'
---

# AMASC01 AllskyTeam/allsky Stack

<div class="notification is-info is-light">
  <strong>Default software since October 2026 is <a href="/docs/AMASC01/caelum/">Caelum</a>.</strong> This page describes the AllskyTeam/allsky stack shipped with AMASC01 cameras sold before October 2026.
</div>

AMASC01 cameras sold before October 2026 are delivered with this software environment already installed and configured at the factory. This allows the system to start operating immediately after installation, without requiring manual software setup for standard use.

## Software Foundation

The included software is based on the open-source project:  
**AllskyTeam/allsky**: <https://github.com/AllskyTeam/allsky>

This provides the core imaging, automation, and user interface framework used by the camera during regular operation.

## AstroMeters Integration

In addition to the upstream base software, AMASC01 includes pre-configured settings and **hardware management tools** for controlling camera-specific components such as dome heating, ventilation, and anti-dew systems.

Proper hardware control is essential for reliable long-term outdoor operation and stable image quality. For details about the thermal subsystem, see the [Thermal Control documentation](/docs/AMASC01/thermal-control/).

## Other Software Options

The primary AMASC01 software is [Caelum](/docs/AMASC01/caelum/), the open-source capture engine developed by AstroMeters (documentation at [caelum.astrometers.eu](https://caelum.astrometers.eu)). AMASC01 can also run [indi-allsky](/docs/AMASC01/indi-allsky/).

## Included Capabilities

- **Web-based user interface** for configuration and monitoring
- **Exposure and imaging parameter control**
- **Image masking capabilities** for excluding unwanted areas
- **Data processing pipeline** with numerical operations
- **Modular and customizable architecture**
- **Image archiving and timelapse generation**
- **Overlay support** for metadata display
- **Hardware management interface** for dome heating, ventilation control, and environmental monitoring

## Operation Summary

For normal deployment, the user typically only needs to:

1. **Connect** the camera via Ethernet/PoE cable
2. **Access** the web interface using the assigned IP address or hostname
3. **Adjust** imaging parameters if needed
4. **Begin** regular image capture

No complex software modifications or manual system configuration steps are required for standard operation.
