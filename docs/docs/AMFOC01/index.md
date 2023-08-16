---
layout: page
title: AstroMeters documentation page
subtitle: 'AMFOC01: Advanced focuser for astronomy telescopes'
menubar: docs_menu
show_sidebar: false
toc: false
---


AMFOC01 is a highly sophisticated focuser primarily designed for astronomical telescopes, but it can also be applied to other optical devices. It employs cutting-edge technologies, such as the micro-stepping driver [TMC5130](https://www.trinamic.com/products/integrated-circuits/details/tmc5130/) for stepper motors and the [RP2040](https://www.raspberrypi.org/products/rp2040/) processor. These components ensure smooth and quiet operation without the unpleasant vibrations common with traditional methods of controlling stepper motors.

The device is equipped with an red OLED display and four buttons for easy user interaction. It can be connected to a computer via USB-C and controlled using software compatible with the [MoonLight](https://indilib.org/devices/focusers/moonlite-focuser.html) protocol, such as [KStars](https://edu.kde.org/kstars/) or [INDI](https://www.indilib.org/) or it can be used without computer in manual or temperature-tracking mode.

## Key Features

- **High precision and smooth operation:** Thanks to the use of the micro-stepping driver [TMC5130](https://www.trinamic.com/products/integrated-circuits/details/tmc5130/) and the [RP2040](https://www.raspberrypi.org/products/rp2040/) processor, the focuser provides smooth and quiet operation, ensuring high focusing accuracy without vibrations transferred to the assembly.
- **Power flexibility:** The focuser can be powered in the voltage range of 9-16V, making it compatible with lead-acid batteries (e.g., car batteries) or car onboard voltage. Powering is realized through a coaxial DC connector 5.5/2.1.
- **Easy operation and compatibility:** AMFOC01 is equipped with a red OLED display and four buttons for intuitive control. It can be connected to a computer via USB-C and controlled using software compatible with the [MoonLight](https://indilib.org/devices/focusers/moonlite-focuser.html) protocol. However, the motor cannot be powered via USB-C.
- **Temperature measurement:** The focuser includes an integrated thermometer for monitoring ambient temperature, which is useful for compensating for temperature influences on focusing.

AMFOC01 is designed to be easily connectable to a wide range of astronomical telescopes. Using 3D printing, customized mechanical adapters can be created for specific telescope models or optical systems.

Project is fully open-source. This means that all software, firmware, and hardware design are publicly available and can be modified according to the user's needs. We are also offering custom modification on request.

AMFOC01 can be used in a variety of scenarios where precise focusing of optical systems is needed. This device is primarily intended for astronomical telescopes but can also be used in other optical devices.


## AMFOC01 description

1. USB interface with USB-C
1. RJ12 connector from wire hand controller
1. MiniDIN connector for motor 
1. Power input - coaxial DC connector, 12V
1. OLED red display
1. Four interface buttons (BACK, SET, LEFT, RIGHT)



## Usage
A unique feature of the AMFOC01 focuser is its versatility, allowing it to be used for manual visual observation, astrophotography with just a camera, or in complex telescope setups controlled by a computer. Thanks to its design, AMFOC01 can cater to all of these possibilities.

In the following section, you will discover key features tailored for specific types of observation.

### Robotic Observing
AMFOC01 can be connected to your computer via USB-C, allowing you to control your telescope's focusing mechanism. The recommended tool for controlling the focuser is the INDI system and the EKOS interface within the KStars planetarium software.

The focuser currently supports the MoonLite protocol, making it seamless to integrate into existing setups without the need for software updates. Through the MoonLite protocol, you can retrieve the current position of the focuser and send commands for adjustments. Equipped with a thermometer, the focuser can perform automatic focusing corrections based on temperature changes.

### Autonomous Operation
Many astrophotographers observe without connecting a computer. They need the ability to focus or refocus based on temperature or the optical filter in use. This is where AMFOC01 proves invaluable. With its intuitive user interface and wide voltage input range, you can seamlessly integrate AMFOC into your setup and enjoy very sharp images. 

Utilizing the wired controller, you can achieve precise and rapid focusing without introducing vibrations or movements to the optical system. Enabling the temperature correction, you can let the focuser automatically refocus throughout your observation session, ensuring consistently sharp images.

### Visual Observing
Do you enjoy observing celestial objects with the naked eye trough telescope? It's a wonderful pursuit. However, changing eyepieces often requires significant refocusing, potentially causing the object to slip out of view, especially when switching to eyepieces with smaller focal lengths. This is where the AMFOC system comes to your aid. You can easily store your eyepieces in the AMFOC system, allowing the focuser to be adjusted with a single click, ensuring the object remains beautifully sharp even with a new eyepiece. You can then fine-tune the focus according to your eye's preference. Simple, isn't it? :)

## Construction
The focuser's electronics are of our proprietary design, development, and manufacturing. No Chinese modules are utilized within the focuser, ensuring both its robustness and high quality. Thanks to the ingenious electronics design, the focuser provides exceptionally smooth focusing, without introducing undesirable vibrations to your setup.

<p align="center">
  <img alt="Light" src="/images/products/AMFOC01/AMFOC01-top.png" width="49%">
  <img alt="Dark" src="/images/products/AMFOC01/AMFOC01-bottom.png" width="49%">
</p>


The focuser includes a high-quality red OLED display, offering a quick overview of the focuser's status while not disturbing your night vision adaptation.

Equipped with an integrated thermometer, the focuser can also accommodate an external thermometer for more precise temperature readings.

As the actuating component, a stepper motor terminated with a 4-pin miniDIN connector is assumed. The connector wiring is as follows:

> PICTURE OF motor WIRING

> TODO: Add possible motor parameters.
