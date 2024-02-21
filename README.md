# Smart Automated Irrigation System - LoRaWAN + AWS IoT Core

## Overview
This project aims to create a smart automated irrigation system using Arduino Edge Control equipped with various sensors to monitor environmental conditions. The system utilizes LoRaWAN for communication between the sensors and a central gateway, which then forwards data to AWS IoT Core. This setup allows for efficient water usage in agriculture by automating irrigation based on real-time data analysis.

This repository is made to provide a step-by-step guidance for developing an IoT Solution for smart irrigation using LoRaWAN technology and AWS IoT Services.

## Features
- Real-time soil moisture monitoring
- Temperature and humidity tracking
- Automated irrigation control based on sensor data
- Data analysis and monitoring through AWS IoT Core
- Scalable and secure data transmission with LoRaWAN

## Hardware Requirements
- Arduino Edge Control board
- Soil moisture sensor
- Temperature and humidity sensor
- LoRaWAN gateway
- Any additional sensors or actuators you plan to use

## Proposed Solution Architecture
<img width="452" alt="image" src="https://github.com/kaamiiaar/Automated-Irrigation-LoRaWAN/assets/47272408/4767bdc0-8307-4512-ab79-da911168f70b">


## Software Requirements
- Arduino IDE for programming the Arduino Edge Control
- AWS account for setting up AWS IoT Core and other services (e.g., Lambda, DynamoDB)

## Setup and Installation
### Hardware Setup
1. Connect the sensors to the Arduino Edge Control according to the wiring diagrams provided in the `diagrams` folder.
2. Ensure the LoRaWAN gateway is set up and connected to the internet.

### Software Setup
1. **Arduino Software**:
   - Install the Arduino IDE.
   - Use the provided sketches in the `arduino` folder to program your Arduino Edge Control.
   - Make sure to configure the LoRaWAN keys and settings as per your network provider.

2. **AWS IoT Core Configuration**:
   - Create a new thing in AWS IoT Core for your device.
   - Register your LoRaWAN gateway with AWS IoT Core for LoRaWAN.
   - Set up policies and certificates for secure communication.

### Running the Project
After setting up the hardware and software, deploy your system in the field. Use the AWS IoT Core console to monitor data and adjust the irrigation logic as needed.

## Usage
This section explains how to interact with the system, including any commands or scripts to run for testing or deployment.

## Acknowledgements
The Arduino code is sourced from Arduino documentation, while the AWS code is obtained from the AWS IoT - LoRaWAN Workshop materials.

## Contact
For any queries or further assistance, please contact kamyar1karimi@gmail.com

