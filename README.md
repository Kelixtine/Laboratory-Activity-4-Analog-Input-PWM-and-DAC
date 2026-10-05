# Laboratory Activity 4 – Analog Input, PWM, and DAC

**Course:** BCA152 – Microcontrollers
**Laboratory Activity:** No. 4
**Student Name:** Emmery Kelsey V. Mendoza

## Overview

This laboratory activity demonstrates the use of analog input, Pulse Width Modulation (PWM), and Digital-to-Analog Conversion (DAC) using an ESP32 microcontroller.

The project contains examples that demonstrate reading an analog signal from a potentiometer, controlling an LED using PWM, and generating DAC voltage levels with ADC verification.

## Objectives

* Understand analog input using the ESP32 ADC.
* Read analog values from a potentiometer.
* Control LED brightness using PWM.
* Understand PWM frequency and resolution.
* Generate analog voltage levels using the ESP32 DAC.
* Verify DAC output using an ADC reading.
* Observe sensor and output values through the Serial Monitor.

## Hardware and Components

* ESP32 Development Board
* Potentiometer
* LED
* Resistor
* Breadboard
* Jumper wires
* Connecting wires

## Software and Tools

* Visual Studio Code
* PlatformIO
* Arduino Framework
* ESP32 Development Platform
* Serial Monitor
* Git and GitHub

## Laboratory Exercises

### Example 3

`example3.cpp` is included in the project structure for the laboratory activity.

### Example 4 – PWM LED Control Using Potentiometer

This example reads an analog value from a potentiometer connected to **GPIO 34** and maps the 12-bit ADC reading to an 8-bit PWM duty cycle.

The LED is connected to **GPIO 19**. The PWM signal uses a frequency of **5 kHz** and an **8-bit resolution**, allowing the LED output to be controlled from 0 to 255.

The program also supports both ESP32 Arduino Core version 2.x and version 3.x or newer.

**Pin Configuration:**

| Component     | ESP32 Pin |
| ------------- | --------- |
| Potentiometer | GPIO 34   |
| LED           | GPIO 19   |

**Configuration:**

* ADC Resolution: 12-bit
* ADC Range: 0–4095
* PWM Frequency: 5 kHz
* PWM Resolution: 8-bit
* PWM Duty Range: 0–255
* Serial Baud Rate: 115200

### Example 5 – DAC Voltage Generation and ADC Verification

This example generates different DAC output levels through **GPIO 25** using the ESP32's built-in DAC.

The DAC values used are:

```text
0, 64, 128, 192, 255
```

The generated voltage is then verified through an ADC connected to **GPIO 34**. The measured voltage is displayed through the Serial Monitor.

**Pin Configuration:**

| Function         | ESP32 Pin |
| ---------------- | --------- |
| DAC Output       | GPIO 25   |
| ADC Verification | GPIO 34   |

**Configuration:**

* DAC Resolution: 8-bit
* ADC Resolution: 12-bit
* ADC Attenuation: 11 dB
* Serial Baud Rate: 115200

## Project Structure

```text
Laboratory-Activity-4-Analog-Input-PWM-and-DAC/
├── include/
├── lib/
├── src/
│   ├── example3.cpp
│   ├── example4.cpp
│   └── example5.cpp
├── test/
├── .gitignore
├── platformio.ini
├── README.md
└── documentation.mp4
```

## Documentation Video

[Watch the Documentation Video](./documentation.mp4)

## GitHub Repository

[View the GitHub Repository](https://github.com/Kelixtine/Laboratory-Activity-4-Analog-Input-PWM-and-DAC)

## Conclusion

This laboratory activity provided practical experience with the ESP32's analog and output capabilities. The exercises demonstrated analog input through a potentiometer, PWM-based LED control, and DAC voltage generation with ADC verification. These activities helped reinforce the relationship between digital values, analog signals, and microcontroller output control.
