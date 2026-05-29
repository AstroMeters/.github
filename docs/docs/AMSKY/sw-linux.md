---
layout: page
title: AMSKY – Linux Setup
subtitle: 'AMSKY: Sky quality and cloud sensors'
description: 'AMSKY Linux usage – stable device naming, sensor_viewer.py tool, INDI driver integration, and ser2net TCP streaming. Works with AMSKY01 and AMSKY02.'
keywords: 'AMSKY sensor, AMSKY01, AMSKY02, sky quality meter, cloud detection sensor, USB-C weather sensor, astronomical weather station, RS-485 sensor, SQM, sky monitoring, environmental sensor, observatory automation'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 2
hero_image: '/images/docs.jpg'
redirect_from:
  - /docs/AMSKY01/sw-linux/
---

# AMSKY – Software Usage on Linux

This section describes how to use AMSKY sensors (AMSKY01 and AMSKY02) under Linux. It covers stable device naming, usage with the `sensor_viewer.py` tool, integration with the INDI driver, and making the sensor available over the network using ser2net. Each method includes guidance on when it is most appropriate to use.

---

## 1) Stable Device Naming

When the sensor is connected, it usually appears as `/dev/ttyACM0`, `/dev/ttyACM1`, etc. The assigned number may change between reboots or re-plugs, which can be inconvenient. There are two recommended approaches to create a stable name:

### Option A – using `/dev/serial/by-id/`

The system automatically creates symlinks containing the manufacturer name and the device serial number. These symlinks are unique and stable.

Example:

```bash
ls -l /dev/serial/by-id/
usb-AstroMeters.eu_AMSKY01_DF6490926758602A-if00 -> ../../ttyACM0
```

This symlink can be used directly in your applications.

### Option B – custom symlink using udev

If you prefer shorter names (e.g. `/dev/ttyAMSKY`), you can create a udev rule based on Vendor ID and Product ID.

1. Identify values using `lsusb`:

   ```bash
   lsusb
   # Example: ID 1209:ae02 AstroMeters.eu AMSKY
   ```
2. Create rule `/etc/udev/rules.d/99-amsky.rules`:

   ```udev
   SUBSYSTEM=="tty", ATTRS{idVendor}=="1209", ATTRS{idProduct}=="ae02", SYMLINK+="ttyAMSKY"
   ```
3. Apply rule:

   ```bash
   sudo udevadm control --reload-rules
   sudo udevadm trigger
   ls -l /dev/ttyAMSKY
   ```

This approach is useful if you want a simple, consistent port name regardless of the specific device serial number.

---

## 2) Using `sensor_viewer.py`

`sensor_viewer.py` is intended for users who want to quickly view AMSKY data or log it to a CSV file. It supports both serial and TCP connections.

Show help:

```bash
python3 sensor_viewer.py --help
```

Typical use cases:

* **Quick sensor testing** without additional software.
* **Data logging** to a CSV file for later analysis.
* **Remote access** to the sensor over TCP if ser2net is enabled (see chapter 4).

Detailed instructions and examples are provided on a dedicated documentation page for this tool.

---

## 3) Using INDI

The INDI driver is recommended if you want to integrate the AMSKY sensor with astronomy software (e.g. KStars/Ekos) or in larger systems where a unified interface for multiple devices is required.

<img width="866" height="653" alt="image" src="https://github.com/user-attachments/assets/2c46e338-ea4b-472f-8d5c-64ea2ba1ef52" />


### 3.1 Starting the INDI server

```bash
indiserver indi_amsky01
```

### 3.2 Connection options

In the AMSKY driver you can choose:

* **Serial connection** – simple and direct for local use.
* **TCP connection** – useful if the device is shared over the network via ser2net.

### 3.3 Command line configuration

```bash
indi_getprop | grep AMSKY
indi_setprop "AMSKY01.CONNECTION.CONNECTION_MODE=Serial"
indi_setprop "AMSKY01.SERIAL.PORT=/dev/ttyAMSKY"
indi_setprop "AMSKY01.CONNECTION.CONNECT=On"
```

Detailed installation instructions for INDI drivers are described on a separate documentation page.

---

## 4) Converting Serial Port to TCP Stream (ser2net)

In some cases, it is advantageous not to access the sensor directly via a serial port but to expose it as a TCP stream. This approach allows multiple clients to connect simultaneously, simplifies remote access over the network, and unifies configuration for applications.

### 4.1 When to use ser2net

Ser2net is useful in the following scenarios:

* You want **multiple applications** (e.g. `sensor_viewer.py` and the INDI driver) to access AMSKY at the same time.
* You need **remote access** to the sensor from another computer.
* You want to simplify configuration for applications that prefer TCP connections over serial ports.

Using TCP increases flexibility and compatibility.

### 4.2 Installing ser2net

On Debian/Ubuntu:

```bash
sudo apt-get update
sudo apt-get install ser2net
```

### 4.3 Configuration

Configuration file `/etc/ser2net/ser2net.yaml`:

```yaml
connection: &amsky
  accepter: tcp,0.0.0.0,2000
  enable: on
  options:
    banner: "AMSKY ready\n"
    kickolduser: true
    telnet-brk-on-sync: true
  connector: serialdev,/dev/ttyAMSKY,9600n81,local
```

### 4.4 Restarting the service and testing

```bash
sudo systemctl restart ser2net
sudo systemctl status ser2net
ss -ltnp | grep :2000
```

Quick test with netcat:

```bash
nc localhost 2000
```

---
