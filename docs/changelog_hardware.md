
# Changelog (Lista de cambios)

## Pedales PCB

### Resultado (Versión 1)

![pedales_v2](./img/pcb_pedales_v1.png)

### Principales problemas con la Versión 1

1. Los conectores usados son difíciles de usar, requieren de un ensamble meticuloso
para que funcione correctamente.

2. Los botones usados para el **Reset** y **Boot** son muy pequeños, por lo que si se
usa un case, podrían ser de difícil acceso.

3. La Api **HAL** del MCU tiene problemas que aún no he podido resolver de manera 
correcta, estos están relacionados con la lectura analógica.

4. Los puertos para la depuración y programación no están distribuidos eficientemente.

5. Aunque tiene una resolución máxima de 14bits, tiene ruido que altera las lecturas
ocasionando una peor experiencia de juego.

6. Cuando se sube el nuevo firmware no se logra actualizar a menos de que se presionen
los botones físicamente.

### Solución de problemas para la Versión 1

1. Cambiar los conectores usados por unos _pin sockets_, y agregar una huella para soldar
directamente un cable, además de añadir la serigrafía necesaria.

2. Elegir botones más altos y acomodarlos en una zona de fácil acceso 

3. Usar la capa LL(Low Level) para tener un control más preciso de las lecturas 
analógicas

4. Acomodar los puertos a una zona más accesible, como a un costado, uno al lado del otro

5. Agregar un filtro por software

6. Conectar las entras de Reset y Boot al puerto rj45

### Mejoras (nuevos componentes agregados)

- Multiplexor de 8 canales con ADC 

- Hardware para 3 células de carga
	- Posible modelo de celda de carga [Aliexpress](https://es.aliexpress.com/item/1005004518830741.html)

- Añadir pines para conexión SPI y I2c

- USB tipo C

- Nuevo Microcontrolador más potente(Familia STM32F0), con soporte para conexión HID,
por lo que podría funcionar sin la placa principal

### Resultado (Versión 2)

![PCB V2](./img/Pedals3.png)



