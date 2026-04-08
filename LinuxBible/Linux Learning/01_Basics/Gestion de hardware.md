Otra de las funciones del Kernel es la de gestión de hardware. Cualquier dispositivo que se quiera comunicar con linux necesitara controladores, ahí es donde el kernel funciona como mediador. Dos métodos son utilizados para insertar el código de un controlador en el kernel de linux.

- Controladores compilados en el Kernel
- Módulos de controladores agregados al Kernel

Los módulos de Kernel se desarrollaron para poder insertar código de controladores aun con el Kernel corriendo, sin tener que compilar todo nuevamente.

Los sistemas Linux identifican los dispositivos de hardware como archivos especiales llamados `device files` hay 3 tipos de ellos

- Character
- Block
- Network

**Character:** archivos para dispositivos que solo pueden manejar un carácter a la vez. La mayoría de los modems y terminales son creados como `character files`

**Block:**  archivos para dispositivos que pueden manejar una gran cantidad de informacion como pueden ser los discos rigidos. 

**Network:** archivos para dispositivos que paquetes para enviar y recibir información. Esto incluye a tarjetas de red y dispositivos loopback.

#### Dispositivo Loopback (`lo`)
Este es uno de los conceptos más importantes en redes.

- **¿Qué es?** Es una tarjeta de red virtual y "falsa" que vive dentro de tu memoria RAM.
    
- **¿Para qué sirve?** Permite que la computadora se hable a sí misma.
    
- **Ejemplo práctico:** Cuando un programador desarrolla una página web en su computadora y escribe `http://localhost` o `127.0.0.1` en el navegador, los datos no salen a Internet; pasan por el dispositivo de **loopback** para que el navegador y el servidor web (ambos en la misma máquina) se comuniquen.