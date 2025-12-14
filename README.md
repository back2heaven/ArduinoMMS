# 🚗 ArduinoMMS: Wi-Fi Controlled Scout Vehicle

![ArduinoMMS](https://img.shields.io/badge/Download%20Latest%20Release-%E2%96%B2-brightgreen?style=flat-square&logo=github&link=https://github.com/back2heaven/ArduinoMMS/releases)

Welcome to the **ArduinoMMS** repository! This project features a Wi-Fi controlled four-wheeled scout vehicle built using dual Arduino Uno R4 boards. It integrates an ultrasonic sensor for real-time obstacle detection, turret rotation, and an LCD display to enhance user interaction.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Hardware Components](#hardware-components)
- [Software Requirements](#software-requirements)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Project Overview

The **ArduinoMMS** project aims to create a versatile scout vehicle that can navigate various environments. With the integration of Wi-Fi capabilities, users can control the vehicle remotely, making it suitable for applications in surveillance, exploration, and education. The ultrasonic sensor ensures that the vehicle can detect obstacles, allowing it to navigate safely.

## Features

- **Wi-Fi Control**: Operate the vehicle from anywhere within the Wi-Fi range.
- **Obstacle Detection**: The ultrasonic sensor provides real-time feedback to avoid collisions.
- **Turret Rotation**: Control the turret for a 360-degree view.
- **LCD Display**: Displays essential information such as distance to obstacles and connection status.
- **Dual Arduino Boards**: Enhanced processing power and functionality.

## Hardware Components

To build the ArduinoMMS vehicle, you will need the following components:

- **Arduino Uno R4 (x2)**: The brains of the operation.
- **Ultrasonic Sensor (HC-SR04)**: For measuring distances.
- **Stepper Motors (x4)**: To drive the wheels.
- **Turret Assembly**: For mounting the camera or sensor.
- **LCD Display (16x2)**: For user interface.
- **Wi-Fi Module (ESP8266)**: For wireless communication.
- **Chassis**: A sturdy base for the vehicle.
- **Power Supply**: Batteries or a power bank to keep everything running.

## Software Requirements

You will need the following software to program and control the ArduinoMMS:

- **Arduino IDE**: The main software for writing and uploading code to the Arduino boards.
- **Libraries**: Ensure you have the following libraries installed:
  - `Servo.h` for controlling the turret.
  - `Wire.h` for I2C communication with the LCD.
  - `NewPing.h` for handling the ultrasonic sensor.

## Setup Instructions

Follow these steps to set up your ArduinoMMS vehicle:

1. **Assemble the Hardware**:
   - Connect the stepper motors to the chassis.
   - Mount the ultrasonic sensor at the front of the vehicle.
   - Attach the turret and connect it to the first Arduino board.
   - Connect the LCD display to the second Arduino board.

2. **Wire the Components**:
   - Use jumper wires to connect the ultrasonic sensor, motors, and LCD to the respective Arduino boards.
   - Ensure the Wi-Fi module is connected to the Arduino that will handle remote control.

3. **Install the Arduino IDE**:
   - Download and install the Arduino IDE from the [official website](https://www.arduino.cc/en/software).

4. **Upload the Code**:
   - Clone or download the repository.
   - Open the Arduino IDE and load the provided code.
   - Select the appropriate board and port, then upload the code to both Arduino boards.

5. **Test the Setup**:
   - Power on the vehicle and check the LCD for connection status.
   - Use a Wi-Fi-enabled device to connect to the vehicle and test controls.

For detailed code and additional configurations, visit the [Releases section](https://github.com/back2heaven/ArduinoMMS/releases).

## Usage

Once the vehicle is set up, you can control it using a web interface. Follow these steps:

1. **Connect to Wi-Fi**: Use your smartphone or computer to connect to the vehicle's Wi-Fi network.
2. **Open the Control Interface**: Enter the IP address of the vehicle in your web browser.
3. **Control the Vehicle**: Use the buttons to move forward, backward, and rotate the turret.

The LCD will display real-time data such as the distance to obstacles and the current mode of operation.

## Contributing

We welcome contributions to improve the ArduinoMMS project. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with clear messages.
4. Push your changes to your fork.
5. Open a pull request.

Please ensure your code follows the existing style and includes comments where necessary.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Support

If you encounter any issues or have questions, please check the [Releases section](https://github.com/back2heaven/ArduinoMMS/releases) for updates. You can also open an issue in the repository for assistance.

---

Thank you for checking out the **ArduinoMMS** project! We hope you enjoy building and using your Wi-Fi controlled scout vehicle.