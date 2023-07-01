# PCB volante _(Steering Wheel)_

![status](https://badgen.net/badge/Estado/Desarrollo de PCB/purple)

Esta PCB creo que es la mas difícil en comparación con las demas ya que además de 
adquirir datos (señales digitales o analógicas), también necesita proporcionar 
retroalimentaciónn _(Feedback)_

En el mercado actual existe tres maneras de dar la retroalimentaciónn al volante:

- DD (Direct Drive)
- BD (Belt Drive)
- GD (Gear Drive)

[Aquí](https://kommandotech.com/guides/direct-vs-belt-vs-gear-drive/)
se muestra las diferencias, ventajas y desventajas entre cada una de estas formas,
en resumen su nombre hace referencia a como transfieren el movimiento desde el 
motor eléctrico hasta el volante

**Para que sea lo mas modular posible esta PCB estará dividida en dos partes**

## Adquisición de datos
Para obtener el ángulo del volante se usara algún sensor de efecto hall, debido a 
que ofrece un ángulo de giro inlimitado.

Esta PCB solo contara con:

- Microcontrolador principal
- Entrada analógica para obtener el ángulo del volante
- Puerto USB-C y RJ45
- Salida en algún protocolo para controlar la etapa de potencia

## Control de potencia
Para el control de un motor eléctrico es necesario contar con una etapa de potencia,
ya que los pines de un Microcontrolador no pueden ni debe conectarse directamente a un
motor.

**Se diseñaran dos PCBs**

1. Para control de un motor DC (corriente directa)

2. Para control de un motor a pasos

**Como aún no se a iniciado el diseño de es esta PCB se estarán subiendo actualizaciones
aqui**

## Estado Actual

