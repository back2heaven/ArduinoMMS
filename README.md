# Mini-Mobile Scout (MMS)

The **Mini-Mobile Scout (MMS)** is a four-wheeled remote-controlled vehicle designed to serve as a mobile threat detection and mapping system for environments that are hazardous or difficult to access. It was developed by the Advanced Vehicle Concepts Team (AVCT) as part of the EGR2800 course at Oakland University.

## 🔍 Project Summary

The MMS features a rotating ultrasonic sensor mounted on a turret that pans 150°, scanning for obstacles and displaying distances on an LCD. Controlled wirelessly using two Arduino Uno R4 Wi-Fi boards, the system splits its functionality into two major modules:

- **Input Board**: Acts as the user controller, sending joystick and button input to the output system via Arduino IoT Cloud.
- **Output Board**: Receives remote commands to control motors, steering, turret movement, and sensor data processing.

---

## 🧠 Project Goals

- Enable remote navigation and control of the MMS via joystick.
- Rotate the turret for real-time ultrasonic scanning.
- Display detected obstacle distances on an LCD.
- Split functionality between two microcontrollers connected through cloud services.

---

## 📂 Code Overview

This repository contains **two Arduino code folders**:

### 🔹 InputBoard
Location: `InputBoard/`

**Purpose**:  
Controls user input and transmits commands to the Output Board via Arduino Cloud. Connected directly to a computer and includes:

- Joystick module for vehicle direction control.
- Pushbutton to initiate turret scan.
- LCD screen to show obstacle distance in real time.
- Arduino Cloud variable handling (READ-only for joystick & button inputs, READWRITE for displaying distance).

**Key Functions**:
- Reads analog joystick data (A0, A1).
- Transmits button state for turret control.
- Receives distance data from OutputBoard and updates LCD display.

---

### 🔹 OutputBoard
Location: `OutputBoard/`

**Purpose**:  
Receives commands from Input Board to control all mechanical components of the MMS. Powered via battery, includes:

- Dual DC motors for movement (via L293D motor driver).
- Servo motor for steering.
- Stepper motor for turret rotation.
- Ultrasonic sensor for distance measurement.
- Sends measured distance back to Input Board for LCD display.

**Key Functions**:
- Implements pan function for turret (45° L/R).
- Converts ultrasonic sensor echo into cm.
- Drives vehicle movement and steering based on joystick values.
- Handles all component wiring and logic locally.

---

## 📡 Communication Model

The Input and Output Boards communicate via **Arduino IoT Cloud** over Wi-Fi. The Input board sends movement and control commands, while the Output board responds with sensor feedback. This architecture minimizes wiring complexity and enhances flexibility.

---

## ⚙️ Hardware Used

- (2) Arduino Uno R4 Wi-Fi Boards
- Joystick Module with pushbutton
- LCD Display
- Ultrasonic Sensor (HC-SR04)
- (2) 9V DC Brushed Motors
- L293D Motor Driver
- Stepper Motor (28BYJ-48) with ULN2003 Driver
- 25kg·cm Servo Motor
- 9V Batteries
- Custom 3D-Printed Chassis and Mounts

---

## 📌 Setup Instructions

1. Open each folder (`InputBoard/` and `OutputBoard/`) in the Arduino IDE.
2. Set up your Arduino Cloud dashboard and create corresponding variables:
   - Joystick X/Y
   - Button Press
   - Distance (read-only for Input)
3. Flash each program to its respective Uno R4 Wi-Fi board.
4. Power the OutputBoard via 9V batteries.
5. Connect the InputBoard to your PC for remote control.

---

## 🎯 Applications

- Military scouting and threat detection
- Warehouse and retail automation
- Customizable remote delivery or retrieval tasks
- Hobbyist mobile robot development


## 📜 License

This project is for academic purposes under Oakland University’s EGR2800 course. License to be determined by contributors.

