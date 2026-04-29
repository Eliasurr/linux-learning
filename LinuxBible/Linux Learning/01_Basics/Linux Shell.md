La shell de GNU/Linux es una utilidad interactiva especial. Proporciona una forma para que los usuarios inicien programas, gestionen archivos en el sistema y administren los procesos que se ejecutan en Linux. El núcleo de la shell es el **símbolo del sistema (command prompt)**. El prompt es la parte interactiva; te permite ingresar comandos de texto, los interpreta y luego los ejecuta en el kernel.

1. Comandos Internos vs. Externos
	- **Internos (Built-ins):** Son parte de la propia shell (como `cd` o `exit`). Son extremadamente rápidos porque no tiene que buscar un programa en el disco.
    
	- **Externos:** Son programas independientes instalados en tu Fedora (como `ls`, `grep` o `dnf`). La shell busca el archivo ejecutable en carpetas específicas (definidas en una variable llamada `$PATH`) y le pide al Kernel que lo abra.