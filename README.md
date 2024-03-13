# Jetson-Nano-RxTx-Gyro-from-STM32-with-LED
Introduction

The STM32 Roll and Pitch Indicator project aims to create a system that visually represents the roll and pitch of an STM32 development board using onboard LEDs. The roll and pitch angles are obtained from gyroscopic data collected by the STM32 board and transmitted over USB. A Python script running on a Jetson Nano single-board computer receives this data and controls the onboard LEDs accordingly, providing a real-time indication of the device's orientation.

Overview

The system comprises two main components:

STM32 Firmware: This component is responsible for collecting gyroscopic data from onboard sensors and transmitting it over USB to the Jetson Nano. The firmware is developed using STM32CubeIDE, an integrated development environment for STM32 microcontrollers. The firmware is configured to interface with the gyroscope sensor, read the roll and pitch angles, and format the data for transmission over USB.
Jetson Nano Python Script: The Python script running on the Jetson Nano communicates with the STM32 board over USB to receive gyroscopic data. It parses the received data to extract the roll and pitch angles and then controls the onboard LEDs of the STM32 board to visually indicate these angles. The script utilizes the PySerial library for serial communication with the STM32 board.

Block Diagram
The following block diagram illustrates the system architecture and data flow between the components:

Instructions

To run the code:
STM32 Firmware:
Import the provided STM32 project into STM32CubeIDE.
Configure the project settings to enable USB communication and integrate the gyroscope sensor.
Flash the firmware onto the STM32 development board using STM32CubeIDE.
Jetson Nano Python Script:
Ensure that Python 3 is installed on your Jetson Nano.
Install the necessary dependencies by running the following command in the terminal:
pip install pyserial

Run the Python script using the following command:
python USB_gyro_example.py

Dependencies

PySerial: PySerial is a Python library used for serial communication. It provides support for accessing serial ports and communication with serial devices. Install PySerial using the following command:
pip install pyserial

TM32 Firmware: The STM32 firmware provided in this project is required to enable USB communication and obtain gyroscopic data from the STM32 development board.

Table of Contents

USB_gyro_example.py: This Python script controls the STM32 board and indicates the roll and pitch using onboard LEDs.
