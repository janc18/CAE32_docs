# Gear Shift _(Shifter)_

![status](https://badgen.net/badge/Status/PCB Development/purple)

This PCB has the least degree of design complexity since it only needs to read the digital signal from sensors, which can be:

- Buttons (Push, switches, toggles, etc.)
- Hall effect sensors
- Any others that produce high and low signals

This PCB will only include:

- Main microcontroller (with USB HID capabilities)
- 10 digital inputs, one for each gear
- USB-C port and RJ45 port

**As the design for this PCB has not yet started, updates will be posted here.**

## Current Status

I decided to use the RP2040 microcontroller, as mentioned earlier, since only an MCU with HID capabilities is required. When compared to the price of any MCU from the Espressif family, the RP2040 is considerably cheaper.

Another change made was to replace the RJ45 port with "Pin Sockets" to reduce space.

Additionally, 13 inputs for the gears are added instead of 10 inputs.

Lastly, the PCB is given a module format with the use of castellated pins so that this core (this PCB, as it contains the MCU) can be changed in the future. Furthermore, to make the RP2040 utilize all its pins, a Mezzanine port is added to the top layer.

![shifter](./img/Shifter.png)
![shifter3D](./img/Shifter_.png)
