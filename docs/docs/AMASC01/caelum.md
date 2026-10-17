---
layout: page
title: Caelum
subtitle: 'All-sky capture software'
description: 'Caelum – the default AMASC01 software. Open-source headless capture engine for all-sky cameras developed by AstroMeters, with sky-aware auto-exposure, keograms, meteor detection and remote archive upload.'
keywords: 'Caelum, AMASC01 software, all-sky camera software, allsky capture engine, Raspberry Pi allsky, sky-aware auto-exposure, keogram, meteor detection, FITS, DNG'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 5
hero_image: '/images/products/AMASC01/amasc01_hero.webp'
---

# Caelum

**Caelum** is an open-source, headless capture engine for all-sky cameras developed by AstroMeters. It is the **primary software** of the [AMASC01](/products/AMASC01/) camera, designed for long-term unattended operation and scientific data collection.

<div class="notification is-info is-light">
  <strong>Default software since October 2026.</strong> AMASC01 cameras sold from October 2026 onwards are shipped with Caelum pre-installed and pre-configured. Cameras sold earlier run the <a href="/docs/AMASC01/base-software-stack/">AllskyTeam/allsky stack</a> and can be switched to Caelum on request – <a href="/about/#custom-development-and-contact">contact us</a> if you need help.
</div>

- Documentation: <https://caelum.astrometers.eu>
- Getting started: <https://caelum.astrometers.eu/guide/getting-started>
- Source code: <https://github.com/roman-dvorak/caelum>

## Key Features

- **Sky-aware auto-exposure** – Sun and Moon positions are computed from an offline ephemeris, and separate exposure and gain presets are used for day, civil, nautical and astronomical twilight, and night. See [exposure control](https://caelum.astrometers.eu/guide/exposure).
- **RAM-first image pipeline** – frames are calibrated, measured and thumbnailed in memory; only what is worth keeping is written to disk, including raw FITS and DNG files with metadata.
- **Keograms and meteor detection** – built-in plugins assemble a daily keogram and detect meteor streaks; third-party plugins use the same interface. See [plugins](https://caelum.astrometers.eu/guide/plugins).
- **Storage and remote archive** – a rotating local cache with a retention policy and a self-healing rsync upload to a permanent remote archive, viewable as a static multi-camera gallery. See [storage](https://caelum.astrometers.eu/guide/storage) and [upload](https://caelum.astrometers.eu/guide/upload).
- **Web UI** – live view, recordings by night, file browser, settings, live logs and a web terminal, with admin and viewer accounts. See [web UI](https://caelum.astrometers.eu/guide/web-ui).
- **Updates from the browser** – releases are installed and rolled back from the web UI. See [updates](https://caelum.astrometers.eu/guide/updates).

## Operation

1. **Connect** the camera via Ethernet/PoE cable
2. **Open** the Caelum web interface using the camera's IP address or hostname
3. **Adjust** capture, storage and upload settings if needed
4. **Let it run** – Caelum operates unattended day and night

## Other Software Options

AMASC01 can also run [AllskyTeam/allsky](/docs/AMASC01/base-software-stack/) (the default software for cameras sold before October 2026) or [indi-allsky](/docs/AMASC01/indi-allsky/).

## Installation

Caelum comes pre-installed on new AMASC01 cameras. To install it on an older camera or another Raspberry Pi (Raspberry Pi OS Bookworm, 64-bit), run:

```bash
curl -fsSL https://github.com/roman-dvorak/caelum/releases/latest/download/install.sh | sudo bash
```

The installer sets up Caelum as a systemd service together with its web interface. Further options and manual installation are described in the [Caelum deployment guide](https://caelum.astrometers.eu/guide/deployment).
