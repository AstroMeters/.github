---
layout: page
title: AstroMeters documentation page
subtitle: 'AMFOC01: Advanced focuser for astronomy telescopes'
menubar: docs_menu
show_sidebar: false
toc: false
---

# AMFOC01 – High-Precision Focuser for Astronomy and Optics

**AMFOC01** is a highly sophisticated focuser primarily designed for astronomical telescopes, but suitable for a wide range of optical devices. This device is engineered to deliver **smooth, quiet, and highly accurate focusing** thanks to its use of state-of-the-art components—specifically the [TMC5130 micro-stepping driver](https://www.trinamic.com/products/integrated-circuits/details/tmc5130/) and the [RP2040 processor](https://www.raspberrypi.org/products/rp2040/). These technologies provide performance far superior to traditional stepper control, completely eliminating the vibrations that often compromise imaging or visual observation.

AMFOC01 features a **red OLED display** and four tactile buttons, allowing for intuitive control and feedback—while preserving your night vision. The focuser can be connected to a computer via USB-C and controlled using any software compatible with the [MoonLite protocol](https://indilib.org/devices/focusers/moonlite-focuser.html), such as [KStars](https://edu.kde.org/kstars/) and [INDI](https://www.indilib.org/). It is also fully operational as a standalone unit, supporting both manual control and temperature-tracking modes without the need for a computer.

---

## Key Features

* **Exceptional smoothness and precision:**
  By combining the TMC5130 micro-stepping driver with the RP2040 processor, AMFOC01 delivers extremely precise and virtually silent focusing. Unlike classic stepper motor solutions, you won't experience any unpleasant vibrations transferred to your telescope or optical setup.
* **Flexible and robust power input:**
  Operates on 9–16V DC (5.5/2.1mm coaxial connector), making it easy to use with car batteries or any standard 12V field power supply.
* **User-friendly control and compatibility:**
  With a red OLED display and four buttons (BACK, SET, LEFT, RIGHT), the AMFOC01 is easy to use in the dark and provides clear feedback. Control via USB-C enables seamless integration with MoonLite-compatible software, while manual and temperature-tracking modes make it suitable even for users who prefer computer-free operation.
* **Integrated temperature sensor:**
  The built-in thermometer monitors ambient temperature, allowing the focuser to compensate automatically for thermal expansion/contraction and maintain optimal focus throughout the night.
* **Customizable mounting:**
  Designed for adaptability—thanks to 3D printing, you can easily create and attach mechanical adapters for a wide range of telescopes or optical devices.
* **Open-source design:**
  Hardware, firmware, and software are fully open-source and available for customization or further development. Custom modifications are also available upon request.

---

## Device Description

The AMFOC01 focuser includes:

1. **USB-C interface** for computer connection (data only, not for powering the motor)
2. **RJ12 connector** for a wired hand controller
3. **MiniDIN connector** for the stepper motor
4. **12V power input** (coaxial DC, 5.5/2.1mm)
5. **Red OLED display**
6. **Four interface buttons:** BACK, SET, LEFT, RIGHT

---

## Usage Scenarios

One of the major strengths of AMFOC01 is its **versatility**. It is designed to serve a wide spectrum of astronomy users and workflows:

### Robotic/Automated Observing

Connect AMFOC01 to your computer via USB-C and control your telescope’s focusing mechanism with robust and proven tools like INDI and EKOS within KStars.
The focuser fully supports the MoonLite protocol, which ensures seamless integration with many existing astronomy software suites without any need for special drivers or software updates.

AMFOC01 can report its absolute position, receive and process focus commands, and apply temperature-based corrections automatically—ensuring your focus remains sharp throughout long imaging sessions.

### Autonomous Operation

Not every astronomer wants to use a computer in the field! AMFOC01 is perfect for those who prefer visual observing or simple camera setups.
Its user interface (display + buttons) enables quick and precise manual focusing, while the integrated temperature compensation feature can automatically refocus your telescope as temperatures change.

You can easily focus or re-focus based on filter swaps, temperature drift, or just your own eye, without disturbing your equipment or introducing vibrations.

### Visual Observing

When switching eyepieces, it’s easy to lose focus or even have the object slip out of the field of view—especially with high-power eyepieces.
AMFOC01 lets you **store eyepiece focus positions** and instantly recall them with a single click, so you can swap between different eyepieces quickly and always keep your object sharply in view.

Fine-tuning to your personal eyesight is straightforward using the precise control buttons.

---

## Construction

AMFOC01 is **designed, developed, and assembled entirely in-house**, with no off-the-shelf Chinese modules—ensuring top build quality and full control over every aspect of the product.
This careful engineering, especially in the electronics, guarantees a **super-smooth, vibration-free focusing experience** for astrophotography or visual observation.

<p align="center">
  <img alt="AMFOC01 Top" src="/images/products/AMFOC01/AMFOC01-top.png" width="49%">
  <img alt="AMFOC01 Bottom" src="/images/products/AMFOC01/AMFOC01-bottom.png" width="49%">
</p>

The red OLED display is designed to minimize impact on night vision.
The focuser includes an internal thermometer and supports the option to add an external thermometer for even more precise temperature readings.

**Stepper Motor Connection:**
The focuser uses a 4-pin miniDIN connector to drive the stepper motor.
*Add diagram or table of pinout here when ready.*

*Planned: Detailed motor parameter recommendations for best results.*

---

## Open-Source Project

AMFOC01 is **fully open-source**:

* All software, firmware, and hardware documentation is freely available for review and modification.
* Community contributions and feedback are welcome.
* Custom adaptations and consultation are available for advanced users and institutions.

---

## Resources & Links

* [MoonLite Focuser Protocol Documentation](https://indilib.org/devices/focusers/moonlite-focuser.html)
* [KStars Planetarium](https://edu.kde.org/kstars/)
* [INDI Library](https://www.indilib.org/)
* [Project GitHub Repository](https://github.com/your-repo) (add actual link)
* [Contact & Support](mailto:info@astrometers.eu)

---

**Do you have a special telescope, or need help with a custom adapter or setup?**
We are happy to provide guidance, custom mechanical designs, or firmware features—just get in touch.
