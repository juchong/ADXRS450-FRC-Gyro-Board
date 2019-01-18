## ***FRC TEAMS, BE AWARE THAT THE 2019 KICKOFF RELEASE IMAGE (v12) BREAKS COMPATIBILITY WITH ADI GYROS and IMUs! NI HAS RELEASED AN UPDATE SUITE (2019.1.0) ALONG WITH A NEW ROBORIO IMAGE (v13) THAT FIXES THE ISSUE. THE UPDATED INSTALLER CAN BE FOUND [HERE](http://www.ni.com/download/first-robotics-software-2017/7904/en/).***

# Analog Devices Gyro Board for FIRST Robotics
## A simple breakout board for interfacing the ADXRS450/ADXRS453 gyroscope with an FRC RoboRIO!

This repository is meant to document the development of the ADXRS450/453 donation board built by Analog Devices Inc. and donated to FIRST Robotics Competition teams. The gyro board incorporates a calibrated, single-axis yaw-rate sensor typically used in industrial and navigation applications. 

![2017 Gyro Board - Image courtesy of AndyMark Inc.](https://raw.githubusercontent.com/juchong/Analog-Devices-Gyro-Board/master/Documentation/2017/am-3555-2.jpg )

## Why isn't your example code working?
A bug was introduced in the 2019 kickoff RoboRIO image which broke "Auto SPI." All ADI sensors currently offered to FRC teams rely on this feature to synchronously capture IMU data and feed it to the Zynq CPU for processing. The source of the bug was traced back to a RoboRIO image packaging issue and could be temporarily resolved on a v12 image by connecting to the serial/SSH terminal on the RoboRIO and executing the command "updateNIDrivers". This command forces the RoboRIO to re-compile the affected kernel module and fully resolves the issue. As of 01/17/2019, NI has released an updated [installer](http://www.ni.com/download/first-robotics-software-2017/7904/en/) (2019.1.0) that includes a pre-patched RoboRIO image (v13).

## ADXRS450 Features:

- Complete rate gyroscope on a single chip
- ±300°/sec angular rate sensing (single axis Z)
- High vibration rejection over a wide frequency range
- Excellent 25°/hour null offset stability
- Internally temperature compensated
- 2000 g powered shock survivability
- SPI digital output with 16-bit data-word
- Low noise and low power
- 3.3 V and 5 V operation
- -40°C to +105°C operation
- Ultra-small, light, and RoHS compliant

## Gyro Board Features:

- Designed to easily interface with the SPI port on the RoboRIO
- Software support is built into the official WPILib software distribution 
- Java, C++, and LabVIEW are fully supported
- *New in 2019* - SPI CS solder jumper for compatibility with other SPI devices on the same bus

## Getting Started:

Looking to get started with the sensor? Check out the FRC getting started guides available on the [Analog Devces Wiki](https://wiki.analog.com/first)!

## Build Your Own:

Circuit boards can be purchased from OshPark in quantities as few as 3. Links to the 2017 and 2019 PCB versions are provided below.

- [2019 Gyro Board](https://oshpark.com/shared_projects/y65Hwywf)
- [2017 Gyro Board](https://oshpark.com/shared_projects/hwu7OKyt)

