---
layout: page
title: AstroMeters documentation page
subtitle: 'AMFOC01: Focuser handling'
description: 'Complete AMFOC01 focuser handling guide covering user interface navigation, button functions, connection procedures, and operational modes. Learn how to effectively control your astronomical focuser for manual focusing, eyepiece mode, and configuration settings.'
keywords: 'AMFOC01 handling, telescope focuser operation, focuser user interface, manual focusing, eyepiece mode, focuser configuration, astronomy equipment control'
menubar: docs_menu
show_sidebar: false
toc: false
---


This page describes how to handle the AMFOC focuser and perform selected operations with it. We'll begin with an overview of the controller interface.

> Focuser image with arrows and descriptions...

#### Connection

#### Buttons

## User Interface
The focuser's user interface is managed using a set of four buttons, each with its own function. These buttons are used for navigating through various screens and interacting with the focuser's parameters.

* **BACK** - This button is used to return to the previous parent screen.
* **SET** - The SET button serves as an entry point to sub-screens or as a trigger for specific actions based on the current screen or for confirming selected values.
* **LEFT**, **RIGHT** - The LEFT and RIGHT buttons are employed for navigating between user interface pages or for adjusting individual values.

### User Interface Map
The following diagram illustrates the hierarchy and interconnections among different screens, which will be described in detail below.


[![](https://mermaid.ink/img/pako:eNp9kVFrgzAUhf9KyFME3cMeZQyK67CwKKxPG75c4tWGaSJptHSl_32x0Q0dNA8hnPsdzgn3QoUukca0avRJHMBY8vZeKOLOju2UtBIa-Q1WahWQKHomKUt1i6SDGgPP-ZtzxkH10JBWD9iisgF5ih5Ghwe2H1u2PWMnUeBxnnHuh0nGEq0qWfdmyvJzZyrUHOA0J23-J5GIgLjZfqMmdhG6xjaeG3OSNSgWbaaSf_z-Lk8eZ0c29Ujy7HX5w3WZ1JM5ywc0g8ST02lIWzQtyNIt6DJyBbUH9-WCxu5ZgvkqaKGujoPe6v1ZCRpb02NI-64Eiy8SagMtjStojk7FUlptuN_4bfEh7UB9aj0z1x8SNqJR?type=png)](https://mermaid.live/edit#pako:eNp9kVFrgzAUhf9KyFME3cMeZQyK67CwKKxPG75c4tWGaSJptHSl_32x0Q0dNA8hnPsdzgn3QoUukca0avRJHMBY8vZeKOLOju2UtBIa-Q1WahWQKHomKUt1i6SDGgPP-ZtzxkH10JBWD9iisgF5ih5Ghwe2H1u2PWMnUeBxnnHuh0nGEq0qWfdmyvJzZyrUHOA0J23-J5GIgLjZfqMmdhG6xjaeG3OSNSgWbaaSf_z-Lk8eZ0c29Ujy7HX5w3WZ1JM5ywc0g8ST02lIWzQtyNIt6DJyBbUH9-WCxu5ZgvkqaKGujoPe6v1ZCRpb02NI-64Eiy8SagMtjStojk7FUlptuN_4bfEh7UB9aj0z1x8SNqJR)


## Focuser Initialization
The focuser will automatically initiate itself upon power connection through either the coaxial DC connector or the USB-C port. The focuser will operate fully only when powered by a 12V source.

After startup, a system initialization will occur, configuring the individual components. Upon successful initialization, the introductory screen will be displayed on the OLED.

#### Introductory Screen
On the introductory screen, you will find basic information about the focuser. In two columns, you'll observe the status of USB connection and the 12V power source.

On the next line, you'll see the motor's status (whether it's rotating or stationary) and its position in steps. In the state of disconnected 12V power, the position will be zero, and the motor will not rotate.

The current temperature is displayed on the third line.


Now, by using the side arrows, you switch between individual focuser functions. Among these, you'll encounter the introductory screen, followed by Manual Focuser Control, the Rapid Focusing Tool, and Focuser Settings. To activate each function, press the 'SET' button on the respective page.


#### Manual focus
This page serves for easy manual focusing using the buttons. By pressing the 'SET' button, you adjust the focusing speed in increments of 10 steps. While holding the arrow buttons, you perform the actual focusing, moving in the respective direction.

#### Eyepiece mode


#### Configuration
In the settings, you can modify the fundamental behavior of the focuser. Currently, within the settings, you can adjust four aspects.

By pressing the 'SET' button, you select the parameter you want to adjust (actual parameter is marked with arrow). Subsequently, you use the arrow buttons to toggle its value. Upon exiting the menu (using the 'BACK' button), the settings will be permanently stored in the internal memory. This configuration will persist even after the focuser is restarted.