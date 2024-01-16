# Device Simulation (HID)

To verify the functionality of the GUI on **Linux**, we make use of the [uinput](https://www.kernel.org/doc/html/v4.12/input/uinput.html) module, which can emulate input devices.

## Report Descriptors

A Report Descriptor is a character string used to define and classify the type of device that has just been connected.

**Example of a Report Descriptor data string**

```c
uint8_t hid_report_descriptor[] = {
    0x05, 0x01, /* USAGE_PAGE (Generic Desktop) */
    0x09, 0x04, /* USAGE (Joystick) */
    0xa1, 0x01, /* COLLECTION (Physical) */
    0x85, 0x01, /* REPORT_ID (1) */
    0x05, 0x09, /* USAGE_PAGE (Button) */
    0x19, 0x01, /* USAGE_MINIMUM (Button 1) */
    0x29, 0x08, /* USAGE_MAXIMUM (Button 3) */
    0x15, 0x00, /* LOGICAL_MINIMUM (0) */
    0x25, 0x01, /* LOGICAL_MAXIMUM (1) */
    0x95, 0x01, /* REPORT_COUNT (1) */
    0x75, 0x08, /* REPORT_SIZE (8) */
    0x81, 0x02, /* INPUT (Data,Var,Abs) */
    0x05, 0x01, /* USAGE_PAGE (Generic Desktop) */
    0x09, 0x30, /* USAGE (X) */
    0x09, 0x31, /* USAGE (Y) */
    0x09, 0x32, /* USAGE (Z) */
    0x09, 0x33, /* USAGE (Rx)*/
    0x15, 0x81, /* LOGICAL_MINIMUM(-129)*/
    0x25, 0x7f, /* LOGICAL_MAXIMUM(127)*/
    0x35, 0xc9, /* */
    0x45, 0xc8, /* */
    0x75, 0x08, /* REPORT_SIZE  (1)*/
    0x95, 0x04, /* REPORT_COUNT (4)*/
    0x81, 0x02, /* INPUT (Data,Var,Abs)*/
    0xc0        /* */
};
```

For more information on the meaning of each value, it is recommended to visit the [official USB HID documentation](https://www.usb.org/sites/default/files/documents/hid1_11.pdf)

Currently, the [TinyUSB](https://docs.tinyusb.org/en/latest/) library is available, which offers abstraction layers that make it easy to have a functional HID device quickly.
This library can easyly use with all the ESP-32 microcontroller family.

In the case of STM32 microcontrollers, STMicroelectronics provides its own library
for USB communication. 

## Device Descriptor Tester

As of today, January 15, 2024, an application is being developed for automated testing.
This application consists of a program that receives an input file with all the 
desired features of the device. The file is then parsed, and reading the device file
descriptor allows it to be compared with the input file. The application then 
returns a summary with all the test results
