Otra de las funciones del Kernel es la de gestión de hardware. Cualquier dispositivo que se quiera comunicar con linux necesitara controladores, ahí es donde el kernel funciona como mediador. Dos métodos son utilizados para insertar el código de un controlador en el kernel de linux.

- Controladores compilados en el Kernel
- Módulos de controladores agregados al Kernel

Los módulos de Kernel se desarrollaron para poder insertar código de controladores aun con el Kernel corriendo, sin tener que compilar todo nuevamente.

Los sistemas Linux identifican los dispositivos de hardware como archivos especiales llamados `device files` hay 3 tipos de ellos

- Character
- Block
- Network

Character: archivos para dispositivos que solo pueden manejar un carácter a la vez. La mayoría de los modems y terminales son creados como `character files` 