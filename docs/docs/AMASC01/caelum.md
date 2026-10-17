---
layout: page
title: AMASC01 caelum
subtitle: 'AMASC01: caelum capture software'
description: 'caelum – open-source headless capture engine for all-sky cameras developed by AstroMeters, with sky-aware auto-exposure, keograms, meteor detection and remote archive upload.'
keywords: 'caelum, AMASC01 caelum, all-sky camera software, allsky capture engine, Raspberry Pi allsky, sky-aware auto-exposure, keogram, meteor detection, FITS, DNG'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 5
hero_image: '/images/products/AMASC01/amasc01_hero.webp'
---

# AMASC01 caelum

**caelum** is an open-source, headless capture engine for all-sky cameras developed by AstroMeters. It is an **alternative software solution** for the [AMASC01](/products/AMASC01/) camera, designed for long-term unattended operation and scientific data collection.

- Documentation: <https://caelum.astrometers.eu>
- Getting started: <https://caelum.astrometers.eu/guide/getting-started>
- Source code: <https://github.com/roman-dvorak/caelum>

AMASC01 is **fully supported** by caelum – its Sony IMX477 sensor runs through the Raspberry Pi camera backend (picamera2/libcamera).

## Key Features

- **Sky-aware auto-exposure** – Sun and Moon positions are computed from an offline ephemeris, and separate exposure and gain presets are used for day, civil, nautical and astronomical twilight, and night. See [exposure control](https://caelum.astrometers.eu/guide/exposure).
- **RAM-first image pipeline** – frames are calibrated, measured and thumbnailed in memory; only what is worth keeping is written to disk, including raw FITS and DNG files with metadata.
- **Keograms and meteor detection** – built-in plugins assemble a daily keogram and detect meteor streaks; third-party plugins use the same interface. See [plugins](https://caelum.astrometers.eu/guide/plugins).
- **Storage and remote archive** – a rotating local cache with a retention policy and a self-healing rsync upload to a permanent remote archive, viewable as a static multi-camera gallery. See [storage](https://caelum.astrometers.eu/guide/storage) and [upload](https://caelum.astrometers.eu/guide/upload).
- **Web UI** – live view, recordings by night, file browser, settings, live logs and a web terminal, with admin and viewer accounts. See [web UI](https://caelum.astrometers.eu/guide/web-ui).
- **Updates from the browser** – releases are installed and rolled back from the web UI. See [updates](https://caelum.astrometers.eu/guide/updates).

## Position in the Software Ecosystem

The standard AMASC01 software environment is the [Base Software Stack](/docs/AMASC01/base-software-stack/) built on **AllskyTeam/allsky**. Another alternative is [indi-allsky](/docs/AMASC01/indi-allsky/).

caelum may be suitable for users who need:

- unattended operation on remote or networked observing stations
- raw scientific data (FITS, DNG) alongside preview images
- automatic archiving of several cameras to a central server
- meteor detection and keograms without additional tools

## Installation

On a Raspberry Pi running Raspberry Pi OS Bookworm (64-bit), caelum is installed with a single command:

```bash
curl -fsSL https://github.com/roman-dvorak/caelum/releases/latest/download/install.sh | sudo bash
```

The installer sets up caelum as a systemd service and its web interface. Further options and manual installation are described in the [caelum deployment guide](https://caelum.astrometers.eu/guide/deployment).

If you would like your AMASC01 delivered with caelum pre-installed, or want to discuss a suitable configuration, please [contact us](/about/#custom-development-and-contact).
