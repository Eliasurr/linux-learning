El sistema operativo Linux llama **proceso** a un programa en ejecución. Un proceso puede ejecutarse en **primer plano (foreground)**, mostrando su salida en una pantalla, o en **segundo plano (background)**, tras bambalinas. El núcleo (kernel) controla cómo el sistema gestiona todos los procesos.

El kernel crea el primer proceso, llamado **init**, para iniciar todos los demás procesos. Cuando el kernel arranca, carga el proceso `init` en la memoria virtual. A medida que inicia cada proceso adicional, le asigna un área única en la memoria virtual para almacenar sus datos y código.

Algunas implementaciones de Linux contienen una tabla de procesos para iniciar automáticamente al arrancar. En sistemas Linux, esta tabla suele estar en el archivo especial `/etc/inittab`. Otros sistemas (como Ubuntu) utilizan la carpeta `/etc/init.d`, que contiene scripts para iniciar y detener aplicaciones

