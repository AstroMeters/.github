---
layout: page
title: AMFOC01
subtitle: Advanced focuser for astronomy telescopes
menubar: docs_menu
show_sidebar: false
toc: true
---


AMFOC01 is a highly sophisticated focuser primarily designed for astronomical telescopes, but it can also be applied to other optical devices. It employs cutting-edge technologies, such as the micro-stepping driver [TMC5130](https://www.trinamic.com/products/integrated-circuits/details/tmc5130/) for stepper motors and the [RP2040](https://www.raspberrypi.org/products/rp2040/) processor. These components ensure smooth and quiet operation without the unpleasant vibrations common with traditional methods of controlling stepper motors.

The device is equipped with an red OLED display and four buttons for easy user interaction. It can be connected to a computer via USB-C and controlled using software compatible with the [MoonLight](https://indilib.org/devices/focusers/moonlite-focuser.html) protocol, such as [KStars](https://edu.kde.org/kstars/) or [INDI](https://www.indilib.org/) or it can be used without computer in manual or temperature-tracking mode.

### Key Features

- **High precision and smooth operation:** Thanks to the use of the micro-stepping driver [TMC5130](https://www.trinamic.com/products/integrated-circuits/details/tmc5130/) and the [RP2040](https://www.raspberrypi.org/products/rp2040/) processor, the focuser provides smooth and quiet operation, ensuring high focusing accuracy without vibrations transferred to the assembly.
- **Power flexibility:** The focuser can be powered in the voltage range of 9-16V, making it compatible with lead-acid batteries (e.g., car batteries) or car onboard voltage. Powering is realized through a coaxial DC connector 5.5/2.1.
- **Easy operation and compatibility:** AMFOC01 is equipped with a red OLED display and four buttons for intuitive control. It can be connected to a computer via USB-C and controlled using software compatible with the [MoonLight](https://indilib.org/devices/focusers/moonlite-focuser.html) protocol. However, the motor cannot be powered via USB-C.
- **Temperature measurement:** The focuser includes an integrated thermometer for monitoring ambient temperature, which is useful for compensating for temperature influences on focusing.

AMFOC01 is designed to be easily connectable to a wide range of astronomical telescopes. Using 3D printing, customized mechanical adapters can be created for specific telescope models or optical systems.

Project is fully open-source. This means that all software, firmware, and hardware design are publicly available and can be modified according to the user's needs. We are also offering custom modification on request.

AMFOC01 can be used in a variety of scenarios where precise focusing of optical systems is needed. This device is primarily intended for astronomical telescopes but can also be used in other optical devices.
