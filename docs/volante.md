# Steering Wheel PCB

![status](https://badgen.net/badge/Status/Development%20on%20hold,%20currently%20working%20on%20another%20aspect%20of%20the%20project/orange?icon=label)

This PCB has a medium to advanced level of difficulty because, in addition to acquiring data (digital or analog signals), it also needs to provide feedback by controlling an electric motor.

In the current market, there are three ways to provide feedback to the steering wheel:

- DD (Direct Drive)
- BD (Belt Drive)
- GD (Gear Drive)

[Here](https://kommandotech.com/guides/direct-vs-belt-vs-gear-drive/) you can find a comparison of the differences, advantages, and disadvantages of each of these methods. In summary, their names refer to how they transfer motion from the electric motor to the steering wheel.

**To make it as modular as possible, this PCB will be divided into two parts.**

## Data Acquisition
To obtain the steering wheel angle, some Hall effect sensor will be used as it offers an unlimited angle of rotation.

This PCB will only include:

- Main microcontroller (with USB HID capabilities)
- Analog input to obtain the steering wheel angle
- USB-C and RJ45 ports
- Output in some protocol to control the power stage

## Power Control
For controlling an electric motor, a power stage is necessary since the pins of a microcontroller cannot and should not be directly connected to a motor.

**Two PCBs will be designed:**

1. DC motor control (direct current)
2. Stepper motor control

**As the design of this PCB has not yet begun, updates will be posted here.**

## Current Status
