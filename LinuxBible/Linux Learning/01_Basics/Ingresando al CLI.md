Una forma de acceder a la CLI (Interfaz de Línea de Comandos) es sacar al sistema Linux del modo de escritorio gráfico y ponerlo en modo de texto. Esto no proporciona nada más que una simple shell en el monitor, justo como en los días previos a los escritorios gráficos. Este modo se llama **consola de Linux** porque emula los viejos tiempos de una terminal de consola cableada y es una interfaz directa con el sistema Linux.

Cuando el sistema Linux arranca, crea automáticamente varias **consolas virtuales**. Una consola virtual es una sesión de terminal que se ejecuta en la memoria del sistema Linux. En lugar de tener varias "terminales tontas" (dumb terminals) conectadas a la computadora, la mayoría de las distribuciones de Linux inician cinco o seis (o a veces incluso más) consolas virtuales a las que puedes acceder desde un solo teclado y monitor.

- **Consola Virtual (TTY):** Interfaz pura de texto, directa al sistema. Útil para emergencias.
    
- **Acceso:** `Ctrl + Alt + F(1-6)`.
    
- **Dato Pro:** Si el entorno gráfico de Fedora se congela, entra a una TTY, haz login y usa el comando `top` para matar el proceso que bloquea todo.
    

> **Dato curioso:** Se llaman "Virtuales" porque antes eran físicas. Hoy, tu teclado y monitor se "reparten" entre estas consolas según la combinación de teclas que presiones.

