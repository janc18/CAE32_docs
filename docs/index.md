# Welcome to CAE32 Documentation

You can visit the [repository](https://github.com/janc18/CAE32)
to access all the resources.

## CAE32

CAE32 is an open-source project under the [GPLv3 license](https://www.gnu.org/licenses/quick-guide-gplv3.html). It aims to provide all the necessary elements for enjoying simulation games with Open Source Hardware, Software, and Firmware, primarily in the automotive field, but it can be used for other areas as well.

## Components

- Hardware:
	- Pedals
	- Shifter (Gear Shift)
	- Steering Wheel
- Firmware
- GUI (GTK3)

## Hardware

<img src="./img/oshw-logo.svg" alt="drawing" width="200"/>

The Hardware for this project is Open Source Hardware. You can find all the related files for hardware development [here](https://github.com/janc18/CAE32/tree/main/Esquematicos/CAE32_PCB). The software used is [KiCad](https://www.kicad.org/).

The idea behind CAE32 hardware is to make it as modular as possible.

**Example**

- The PCB for the pedals can be used either with the main board or independently, as it has HID (Human Interface Device) capability.
- Peripherals (SPI, UART, CAN) are exposed for adding additional capabilities.

Visit the Hardware category for more information.

## Firmware

The Firmware is developed using the framework provided by the manufacturer:

- ESP-IDF
- STM32CubeIDE

Additionally, FreeRTOS is implemented in both for ease of programming.

Visit [here](./firmware.md) for more information.

## GUI

To intuitively configure each of the features, a GUI is created, making it relatively easy to modify the behavior of certain functions.

The GUI is built using the GTK3 framework and is specially designed to run on Linux.

