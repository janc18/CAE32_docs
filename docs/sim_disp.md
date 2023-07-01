# Simulación de dispositivo (HID)

Para verificar el funcionamiento de la GUI, en **Linux** se hace uso del modulo
[uinput](https://www.kernel.org/doc/html/v4.12/input/uinput.html), el cual puede emular
dispositivos de entrada.

En el repositorio se encuentra código funcional con el cual se puede mostrar como 
interactua la GUI con el dispositivo, [aquí](https://github.com/janc18/CAE32/tree/main/Codigo/Device_simulation)
puedes encontrarlo

## _Report Descriptors_

Es una trama de caracteres usada para definir y clasificar el tipo de dispositivo
que se acaba de conectar.

**Ejemplo de una trama de datos de un Report Descriptor**

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
Para mayor información de el significado de cada valor es recomendable visitar la
siguiente documentación [aquí](https://www.usb.org/sites/default/files/documents/hid1_11.pdf).

Actualmente existe la librería [TinyUSB](https://docs.tinyusb.org/en/latest/), que ofrece
capas de abstracción con la que resulta sencillo tener un dispositivo HID funcional 
rapidamente.


