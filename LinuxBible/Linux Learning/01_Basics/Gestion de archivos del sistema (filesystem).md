Linux crea archivos especiales, llamados **nodos**, para cada dispositivo en el sistema. Toda la comunicación con el dispositivo se realiza a través de su nodo de dispositivo. Cada nodo tiene un par de números único que lo identifica ante el núcleo (kernel) de Linux. El par de números incluye un **número de dispositivo mayor** y uno **menor**. Los dispositivos similares se agrupan bajo el mismo número mayor. El número menor se utiliza para identificar un dispositivo específico dentro del grupo mayor.

En Windows, sueles interactuar con el hardware a través de letras de unidad (`C:`, `D:`) o el Administrador de Dispositivos. En Linux, para hablar con un disco duro o una terminal, el sistema escribe datos en un archivo especial dentro de la carpeta `/dev/`.

### 1. ¿Dónde viven estos nodos?

Casi todos los nodos de dispositivo están en el directorio **`/dev/`** (abreviatura de _devices_).

- Tu disco principal suele ser `/dev/sda` o `/dev/nvme0n1`.
    
- Tu terminal actual es algo como `/dev/pts/0`.
### 2. El Par de Números (Major & Minor)

Piensa en esto como una **dirección postal**:

- **Major Number (Número Mayor):** Identifica el **driver** (controlador) necesario. Por ejemplo, todos los discos duros de un tipo específico podrían compartir el número 8. Le dice al Kernel: "Usa el manual de instrucciones para discos".
    
- **Minor Number (Número Menor):** Identifica la **unidad o partición específica**. Por ejemplo, dentro del grupo de discos, el número 1 es la primera partición, el 2 es la segunda, etc.
    
### 3. Tipos de Nodos
existen dos tipos principales que verás:

- **Character Devices (c):** Envían datos carácter por carácter (como tu teclado o el mouse).
    
- **Block Devices (b):** Envían datos en bloques grandes (como tu disco duro o un pendrive).


![[Pasted image 20260408162439.png]]

Cualquier unidad de almacenamiento que quiera instalarse linux deberá estar formateada usando uno los `filesystem` que se ven la imagen.