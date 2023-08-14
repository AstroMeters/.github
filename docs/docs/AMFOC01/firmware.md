---
layout: page
title: AstroMeters documentation page
subtitle: 'AMFOC01: Firmware'
menubar: docs_menu
show_sidebar: false
toc: false
---


The firmware is an integral part of the focuser, ensuring the proper control of the stepper motor for precise positioning, sensor readouts, and user interface interactions. This enables you to utilize all the features of your AMFOC01 focuser.

The firmware is open-source and fully available on [GitHub](https://github.com/AstroMeters/AMFOC01). Stable firmware releases, including their binary files, can be found in the [releases section](https://github.com/AstroMeters/AMFOC01/releases). You'll learn how to update your focuser to the latest version in the following sections. Detailed changes between firmware versions are also outlined in the release overview.

### Firmware Update:

For updating the firmware, a simple Python tool is provided, which facilitates the loading of new firmware onto the AMFOC01 focuser. While uploading, please ensure that you're selecting the correct file.

#### Procedure:
1. Download the appropriate [zip file](https://github.com/AstroMeters/AMFOC01/releases) with firmware from the [releases page](https://github.com/AstroMeters/AMFOC01/releases) as a ZIP archive.
2. Extract the ZIP archive, containing two files: the Python programming tool and the firmware itself.
3. Open a terminal in the directory where you've extracted the archive.
4. Connect the AMFOC01 to your computer using USB.
5. Execute the programming command.
6. Once the firmware is uploaded, you can disconnect the device and begin utilizing its new features.
