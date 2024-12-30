# Table of Contents

1. [Overview](#overview)  
2. [JoySticks](#joysticks)  
3. [CentOS and Fedora Automotive Distro](#centos-and-fedora-automotive-distro)  
4. [Features](#features)  
5. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
     - [Step 1: Clone the Repository](#step-1-clone-the-repository)  
     - [Step 2: Install Dependencies](#step-2-install-dependencies)  
6. [Example: Joystick-Controlled UGV](#example-joystick-controlled-ugv)  
7. [Waveshare Robotic Arm Kit](#waveshare-robotic-arm-kit)
8. [Not Tested Yet](#not-tested-yet)  
9. [COVESA and VSS](#covesa-and-vss)
10. [Contributions](#contributions)  
11. [License](#license)  

# Waveshare Rover Devices Support Module

## Overview

This repository provides a **generic Python module** designed to support Waveshare devices, particularly for Unmanned Ground Vehicles (UGVs) and remote-controlled robotics projects. The module simplifies integration, control, and operation of vehicles by offering features like joystick-based driving, Wi-Fi connectivity, and motor speed control.

Tested devices include:

- **Waveshare UGV Rover Open-Source 6 Wheels 4WD AI Robot, Compatible with Raspberry Pi 5, Dual Controllers, Comes with Pan-Tilt Module, PI5-4GB Included**  
- [Amazon link](https://www.amazon.com/gp/product/B0D2L27JDT/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)  
<p align="center">
  <img src="https://raw.githubusercontent.com/dougsland/waveshare/main/pics/01.jpg" alt="Waveshare UGV Rover Open-Source 6 Wheels 4WD AI Robot, Compatible with Raspberry Pi 5, Dual Controllers, Comes with Pan-Tilt Module, PI5-4GB Included" width="50%">
</p>
   
   - Enables the use of Raspberry Pi Compute Module (CM) in standard Raspberry Pi 4 setups.
   - Offers compatibility with GPIO and other Raspberry Pi peripherals.

- **Waveshare Wave Rover Flexible and Expandable 4WD Mobile Robot Chassis, Full Metal Body, Multiple Hosts Support, with Onboard ESP32 Module**
- [Amazon link](https://www.amazon.com/gp/product/B0CF55LM6Q/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)  
<p align="center">
  <img src="https://github.com/dougsland/waveshare/blob/main/pics/02.jpg" alt="Waveshare Wave Rover Flexible and Expandable 4WD Mobile Robot Chassis, Full Metal Body, Multiple Hosts Support, with Onboard ESP32 Module" width="50%">
</p>

   - A compact baseboard with Power over Ethernet (PoE) support.  
   - Ideal for powering IoT and automotive projects via Ethernet.

---

## JoySticks

Tested JoySticks

- **PC Joystick, USB Gaming Flight Simulator Game Controller with Vibration Function and Throttle Control, PXN 2113 Wired Gamepad Flight Sim Stick for Windows PC/Computer**
- [Amazon link](https://www.amazon.com/gp/product/B06XGBL1HL/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)  
<p align="center">
  <img src="https://github.com/dougsland/waveshare/blob/main/pics/joysticks/1.jpg" alt="PC Joystick, USB Gaming Flight Simulator Game Controller with Vibration Function and Throttle Controller, PXN 2113 Wired Gamepad Flight Sim Stick for Windows PC/Computer" width="50%">
</p>

- **PS5 PlayStation DualSense®**
- [Amazon link](https://www.amazon.com/PlayStation-DualSense%C2%AE-Wireless-Controller-White-5/dp/B0CQKLS4RP/ref=sr_1_3?crid=3HJ0GMFISNWGT&dib=eyJ2IjoiMSJ9.LaC19IrSLdAwP5Gxrrk1v97nBzs5JfZBgrfiZcRPcQ23UsYeRDoDedv4BDQNSrGpicTx5kb2vNw4WIbg3C6vQgS9z_46e8tApi9a3NXKp9-BzmpoDfhgjPbF3YFaoeaGj2yPkAfzMIcY0rIks9Skd11rXIE598rBynk1g4uIDVFqWdwTCgXfxvmUKlFeZZyGrZjRAYsKbNr9HjaVWMXYNtAEXKPqEUTUbo6l-TR4KaY.c9mT2ZS0arEwVVbpzsjmKZwRjK3z8QNWP_Zbx310zlk&dib_tag=se&keywords=ps5%2Bjoystick&qid=1735369418&sprefix=ps5%2Bjo%2Caps%2C134&sr=8-3&th=1)
<p align="center">
  <img src="https://github.com/dougsland/waveshare/blob/main/pics/joysticks/2.jpg" alt="Joystick PS5" width="50%">
</p>

---

## CentOS and Fedora Automotive Distro

CentOS and Fedora Automotive is tested and works out of box. To deploy it you will require to plug a raspberry into the UAV and install the distribution into the SDcard.  

To install follow the steps below (assuming you are using Fedora latest):

Example:

1) Download the lastest Fedora Image, example Workstation
```console
wget https://dl.fedoraproject.org/pub/fedora/linux/releases/41/Workstation/aarch64/images/Fedora-Workstation-41-1.4.aarch64.raw.xz
```

Please note for CentOS Automotive SIG, [download the **aarch64** version](https://autosd.sig.centos.org/AutoSD-9/nightly/sample-images/).

2) Install it via software store **Raspberry Pi Imager** and *upload the Fedora image into SDCard*
![Software Store Raspberry Pi Imager](https://github.com/dougsland/waveshare/blob/main/pics/software_storage_rasp_pi_imager.png)

3) Insert SDCard into the UAV and turn on, to avoid the AC cord, use batteries, for example [6pcs 1￵8￵6￵50 Rechargeable Batter￵y 5000mAh W￵i￵th 18650 Battery Charger,Universal Charger for Rechargeable 3.7V Li-ion Batteries 26650 14500 10440 Tokeyla (Button Top Type)](https://www.amazon.com/gp/product/B0BCW9Q5QQ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1)

<p align="center">
  <img src="https://github.com/dougsland/waveshare/blob/main/pics/raspberry_on_rover_autosd_photo1_720.jpg" alt="Fedora 41 booting in ARM" width="50%">
</p>

## Features

- **Joystick-Based Control**:
  - Use any standard joystick or game controller to drive the vehicle (Must be supported by pygame).

- **Wi-Fi Connectivity**:
  - Easily connect to and control the vehicle via Wi-Fi.

- **Motor Speed Normalization**:
  - Smooth and accurate motor speed adjustments for stable navigation.

- **Cross-Platform Support**:
  - Works on Raspberry Pi OS and other Linux-based distributions.

---

## Getting Started

### Prerequisites

1. **Hardware**:
   - Raspberry Pi Compute Module 4 (CM4) with one of the supported Waveshare adapters.
   - A compatible joystick or game controller.
   - A vehicle chassis with motor drivers connected to the Raspberry Pi.

2. **Software**:
   - Python 3.x.
   - Required libraries installed (see below).

---

### Installation

#### Step 1: Clone the Repository

```bash
git clone https://github.com/dougsland/waveshare.git
cd waveshare
```

#### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Example: Joystick-Controlled UGV

The following example demonstrates how to use the module to control a UGV using a joystick and Wi-Fi:

```python
import pygame
from FOSS import UGVController
from time import sleep

# Instantiate the controller with default parameters
ugv_controller = UGVController(
    ssid="UGV",             # Default Wifi
    password="12345678",    # Default Pass
    ip="192.168.4.1",       # Default IP for the Rover
    interface_name="wlan0"  # Your device interface name
)

# Connect to Wi-Fi
ugv_controller.connect_to_wifi()

# Initialize pygame and joystick
pygame.init()
pygame.joystick.init()

# Ensure a joystick is connected
if pygame.joystick.get_count() == 0:
    print("No joystick detected. Please connect a joystick.")
    pygame.quit()
    exit()

# Get the first joystick
joystick = pygame.joystick.Joystick(0)
joystick.init()
print(f"Joystick detected: {joystick.get_name()}")

# Control loop
try:
    print("Use the joystick to control the UGV.")
    print("Press Ctrl+C to exit.")

    while True:
        # Process events
        pygame.event.pump()

        # Get joystick axis values
        axis_forward_back = joystick.get_axis(1)  # Forward/Backward
        axis_left_right = joystick.get_axis(0)   # Left/Right

        # Map axis values to speeds
        forward_speed = -axis_forward_back  # Invert to match UGV forward
        turn_speed = axis_left_right

        # Calculate motor speeds
        left_speed = forward_speed + turn_speed
        right_speed = forward_speed - turn_speed

        # Normalize speeds if necessary
        max_speed = max(abs(left_speed), abs(right_speed), 1.0)
        left_speed /= max_speed
        right_speed /= max_speed

        # Command the UGV
        ugv_controller.move(left_speed=left_speed, right_speed=right_speed)

        # Delay to avoid spamming commands
        sleep(0.1)

except KeyboardInterrupt:
    print("\nStopping the UGV...")
    ugv_controller.move(left_speed=0, right_speed=0)
    print("UGV stopped. Exiting.")
finally:
    pygame.quit()
```

---

## Waveshare Robotic Arm Kit

Waveshare Robotic Arm Kit, Desktop Robot Kit, High-Torque Serial Bus Servo, Based On ESP32, 4-DOF, Supports Flexible Expansion and Secondary Development, Wireless Control

First, connect to wireless network available, usually is **RoArm-M2**, the defaul password is 12345678. Feel free to script or change the python examples for automation and send a PR for this repo. ;-)

<p align="center">
  <img src="https://github.com/dougsland/waveshare/blob/main/pics/03.jpg" alt="robotic arm" width="50%">
</p>

---

## Not tested yet

- [Waveshare UGV Beast ROS 2 Open-Source Off-Road Tracked AI Robot, Dual Controllers, Computer Vision, All-Metal Body, Flexible and Expandable, Compatible with Raspberry Pi 5 (Not Included)](https://www.amazon.com/Waveshare-Open-Source-Controllers-Expandable-Compatible/dp/B0DJQD9MZZ/ref=sr_1_3?crid=3A5TOSRQ6SVWV&dib=eyJ2IjoiMSJ9.4dkL0mW3Dn3Ghl4rp6VwkjMS_q7FLodJwb1fTGW7o-oCa33bm5F1XaWHDeLXwiuFAvUWLeOqGCFC08a7-LH6TyxcNgA2YnWBcMB7Dqy4XF4S1T5ujDYoWyrNvEbcYR3Sv0vjlG28eBAJxGv9AB5wNC8eeCAUb35MHY9iM0inwWUF-X0tG5leCSG-BitA2Vjl2SKLn_M7APTnDuEghrehn8jVGVFV7xHEveAop45tH_s.ZojNYtIzvhGswvJxQIxipQMmMr9r1reUKmYQyP5T3e0&dib_tag=se&keywords=Waveshare+UGV+Rover+Open-Source+beast&qid=1735342472&sprefix=waveshare+ugv+rover+open-source+beas%2Caps%2C222&sr=8-3)

- [Waveshare UGV Rover Open-Source 6 Wheels 4WD AI Robot, Compatible with Raspberry Pi 5, Dual Controllers, Computer Vision, PI5-4GB NOT Included](https://www.amazon.com/Waveshare-Open-Source-Compatible-Raspberry-Controllers/dp/B0D2L1ST5X/ref=sr_1_4?crid=3A5TOSRQ6SVWV&dib=eyJ2IjoiMSJ9.4dkL0mW3Dn3Ghl4rp6VwkjMS_q7FLodJwb1fTGW7o-oCa33bm5F1XaWHDeLXwiuFAvUWLeOqGCFC08a7-LH6TyxcNgA2YnWBcMB7Dqy4XF4S1T5ujDYoWyrNvEbcYR3Sv0vjlG28eBAJxGv9AB5wNC8eeCAUb35MHY9iM0inwWUF-X0tG5leCSG-BitA2Vjl2SKLn_M7APTnDuEghrehn8jVGVFV7xHEveAop45tH_s.ZojNYtIzvhGswvJxQIxipQMmMr9r1reUKmYQyP5T3e0&dib_tag=se&keywords=Waveshare+UGV+Rover+Open-Source+beast&qid=1735342472&sprefix=waveshare+ugv+rover+open-source+beas%2Caps%2C222&sr=8-4)

- [Waveshare UGV Beast Open-Source Off-Road Tracked AI Robot for Jetson Orin Series Board, Dual Controllers, with Driver Boards and 360° Omnidirectional Pan-Tilt, No Include Jetson Orin Nano 4GB Kit](https://www.amazon.com/Waveshare-Open-Source-Off-Road-Controllers-Omnidirectional/dp/B0D9W5NNGL/ref=sr_1_5?crid=3A5TOSRQ6SVWV&dib=eyJ2IjoiMSJ9.4dkL0mW3Dn3Ghl4rp6VwkjMS_q7FLodJwb1fTGW7o-oCa33bm5F1XaWHDeLXwiuFAvUWLeOqGCFC08a7-LH6TyxcNgA2YnWBcMB7Dqy4XF4S1T5ujDYoWyrNvEbcYR3Sv0vjlG28eBAJxGv9AB5wNC8eeCAUb35MHY9iM0inwWUF-X0tG5leCSG-BitA2Vjl2SKLn_M7APTnDuEghrehn8jVGVFV7xHEveAop45tH_s.ZojNYtIzvhGswvJxQIxipQMmMr9r1reUKmYQyP5T3e0&dib_tag=se&keywords=Waveshare+UGV+Rover+Open-Source+beast&qid=1735342472&sprefix=waveshare+ugv+rover+open-source+beas%2Caps%2C222&sr=8-5)

- [Waveshare UGV Beast ROS 2 Open-Source Off-Road Tracked AI Robot, Dual Controllers, Computer Vision, All-Metal Body, Flexible and Expandable, Compatible with Raspberry Pi 5 (Included)](https://www.amazon.com/Waveshare-Open-Source-Controllers-Expandable-Compatible/dp/B0DJQD1V5R/ref=sr_1_6?crid=3A5TOSRQ6SVWV&dib=eyJ2IjoiMSJ9.4dkL0mW3Dn3Ghl4rp6VwkjMS_q7FLodJwb1fTGW7o-oCa33bm5F1XaWHDeLXwiuFAvUWLeOqGCFC08a7-LH6TyxcNgA2YnWBcMB7Dqy4XF4S1T5ujDYoWyrNvEbcYR3Sv0vjlG28eBAJxGv9AB5wNC8eeCAUb35MHY9iM0inwWUF-X0tG5leCSG-BitA2Vjl2SKLn_M7APTnDuEghrehn8jVGVFV7xHEveAop45tH_s.ZojNYtIzvhGswvJxQIxipQMmMr9r1reUKmYQyP5T3e0&dib_tag=se&keywords=Waveshare+UGV+Rover+Open-Source+beast&qid=1735342472&sprefix=waveshare+ugv+rover+open-source+beas%2Caps%2C222&sr=8-6)

- [Waveshare UGV Rover ROS 2 Open-Source 6 Wheels 4WD AI Robot, Compatible with Jetson Orin Nano/NX, Dual Controllers, with Multi-Functional Driver Board and 360° Flexible Omnidirectional Pan-Tilt](https://www.amazon.com/Open-Source-Compatible-Controllers-Multi-Functional-Omnidirectional/dp/B0DM4KBWT7/ref=sr_1_9?crid=3A5TOSRQ6SVWV&dib=eyJ2IjoiMSJ9.4dkL0mW3Dn3Ghl4rp6VwkjMS_q7FLodJwb1fTGW7o-oCa33bm5F1XaWHDeLXwiuFAvUWLeOqGCFC08a7-LH6TyxcNgA2YnWBcMB7Dqy4XF4S1T5ujDYoWyrNvEbcYR3Sv0vjlG28eBAJxGv9AB5wNC8eeCAUb35MHY9iM0inwWUF-X0tG5leCSG-BitA2Vjl2SKLn_M7APTnDuEghrehn8jVGVFV7xHEveAop45tH_s.ZojNYtIzvhGswvJxQIxipQMmMr9r1reUKmYQyP5T3e0&dib_tag=se&keywords=Waveshare+UGV+Rover+Open-Source+beast&qid=1735342472&sprefix=waveshare+ugv+rover+open-source+beas%2Caps%2C222&sr=8-9)

- [Waveshare UGV Beast ROS 2 Open-Source Off-Road Tracked AI Robot, Compatible with Jetson Orin Nano/NX, with 360° Flexible Omnidirectional Pan-Tilt, Includes Jetson Orin Nano 4GB Kit](https://www.amazon.com/Waveshare-Open-Source-Off-Road-Compatible-Omnidirectional/dp/B0DM8P7BM8/ref=sr_1_11?crid=3A5TOSRQ6SVWV&dib=eyJ2IjoiMSJ9.4dkL0mW3Dn3Ghl4rp6VwkjMS_q7FLodJwb1fTGW7o-oCa33bm5F1XaWHDeLXwiuFAvUWLeOqGCFC08a7-LH6TyxcNgA2YnWBcMB7Dqy4XF4S1T5ujDYoWyrNvEbcYR3Sv0vjlG28eBAJxGv9AB5wNC8eeCAUb35MHY9iM0inwWUF-X0tG5leCSG-BitA2Vjl2SKLn_M7APTnDuEghrehn8jVGVFV7xHEveAop45tH_s.ZojNYtIzvhGswvJxQIxipQMmMr9r1reUKmYQyP5T3e0&dib_tag=se&keywords=Waveshare+UGV+Rover+Open-Source+beast&qid=1735342472&sprefix=waveshare+ugv+rover+open-source+beas%2Caps%2C222&sr=8-11)

- [Waveshare Open-Source Off-Road Tracked AI Robot, Compatible with Raspberry Pi 5, Dual Controllers, Computer Vision, PI5-4GB NOT Included](https://www.amazon.com/Waveshare-Open-Source-Compatible-Raspberry-Controllers/dp/B0D3DNRTTF/ref=sr_1_18?crid=3A5TOSRQ6SVWV&dib=eyJ2IjoiMSJ9.4dkL0mW3Dn3Ghl4rp6VwkjMS_q7FLodJwb1fTGW7o-oCa33bm5F1XaWHDeLXwiuFAvUWLeOqGCFC08a7-LH6TyxcNgA2YnWBcMB7Dqy4XF4S1T5ujDYoWyrNvEbcYR3Sv0vjlG28eBAJxGv9AB5wNC8eeCAUb35MHY9iM0inwWUF-X0tG5leCSG-BitA2Vjl2SKLn_M7APTnDuEghrehn8jVGVFV7xHEveAop45tH_s.ZojNYtIzvhGswvJxQIxipQMmMr9r1reUKmYQyP5T3e0&dib_tag=se&keywords=Waveshare+UGV+Rover+Open-Source+beast&qid=1735342472&sprefix=waveshare+ugv+rover+open-source+beas%2Caps%2C222&sr=8-18)

---

## COVESA and VSS

Clone the VSS repo into the SDCard, example:

```console
root@fedora:# mount /dev/sdc3 /mnt/
root@fedora:# cd /mnt/home/douglas/
root@fedora:/mnt/home/douglas# git clone https://github.com/autosd-vss-mw/vss-lib.git
Cloning into 'vss-lib'...
remote: Enumerating objects: 974, done.
remote: Counting objects: 100% (81/81), done.
remote: Compressing objects: 100% (54/54), done.
remote: Total 974 (delta 27), reused 67 (delta 17), pack-reused 893 (from 1)
Receiving objects: 100% (974/974), 188.50 KiB | 1.41 MiB/s, done.
Resolving deltas: 100% (468/468), done.
root@fedora:~# umount /mnt 
```
## Contributions

Contributions are welcome! Please open an issue or submit a pull request if you want to enhance the module or add support for new devices.

---

## License

This repository is licensed under the **Apache License 2.0**. See the [LICENSE](LICENSE) file for details.

---

For questions or support, feel free to open an issue or contact the maintainer. 🚗✨
