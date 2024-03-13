# Jetson-Nano-RxTx-Gyro-from-STM32-with-LED
STM32 Roll and Pitch Indicator

# **Introduction**

The STM32 Roll and Pitch Indicator project aims to create a system that visually represents the roll and pitch of an STM32 development board using onboard LEDs. The roll and pitch angles, which determine the orientation of the device relative to the horizontal plane, are obtained from gyroscopic data collected by the STM32 board and transmitted over USB. A Python script running on a Jetson Nano single-board computer receives this data and controls the onboard LEDs accordingly, providing a real-time indication of the device's orientation.

# **Overview**

The system comprises two main components:

## **1.STM32 Firmware:** 
This component is responsible for collecting gyroscopic data from onboard sensors and transmitting it over USB to the Jetson Nano. The firmware is developed using STM32CubeIDE, an integrated development environment for STM32 microcontrollers. The firmware is configured to interface with the gyroscope sensor, read the roll and pitch angles, and format the data for transmission over USB.

## **2.Jetson Nano Python Script:** 
The Python script running on the Jetson Nano communicates with the STM32 board over USB to receive gyroscopic data. It parses the received data to extract the roll and pitch angles and then controls the onboard LEDs of the STM32 board to visually indicate these angles. The script utilizes the PySerial library for serial communication with the STM32 board.

# **Block Diagram**

The following block diagram illustrates the system architecture and data flow between the components:

.
.
.
.
.

# **Parameters**

Roll Angle: The angle of rotation around the longitudinal axis of the STM32 board, measured in degrees.
Pitch Angle: The angle of rotation around the lateral axis of the STM32 board, measured in degrees.
Instructions

# **To run the code:**

## **STM32 Firmware:**
Import the provided STM32 project into STM32CubeIDE.
Configure the project settings to enable USB communication and integrate the gyroscope sensor.
Flash the firmware onto the STM32 development board using STM32CubeIDE.
## **Jetson Nano Python Script:**
Ensure that Python 3 is installed on your Jetson Nano.
Install the necessary dependencies by running the following command in the terminal:

```pip install pyserial```

Run the Python script using the following command:

```python USB_gyro_example.py```

# **Results**

The system provides real-time indication of the roll and pitch angles of the STM32 development board through the onboard LEDs. As the orientation of the board changes, the LEDs adjust accordingly to reflect the current roll and pitch angles. This visual feedback allows users to monitor the orientation of the device and make informed decisions based on its position.

# **Outcome**

The STM32 Roll and Pitch Indicator project demonstrates the integration of gyroscopic data sensing and LED control to create a practical orientation indicator system. The project showcases the capabilities of microcontroller-based systems for sensor integration and real-time data processing. Additionally, the project serves as a foundation for further exploration into embedded systems development and sensor-based applications.

# **Dependencies**

## **PySerial:**
PySerial is a Python library used for serial communication. It provides support for accessing serial ports and communication with serial devices. Install PySerial using the following command:

```pip install pyserial```

## **STM32 Firmware:** 
The STM32 firmware provided in this project is required to enable USB communication and obtain gyroscopic data from the STM32 development board.

## **link to Code**
.
.
.

# **Table of Contents**

USB_gyro_example.py: This Python script controls the STM32 board and indicates the roll and pitch using onboard LEDs.

# **Credits**

The STM32 firmware was provided as part of the project materials.
PySerial library: PySerial
