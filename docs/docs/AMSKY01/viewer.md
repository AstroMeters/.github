---
layout: page
title: AMSKY01 Viewer - Real-time Visualization Software
subtitle: 'AMSKY01: GUI and CLI tools for sensor monitoring'
description: 'Learn how to install and use AMSKY01 Viewer software for real-time visualization of cloud detection, sky brightness, temperature, and humidity data from your AMSKY01 sensor.'
keywords: 'AMSKY01 viewer, PyQt5, sensor visualization, cloud detection software, sky quality monitoring, real-time data, CSV logging, thermal map visualization'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 3
hero_image: '/images/docs.jpg'
---

# AMSKY01 Viewer – Real-time Visualization Software

The AMSKY01 Viewer is a Python-based GUI application for real-time monitoring and visualization of data from the AMSKY01 sensor. It provides an intuitive graphical interface for viewing sensor data including thermal maps, environmental conditions, and sky brightness measurements.


<p align="center">
  <img alt="AMSKY01 with GUI interface AMSKY01_viewer" src="/images/docs/AMSKY01/python-ui.png" width="80%">
</p>


> **Note:** The `amsky01` package also includes command-line tools (`amsky01_cli`) and log analysis utilities (`plot_logs`). See the [AMSKY01 repository](https://github.com/roman-dvorak/AMSKY01) and  [Linux software usage guide](/docs/AMSKY01/sw-linux/) for more information about these additional tools.

## GUI Viewer

<img width="600" alt="AMSKY01 Viewer interface" src="https://github.com/user-attachments/assets/d425eac0-dab1-45b2-90b5-168619107dd3" />

The graphical viewer provides real-time visualization using PyQt5 and PyQtGraph.

**Features:**
- **16×12 pixel IR thermal map** from MLX90640/MLX90641 thermopile array
- **Temperature and humidity** from SHT41 sensor including dew point calculation
- **Light measurements** from TSL2591 photometer with SQM (mag/arcsec²) conversion
- **Sensor diagnostics** including supply voltage (Vdd) and ambient temperature (Ta)
- **Multiple tabs** for organized data display (Graph, Data Table, HTTP API)

**Usage:**

```bash
# Basic usage with auto-detected port
amsky01_viewer

# Specify serial port and baudrate
amsky01_viewer --port /dev/ttyACM0 --baud 500000

# Enable debug output for troubleshooting
amsky01_viewer --port /dev/ttyACM0 --debug
```

**Command-line Options:**
- `--port` - Serial port device (default: auto-detect)
- `--baud` - Baudrate in bps (default: 115200)
- `--debug` - Enable verbose communication logging


## Integration with INDI, EKOS and KStars

The AMSKY01 GUI application can provide a built-in HTTP REST API, which allows sensor data to be accessed directly from INDI-lib, EKOS, and KStars. This means you can automatically attach real-time sky data to your FITS images or use the information to control your observatory automation—such as closing the dome if clouds are detected.

Configuration is simple: just enable the API endpoint on the third tab of the GUI. Then, in KStars, launch the `indi-amsky01-api` driver, which will automatically connect to the running API and make the data available in your astronomy workflow.

Thanks to this integration, AMSKY01 seamlessly extends the capabilities of your observatory software, making advanced sky condition monitoring and automation easy and reliable.


## Installation

The AMSKY01 software tools are available as a Python package on PyPI and can be installed easily using pip.

### Requirements

- Python 3.7 or newer
- USB-C or RS-485 connection to AMSKY01 sensor
- Linux, Windows, or macOS

### Install from PyPI (Recommended)

It is strongly recommended to use a virtual environment to avoid conflicts with system packages:

```bash
# Create a virtual environment
python3 -m venv amsky01-env

# Activate the virtual environment
source amsky01-env/bin/activate  # On Linux/macOS
# or
amsky01-env\Scripts\activate  # On Windows

# Install the package
pip install amsky01
```

This will install the viewer along with all required dependencies including PyQt5, PyQtGraph, pyserial, pandas, and matplotlib.

**Alternative: System-wide installation** (not recommended)
```bash
pip install amsky01
```

### Install from Source

For development or the latest features, you can install directly from the GitHub repository:

```bash
git clone https://github.com/roman-dvorak/AMSKY01.git
cd AMSKY01/sw
pip install -e .
```


### Running from Virtual Environment

If you installed using venv, make sure to activate the environment first:

```bash
source amsky01-env/bin/activate  # Linux/macOS
amsky01_viewer
```

## Troubleshooting

### Device Not Found

If the viewer cannot detect your AMSKY01 sensor:

1. Check USB connection
2. Verify device permissions:
   ```bash
   ls -l /dev/ttyACM*
   sudo chmod 666 /dev/ttyACM0  # Or add user to dialout group
   ```
3. Use `--port` option to specify device manually
4. Check baudrate matches sensor configuration (default: 500000)

### No Data Displayed

- Enable debug mode with `--debug` flag
- Verify sensor is powered and responding
- Check serial port settings (baudrate, parity)
- Ensure no other application is using the serial port

### Import Errors

If you encounter import errors, reinstall dependencies:

```bash
pip install --upgrade amsky01
# Or install dependencies manually:
pip install pyserial numpy pyqtgraph PyQt5 pandas matplotlib
```

## Source Code and Development

The AMSKY01 software tools are open-source and available on GitHub:

🔗 **Repository:** [https://github.com/roman-dvorak/AMSKY01/tree/main/sw](https://github.com/roman-dvorak/AMSKY01/tree/main/sw)

📦 **PyPI Package:** [https://pypi.org/project/amsky01/](https://pypi.org/project/amsky01/)

Contributions, bug reports, and feature requests are welcome via GitHub Issues.

## See Also

- [AMSKY01 Product Page](/products/AMSKY01/) - Sensor specifications and features
- [AMSKY01 Linux Software Usage](/docs/AMSKY01/sw-linux/) - Advanced Linux integration
- [AMSKY01 Main Documentation](/docs/AMSKY01/) - Complete technical documentation
