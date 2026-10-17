---
layout: page
title: AMASC01 Software
subtitle: 'AMASC01: Software'
description: 'AMASC01 software documentation hub – overview of the software environment, base stack, and advanced capture modes.'
keywords: 'AMASC01 software, AMASC01 documentation, all-sky camera software, base software stack, circle buffer capture'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 4
hero_image: '/images/products/AMASC01/amasc01_hero.webp'
---

# AMASC01 Software

The AMASC01 camera is shipped **fully pre-installed and pre-configured**. All required software components, system settings, and operational parameters are prepared at the factory, allowing the camera to function immediately after installation.

<div class="notification is-info is-light">
  <strong>Default software since October 2026.</strong> AMASC01 cameras sold from October 2026 onwards are shipped with <a href="https://caelum.astrometers.eu">Caelum</a> as the default software.
</div>

This section groups the software-related documentation for the AMASC01 platform:

- [Caelum](/docs/AMASC01/caelum/) - primary software: open-source headless capture engine developed by AstroMeters, with sky-aware auto-exposure, keograms, meteor detection and remote archive upload ([caelum.astrometers.eu](https://caelum.astrometers.eu))
- [AllskyTeam/allsky stack](/docs/AMASC01/base-software-stack/) - default software for cameras sold before October 2026, with AstroMeters hardware integration
- [indi-allsky](/docs/AMASC01/indi-allsky/) - alternative software option with a different feature set and full camera compatibility
- [Circle Buffer Capture](/docs/AMASC01/circle-buffer-capture/) - high-frame-rate event-driven buffered capture workflow
- [Allsky Thermal Control](/docs/AMASC01/thermal-control/) - hardware-specific thermal management integrated into the AMASC01 software environment

## Software Scope

The current documentation is divided into:

- the primary operating software [Caelum](https://caelum.astrometers.eu)
- the AllskyTeam/allsky stack shipped with cameras sold before October 2026
- alternative all-sky software environments with a different workflow and feature set (indi-allsky)
- hardware-specific integration layers added by AstroMeters
- future or optional capture and processing modes

For thermal subsystem details, see the [Thermal Control documentation](/docs/AMASC01/thermal-control/).
