# Interfaz de usuario _(GUI)_

Puedes visitar el [repositorio](https://github.com/janc18/CAE32)
para acceder a todos los recursos.

Para que sea más amigable y fácil para el usuario se crea una GUI en Gtk3 escrita en el 
**C**, la GUI sera capaz de:

- Vista en tiempo real el movimiento de los actuadores.
- Autoactualización de la GUI y de los microcontoladores cuando esto sea posible.
- Configuración de sensores como: límites, deadzone, etc.

La construcción de la GUI se realiza en un contenedor docker con Debian 11

## Estado actual

Por el momento se puede ver el movimiento actual de los pedales

![gui](./videos/output.gif)
