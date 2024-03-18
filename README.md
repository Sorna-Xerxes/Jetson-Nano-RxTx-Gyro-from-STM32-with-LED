# Jetson-Nano-RxTx-Gyro-from-STM32-with-LED

https://github.com/Sorna-Xerxes/Jetson-Nano-RxTx-Gyro-from-STM32-with-LED/assets/147555989/62ed350d-d964-43b5-94dd-c907737a6582


## INTRODUCTION
**Objective**: Visually represent roll, pitch, and yaw of an STM32 development board using onboard LEDs.
**Data Source**: Gyroscopic data collected by the STM32 board.
**Data Transmission**: Data transmitted over USB to a Jetson Nano.
**Data Processing**: Python script running on Jetson Nano receives and processes data.
**Control**: Python script dynamically controls onboard LEDs of the STM32.
**Real-time Feedback**: LEDs provide real-time indication of device orientation relative to the horizontal plane.

## SYSTEM OVERVIEW

### Hardaware Requirements:

**1. STM 32 F3 Discovery - Micro Controller**
The STM32F3 series microcontrollers are  commonly used in a wide range of embedded applications, including industrial automation, consumer electronics, and IoT devices. They are suitable for applications that require precise timing, sensor data acquisition, and control tasks.
- ARM Cortex-M4 core
- Onboard Sensors (MEMS Gyroscope, MEMS Accelerometer, e-Compass)
- lower processing power and are optimized for low power consumption 
- Integrated peripherals such as GPIO, UART, SPI, I2C, ADC, DAC, timers, and PWM controllers.

https://github.com/Sorna-Xerxes/Jetson-Nano-RxTx-Gyro-from-STM32-with-LED/assets/147555989/e3f29be0-a8b1-41d4-a662-0e4d1704ee91


**2. NVDIA Jetson Nano - Micro Processor**
The NVIDIA Jetson Nano is a small, powerful computer designed for AI and robotics applications. Jetson Nano is capable of running complex algorithms and deep learning models, making it suitable for tasks such as image recognition, object detection, and autonomous navigation.
- Quad-core ARM Cortex-A57 CPU with a NVIDIA Maxwell GPU.
- Various interfaces: USB, HDMI, Ethernet, CSI camera interface, and GPIO headers.

## Software Requirements:

### 1.STM32 Cube IDE:
Using STM32CubeIDE, an integrated development environment for STM32 microcontrollers, the firmware is developed to interface with the gyroscope sensor, collect data from onboard sensors, read the roll, pitch, and yaw angles, and transmit them over USB to the Jetson Nano.

### 2. Visual Studio Code:
Visual Studio Code connects to the NVIDIA Jetson Nano through a remote connection. The Python script running on the Jetson Nano communicates with the STM32 board over USB to receive gyroscopic data. It reads and parses the received data to extract the roll, pitch, and yaw angles, and then controls the onboard LEDs of the STM32 board to visually indicate these angles. The script utilizes the PySerial library for serial communication with the STM32 board.

# **Block Diagram**

The following block diagram illustrates the system architecture and data flow between the components:

. ![Alt text](Readme/ske.gif)
.
.
.
.

# **Parameters**

Roll Angle: The angle of rotation around the longitudinal axis of the STM32 board, measured in degrees.
Pitch Angle: The angle of rotation around the lateral axis of the STM32 board, measured in degrees.

# **Instructions**

To run the code:

## **STM32 Firmware:**
Import the provided STM32 project into STM32CubeIDE.
Configure the project settings to enable USB communication and integrate the gyroscope sensor.
Flash the firmware onto the STM32 development board using STM32CubeIDE.
## **Jetson Nano Python Script:**
Ensure that Python 3 is installed on your Jetson Nano.
Install the necessary dependencies by running the following command in the terminal:

```bash
pip install pyserial
```

Run the Python script using the following command:

```bash
python USB_gyro_example.py
```

# **Results**

The system provides real-time indication of the roll and pitch angles of the STM32 development board through the onboard LEDs. As the orientation of the board changes, the LEDs adjust accordingly to reflect the current roll and pitch angles. This visual feedback allows users to monitor the orientation of the device and make informed decisions based on its position.

# **Outcome**

The STM32 Roll and Pitch Indicator project demonstrates the integration of gyroscopic data sensing and LED control to create a practical orientation indicator system. The project showcases the capabilities of microcontroller-based systems for sensor integration and real-time data processing. Additionally, the project serves as a foundation for further exploration into embedded systems development and sensor-based applications.

# **Dependencies**

## **PySerial:**
PySerial is a Python library used for serial communication. It provides support for accessing serial ports and communication with serial devices. Install PySerial using the following command:

```bash
pip install pyserial
```

## **STM32 Firmware:** 
The STM32 firmware provided in this project is required to enable USB communication and obtain gyroscopic data from the STM32 development board.

## **link to Code**
.
.
.
.
# **Table of Contents**

USB_gyro_example.py: This Python script controls the STM32 board and indicates the roll and pitch using onboard LEDs.

# **Credits**

The STM32 firmware was provided as part of the project materials.
PySerial library: PySerial
