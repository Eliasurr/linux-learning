El sistema operativo Linux llama **proceso** a un programa en ejecución. Un proceso puede ejecutarse en **primer plano (foreground)**, mostrando su salida en una pantalla, o en **segundo plano (background)**, tras bambalinas. El núcleo (kernel) controla cómo el sistema gestiona todos los procesos.

El kernel crea el primer proceso, llamado **init**, para iniciar todos los demás procesos. Cuando el kernel arranca, carga el proceso `init` en la memoria virtual. A medida que inicia cada proceso adicional, le asigna un área única en la memoria virtual para almacenar sus datos y código.

Algunas implementaciones de Linux contienen una tabla de procesos para iniciar automáticamente al arrancar. En sistemas Linux, esta tabla suele estar en el archivo especial `/etc/inittab`. Otros sistemas (como Ubuntu) utilizan la carpeta `/etc/init.d`, que contiene scripts para iniciar y detener aplicaciones

### 1. El Concepto de Proceso (El "DNI" del software)

En Linux, nada ocurre si no es a través de un proceso. Cada proceso tiene un **PID** (Process ID). El proceso `init` siempre es el **PID 1**. Es el "padre" de todos los procesos; si el PID 1 muere, el sistema entra en pánico (_Kernel Panic_).

### 2. Los Runlevels (Niveles de ejecución)

Piensa en los niveles de ejecución como "perfiles de energía" de un celular, pero para servicios:

- **Nivel 1:** Solo tú y la terminal (sin Internet, sin gráficos). Útil para rescatar archivos.
    
- **Nivel 3:** Modo multiusuario con red (servidores típicos).
    
- **Nivel 5:** Igual al 3, pero arranca la interfaz gráfica (GNOME en tu caso).
    
### 3. La evolución: SysVinit vs. systemd

El libro menciona `/etc/inittab` y `/etc/init.d`. En **Fedora**, esto ha sido reemplazado por `systemd`.

- **Antes:** Los procesos se iniciaban uno por uno (lento).
    
- **Ahora (systemd):** Los procesos se inician en paralelo (rápido) y se gestionan con el comando `systemctl`.

