---
layout: post
title: "Project: Measurement of optical spectra from fireworks"
description: "A project focused on capturing and analyzing optical emission spectra of fireworks using a diffraction grating spectrograph. The recorded spectra reveal characteristic emission lines of metals used in pyrotechnic compositions."
keywords: "fireworks spectra, optical spectroscopy, diffraction grating, emission spectrum, pyrotechnics, spectrograph, astronomy, AstroMeters"
date: 2023-01-01
author: Roman Dvořák
lang: en
redirect_from:
  - /2023/01/01/fireworks-optical-spectra/
subtitle: "Capturing emission spectra of pyrotechnic compositions with a diffraction grating"
image: /images/blog/2023-01-01-fireworks-spectra/hero.jpg
hero_image: /images/blog/2023-01-01-fireworks-spectra/hero.jpg
hero_darken: true
hero_height: is-medium
tags:
  - spectroscopy
  - fireworks
  - optics
  - spectra
 
---

## A New Year’s Eve Experiment

New Year’s Eve is full of fireworks. People look at the sky and enjoy colors and light. This time, I had no plan I wanted to do something interesting. I had a simple idea. Fireworks are not only light. They are set of interesting elements. Each color comes from a different element. If I can split the light into a spectrum, I should be able to see these elements. So instead of just watching the fireworks, I decided to measure them. I built a simple spectrograph from parts I had or borrowed from my work. The goal was not to build a perfect instrument. The goal was to test if this idea works in real conditions.

<p align="center"><img src="https://github.com/roman-dvorak/Fireworks2023/assets/5196729/0ded7bbc-ed8d-42df-afb6-dae9101b5f0a" width="65%" /></p>


## Building the Setup
The setup was assembled using equipment available to us, allowing to conduct measurement without the need for purchasing expensive gear. This setup was chosen as "the best", with the idea that it could be simplified for futhure measurement based on this experiences (check observed problems at end of this document).

- **80/500 ED Telescope**: An optical device with an 80 mm lens diameter and 500 mm focal length, optimized for capturing clear, detailed images.
- **Spectral Grating 100 lines/millimeter**: Separates light into individual spectral lines for chemical element identification ([SA-100](https://www.rspec-astro.com/star-analyser/)).
- **Monochromatic High-Speed Camera**: Records 1000-800 frames per second, important for capturing fast-moving pyrotechnic events ([Chronos 1.4 monochrome](https://www.krontech.ca/product/chronos-1-4-high-speed-camera/)).
- **Tripod**: A sturdy tripod under the telescope allowing for quick aiming of the setup.
- **Finder Scope**: A device for quickly aiming the telescope.
- **Computer with sufficient storage capacity**: The camera produces a large amount of data; a 6-second recording is approximately 7 GB. Data was immediately uploaded via network to the connected computer.

<p align="center"><img src="https://github.com/roman-dvorak/Fireworks2023/assets/5196729/b99c4376-7233-4b5c-962b-cb13943ac42c" width="65%" /></p>

The following images shows the attaching of a diffraction grating to the camera. Grating was screwed to the end of a C-mount to 1.25" barrel adapter. It ensures constant sensor-grating distance within the optical system.

<div style="display: flex; gap: 1.5rem; align-items: flex-start; justify-content: center;">
  <img src="https://github.com/roman-dvorak/Fireworks2023/assets/5196729/c4ff3cd2-e0c2-44e5-9d8e-66ef24d8ffd8" style="height: 200px; width: auto;" />
  <img src="https://github.com/roman-dvorak/Fireworks2023/assets/5196729/514a96e6-aef7-419b-b3b0-fe0772c6c94e" style="height: 200px; width: auto;" />
</div>


## Cold Night Above Prague

The experiment took place during New Year’s Eve, from a higher building in Prague.

It was cold. The sky was full of random explosions. Fireworks are difficult targets:

- They appear suddenly
- They move fast
- They change brightness very quickly
- They disappear in a moment

The camera was running at high speed (up to \~1000 FPS). It recorded RAW12 data continuously. Each short recording was large. A few seconds could take several gigabytes. Data was sent directly to a computer over the network. Most of the data is useless. But sometimes, everything works. The firework is in the field of view, the focus is correct, and the spectrum is visible. These frames are the result.

## From Raw Data to Spectra

After the night, the real work started. The RAW12 format is efficient, but not easy to use. Two pixels are stored in three bytes. So the first step was conversion.I used a Python script to convert RAW12 files into TIFF images. This process is slow, but necessary. Then I used FFmpeg to create preview videos. This made it easier to search for good frames. You can see these videos here:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; margin-bottom: 1.5rem;">
  <iframe
    src="https://www.youtube.com/embed/tPwrmtYvqSc"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
    allowfullscreen
    loading="lazy"
  ></iframe>
</div>

After that, I manually selected frames with visible spectra. The analysis was done in a Jupyter Notebook. The workflow was simple and interactive. I selected a line across the spectrum. Then I calculated intensity along this line. Finally, I converted pixel position into wavelength. At this moment, the fireworks stopped being just images. They became data.

## Calibration

To convert pixels to wavelength, I used geometry of the setup.

Important parameters were:

- Grating density (100 lines/mm)
- Distance between grating and sensor (not perfectly known)
- Pixel size

To improve accuracy, I used known light sources:

- Sodium street lamp
- Green laser (532 nm)

Calibration works, but it is not perfect. This part needs improvement.

## What the Fireworks Reveal

When looking at the spectra, the result is clear. Fireworks do not produce continuous light. They produce lines. Each element has its own pattern:

- Sodium → yellow
- Strontium → red
- Barium → green
- Copper → blue

This confirms that the method works. However, identification is still manual. I do not have a full spectral database yet.

## Problems During the Experiment

The experiment also showed many problems. Focusing was difficult. The depth of field was very small. Aiming was also difficult. The telescope has high magnification and a narrow field of view. Exposure was another issue. Some parts were too bright, others too dark. The camera also needed time to save data. During this time, new events were missed.  All these problems are important. They show what needs to be improved.

## Results

The main result is simple. The method works. Even with a simple setup, it is possible to measure spectra of fireworks. The data is usable and shows clear emission lines. But the process is not automated. It still requires manual work.

<p align="center">
  <img src="/images/blog/2023-01-01-fireworks-spectra/spectrum_analysis.png" width="70%" alt="Spectrum analysis tool — raw frame with spectral lines and intensity profile" />
</p>
<p class="has-text-centered has-text-grey is-size-7">Interactive analysis tool: raw frame with spectral lines (top) and the extracted intensity profile (bottom).</p>

After extracting the intensity profile along the spectral line, the pixel positions were converted to wavelengths using the calibration. The resulting spectrum clearly shows individual emission peaks. The two dominant groups correspond to strontium lines in the red region (~614 nm, ~628 nm) and a strong sodium doublet near 589 nm.

## Next Steps

There are many ways to improve the system. Better aiming would help a lot. Maybe a tracking mount. Better diffraction grating would improve resolution. Faster data handling would reduce missed events. Better calibration is also needed. And finally, a spectral database is required for automatic identification.



<p align="center">
  <img src="/images/blog/2023-01-01-fireworks-spectra/spectrum_calibrated.png" width="75%" alt="Calibrated spectrum with labeled emission line wavelengths" />
</p>
<p class="has-text-centered has-text-grey is-size-7">Calibrated spectrum with labeled emission lines — visible peaks correspond to barium (green) and strontium (red) emission lines.</p>

## Related Links

- GitHub (full documentation, data, scripts):
  [https://github.com/AstroMeters/Fireworks2023](https://github.com/AstroMeters/Fireworks2023)

- Full PDF report with spectra:
  [https://github.com/AstroMeters/Fireworks2023/blob/main/media/merged.pdf](https://github.com/AstroMeters/Fireworks2023/blob/main/media/merged.pdf)

- Spectra gallery:
  [https://github.com/AstroMeters/Fireworks2023/blob/main/gallery.md](https://github.com/AstroMeters/Fireworks2023/blob/main/gallery.md)

- YouTube recordings:
  [https://www.youtube.com/playlist?list=PL3olITvRKy4xV\_I5JRlAe6PY4d6\_L131k](https://www.youtube.com/playlist?list=PL3olITvRKy4xV_I5JRlAe6PY4d6_L131k)

## Update

In the Czech Republic, from 2026, fireworks are strongly restricted. This means that similar experiments will be harder to repeat in the future.

