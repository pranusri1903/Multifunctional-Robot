# Autonomous and Bluetooth-Controlled Robot

## Overview
This project is an Arduino-based autonomous and Bluetooth-controlled robotic vehicle. It utilizes an ultrasonic sensor for obstacle detection, infrared sensors for human detection, and a Bluetooth module for remote control. The robot is equipped with four DC motors controlled via an Adafruit Motor Shield.

## Features
- **Bluetooth Control**: Navigate the robot using Bluetooth commands ('F', 'B', 'L', 'R', 'S').
- **Obstacle Avoidance**: Uses an ultrasonic sensor to detect and avoid obstacles.
- **Human Detection**: Employs IR sensors to detect human presence and react accordingly.
- **Servo-Controlled Directional Sensing**: Scans left and right before making navigation decisions.

## Components Used
- **Arduino Board**
- **Adafruit Motor Shield**
- **4 x DC Motors**
- **Ultrasonic Sensor (HC-SR04)**
- **IR Sensors**
- **Servo Motor**
- **Bluetooth Module (HC-05 or similar)**

## Setup and Wiring
1. Connect the **motor shield** to the Arduino.
2. Attach **DC motors** to the motor shield.
3. Connect the **ultrasonic sensor**:  
   - Trig → A3  
   - Echo → A4  
4. Connect the **IR sensors**:  
   - IR1 → A0  
   - IR2 → A1  
5. Attach the **servo motor** to pin 10.
6. Connect the **Bluetooth module** to the Arduino (if applicable).
7. Power the system with an external battery pack.

## Installation
1. Install the necessary libraries:
   ```cpp
   #include <Servo.h>
   #include <AFMotor.h>
   ```
2. Upload the provided Arduino sketch to your board using the Arduino IDE.
3. Open the Serial Monitor at 9600 baud rate to test commands.
4. Use a Bluetooth terminal app to send commands if using Bluetooth mode.

## Usage
### Bluetooth Commands:
- `F` → Move Forward
- `B` → Move Backward
- `L` → Turn Left
- `R` → Turn Right
- `S` → Stop
- `+` → Enable Obstacle Avoidance
- `*` → Enable Human Detection

## Functions Explained
- `ultrasonic()`: Measures distance using the ultrasonic sensor.
- `forward()`, `backward()`, `left()`, `right()`, `Stop()`: Basic movement functions.
- `Obstacle()`: Checks for obstacles and decides the best path.
- `human()`: Uses IR sensors to detect human presence and respond.
- `rightsee()`, `leftsee()`: Scans right and left for better navigation.

## Future Enhancements
- Integration with an **app-based controller**.
- Addition of a **camera module** for image processing.
- Implementation of **machine learning** for improved obstacle detection.

## License
This project is open-source under the MIT License.

## Author
Pranjal Srivastava

## Contribution
Feel free to submit pull requests or report issues via GitHub!

