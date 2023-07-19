# Palanca de cambios _(Shifter)_

![status](https://badgen.net/badge/Estado/Desarrollo de PCB/purple)

Esta PCB es la que tiene menos grado de dificultad de diseño, ya que solo tiene que 
leer la señal digital de sensores, estos pueden ser:

- Botones (Push, switches, interruptores, etc.)
- Efecto hall
- Cualquier otro que produzca señales en alto y bajo

Esta PCB solo contará con:

- Microcontrolador principal(con capacidades USB HID)
- 10 Entradas digitales una para cada marcha
- Puerto USB-C y RJ45

**Como aún no se a iniciado el diseño de esta PCB se estarán subiendo actualizaciones
aquí**

## Estado Actual

Decidí usar el microcontrolador RP2040, ya que como se menciona anteriormente
solo es necesario un MCU con capacidades HID y si se compara con el precio de algún 
MCU de la familia de Espressif, el RP2040 resulta considerablemente más barato.

Otro cambio realizado fue el de remover el puerto RJ45 por _"Pin Sockets"_, esto para
reducir el espacio.

Además se añaden 13 entradas para las marchas en vez de 10 entradas.

Por último se le da un formato de módulo a la PCB con el uso de _Castellated pins_ para
que en futuro pueda cambiarse este núcleo(esta PCB, ya que cuenta con el MCU), además
para que el RP2040 aproveche todos sus pines se agrega un puerto Mezzanine en la capa 
superior.

![shifter](./img/Shifter.png)
![shifter3D](./img/Shifter_.png)
