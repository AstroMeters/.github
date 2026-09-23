---
title: AMUSBMOUNT
subtitle: Add USB interface to your mount
description: 'EQmod USB-C converter for Skywatcher mounts (EQ8, EQ6, HEQ5). Plug-and-play control with Stellarium, KStars/INDI, and ASCOM.'
product_code: AMUSBMOUNT01
keywords: 'AMUSBMOUNT01, EQmod converter, USB-C mount controller, Skywatcher mount control, telescope automation, EQ8 controller, EQ6 automation, HEQ5 control, mount interface, Stellarium control, KStars INDI, ASCOM driver, RJ45 converter'
layout: product
image: '/images/products/USBMOUNT01/USBMOUNT01A_photo.webp'
hero_image: '/images/products/USBMOUNT01/am_usbmount_hero.webp'
price: 42.20 EUR
buttons:
  - url: mailto:info@astrometers.eu?subject=AMUSBMOUNT01%20offer%20request
    text: Get offer
    icon_class: fas fa-envelope
  - url: https://lectronz.com/products/amusbmount01
    icon: https://lectronz-images.b-cdn.net/static/badges/buy-it-on-lectronz-medium.png
---

Maximize the potential of your telescope mount with direct computer control.

While many amateur astronomers appreciate mounts like Skywatcher for their optimal balance of price and quality, the true potential of many mounts, across various brands, is unlocked when connected to a computer. Enhance your observational capabilities and precision with the USBMOUNT converter.


## Usage Guide

### Setting Up the Connection
- **Computer Connection:** Simply plug the USBMOUNT into your computer using a USB-C cable, like the one you might use for your smartphone. Upon a successful connection, the `PC (pwr)` LED will light up. For optimal performance, it's best to use a high-quality cable.
- **Mount Connection:** The converter features an RJ45 connector. Use either the hand control cable or a direct Ethernet cable for the connection (ensure your mount supports an RJ45 connection - refer to the table below). Once connected, the `MOUNT (pwr)` LED will illuminate.

### Attaching the Device
Attach using the provided 3M DualLock Reclosable Fastener. Before adhering, clean and degrease the surface. Once glued, press down firmly for some time.

For long-distance USBMOUNT (EQmod) operations, opt for a longer RJ45 cable on the telescope side. A standard, shielded ethernet cable is recommended. However, avoid USB cables longer than 5m to maintain reliability.

### LED Alerts
The USBMOUNT features 4 LED indicators. The two red LEDs signal power in the adjacent connector, confirming a successful connection. The two orange LEDs monitor data transfer: `TX` indicates data flowing from the computer to the mount, while `RX` signals the opposite.

### Driver Installation
#### Linux
USBMOUNT01 seamlessly integrates with modern Linux computers. No driver installation is needed – just connect the device and it appears as a serial port (e.g. `/dev/ttyUSB0` or `/dev/ttyACM0`). You can then operate the mount with your go-to control software, such as INDI combined with KStars.

#### Windows
After connecting, the converter appears as a COM port – check *Device Manager → Ports (COM & LPT)* for the assigned number. To control the mount from ASCOM-compatible applications, install the [EQMOD ASCOM driver](https://eq-mod.sourceforge.net/) and select this COM port in its settings. If no COM port appears, please [contact us](mailto:info@astrometers.eu).

#### Stellarium
Enable the *Telescope Control* plugin in Stellarium and add a new telescope. On Windows, choose the ASCOM connection with the EQMOD driver; on Linux, connect through INDI with the *EQMod Mount* driver. Select the serial port assigned to USBMOUNT01.

#### KStars/INDI/Ekos
In the Ekos profile editor, select the **EQMod Mount** driver as the mount. Start INDI, open the *Connection* tab of the EQMod Mount driver in the INDI Control Panel, set the port to the one assigned to USBMOUNT01 and press *Connect*.

## Compatibility

| Mount Name | Connector Type | Additional Information |
|------------|----------------|------------------------|
| EQ8 | RJ45 | |
| AZ-EQ6 | RJ45 | |
| EQ6-R | RJ45 | |
| NEQ6 PRO | RJ45 | |
| EQ6 Pro | RJ45 | |
| EQ6 Synscan | RJ45 | |
| HEQ5 SynScan | RJ45 | |
| HEQ5 SynTrek | RJ45 | |
| EQ5 Synscan | RJ45 | |
| EQ4 with Synscan (EQ5) | | |
| EQ3-2 with Synscan | | |

> Note: This list might not cover all compatible mounts.
