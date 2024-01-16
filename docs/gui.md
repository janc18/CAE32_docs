# User Interface _(GUI)_

You can visit the [repository](https://github.com/janc18/CAE32)
to access all the resources.

To make it more user-friendly and easy for the user, a GUI in Gtk3 is created, written in **C**. The GUI will be capable of:

- Real-time view of the actuator's movement.
- Auto-update of the GUI and microcontrollers whenever possible.
- Configuration of sensors such as limits, dead zone, etc.

The construction of the GUI is done in a Docker container with Debian 11.

## Current Status

As of January 15, 2024, the plan is to refactor the existing GUI to listen to a socket
connection for receiving stream data with the most updated values. Another application
will generate these values; it will be a low-level application written in C that will 
handle all communication with the device.
