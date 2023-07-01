# PCB volante _(Steering Wheel)_

![status](https://badgen.net/badge/Estado/Desarrollo de PCB/purple)

Esta PCB tiene un grado de medio-avanzado de dificultad, ya que además de 
adquirir datos (señales digitales o analógicas), también necesita proporcionar 
retroalimentación _(Feedback)_ controlando un motor eléctrico.

En el mercado actual existe tres maneras de dar la retroalimentación al volante:

- DD (Direct Drive)
- BD (Belt Drive)
- GD (Gear Drive)

[Aquí](https://kommandotech.com/guides/direct-vs-belt-vs-gear-drive/)
se muestra las diferencias, ventajas y desventajas entre cada una de estas maneras,
en resumen su nombre hace referencia a como transfieren el movimiento desde el 
motor eléctrico hasta el volante.

**Para que sea lo más modular posible esta PCB estará dividida en dos partes**

## Adquisición de datos
Para obtener el ángulo del volante se usará algún sensor de efecto Hall, ya 
que ofrece un ángulo de giro ilimitado.

Esta PCB solo contará con:

- Microcontrolador principal (con capacidades USB HID)
- Entrada analógica para obtener el ángulo del volante
- Puerto USB-C y RJ45
- Salida en algún protocolo para controlar la etapa de potencia

## Control de potencia
Para el control de un motor eléctrico es necesario contar con una etapa de potencia,
ya que los pines de un Microcontrolador no pueden ni deben conectarse directamente a un
motor.

**Se diseñarán dos PCBs**

1. Control de un motor DC (corriente directa)

2. Control de un motor a pasos

**Como aún no se a iniciado el diseño de esta PCB se estarán subiendo actualizaciones
aquí**

## Estado Actual

