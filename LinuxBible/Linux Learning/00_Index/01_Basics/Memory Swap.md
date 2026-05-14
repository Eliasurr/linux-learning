
**Gestión de Memoria Virtual**

Lo hace utilizando espacio en el disco duro, llamado **espacio de intercambio (swap)**. El núcleo (kernel) intercambia los contenidos de las ubicaciones de memoria virtual de un lado a otro, desde el espacio de swap hacia la memoria física real. Esto permite al sistema pensar que hay más memoria disponible de la que existe físicamente.

Las ubicaciones de memoria se agrupan en bloques llamados **páginas**. El kernel ubica cada página de memoria ya sea en la memoria física o en el espacio de swap. Luego, el kernel mantiene una tabla de páginas de memoria que indica qué páginas están en la memoria física y cuáles han sido enviadas al disco (swapped out).

El kernel rastrea qué páginas de memoria están en uso y copia automáticamente al espacio de swap aquellas que no han sido accedidas durante un tiempo (proceso llamado **swapping out**), incluso si hay otra memoria disponible

### Páginas (Pages)

El Kernel no mueve datos bit por bit, sería ineficiente. Divide la memoria en trozos de tamaño fijo llamados **Páginas** (normalmente de 4 KB). Es como organizar un almacén por cajas estándar en lugar de objetos sueltos.