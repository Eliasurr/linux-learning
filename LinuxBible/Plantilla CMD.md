# Comando: `nombre`

## 📋 Resumen
¿Para qué sirve en una frase? (Ej: "Busca patrones de texto en archivos").

## 🛠️ Flags Imprescindibles
- `-i`: Ignora mayúsculas/minúsculas.
- `-v`: Invierte la búsqueda (muestra lo que NO coincide).
- `-r`: Búsqueda recursiva en carpetas.

## 🚀 Ejemplos Reales (Probados en Fedora)
```bash
# Buscar la palabra "error" en los logs del sistema
grep -i "error" /var/log/messages