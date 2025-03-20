# Bluetooth Controlled Car

## Overview
This project is a Bluetooth-controlled car that can be maneuvered using commands sent from a mobile device or another Bluetooth-enabled device. The car can move in different directions and adjust speed accordingly. Additionally, it includes headlight control.

## Components Required
- Arduino Uno
- Bluetooth Module (e.g., HC-05 or HC-06)
- Motor Driver Module (L298N or similar)
- DC Motors (2x)
- Power Supply (Battery pack)
- Jumper Wires

## Circuit Connections
### Motor Driver Connections:
- **Left Motor:**
  - Forward: Pin 7
  - Backward: Pin 8
  - Speed Control (PWM): Pin 5
- **Right Motor:**
  - Forward: Pin 9
  - Backward: Pin 10
  - Speed Control (PWM): Pin 6

### Headlight:
- **Headlight Control:** Pin 1

### Bluetooth Module:
- **TX to RX of Arduino**
- **RX to TX of Arduino**
- **VCC to 5V**
- **GND to GND**

## Code Explanation
- The car receives commands over Bluetooth via the serial interface.
- The `motor()` function controls the movement based on the received character command.
- The speed of the motors can be adjusted dynamically.
- Headlights can be turned on and off using specific commands.

### Bluetooth Commands:
| Command | Action |
|---------|--------|
| F       | Move Forward |
| B       | Move Backward |
| L       | Turn Left |
| R       | Turn Right |
| G       | Rotate Left |
| I       | Rotate Right |
| H       | Pivot Left |
| J       | Pivot Right |
| S       | Stop |
| U       | Turn Headlight On |
| u       | Turn Headlight Off |
| 0-9, q  | Adjust Speed (0 = Stop, q = Max Speed) |

## Installation and Usage
1. Connect all components as per the circuit diagram.
2. Upload the provided Arduino code to your Arduino board.
3. Pair your mobile device with the Bluetooth module.
4. Use a Bluetooth controller app to send commands to the car.
5. Control the car using the assigned commands.

## Troubleshooting
- **Car does not respond:** Ensure the Bluetooth module is paired and the correct serial port is selected.
- **Motors not working properly:** Check motor driver connections and ensure power supply is sufficient.
- **Speed control not working:** Verify that PWM pins are correctly wired.

## Future Improvements
- Implement an obstacle detection system using ultrasonic sensors.
- Add an app-based UI for easier control.
- Integrate a camera module for remote navigation.


