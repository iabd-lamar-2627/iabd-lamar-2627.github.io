# 4. VS Code y Jupyter

Instalar Python y crear el entorno no basta: VS Code tiene que saber **cuál** usar. Aquí es donde más veces falla, y casi siempre por lo mismo.

## Instalar VS Code y las extensiones

1. Descarga VS Code desde [code.visualstudio.com](https://code.visualstudio.com/).
2. Abre VS Code y ve a la pestaña de extensiones (`Ctrl+Shift+X`, o `Cmd+Shift+X` en macOS).
3. Instala **Python** y **Jupyter** (ambas de Microsoft).

## Abrir la carpeta del proyecto

*Archivo → Abrir carpeta…* y elige la carpeta donde creaste `.venv` (por ejemplo `curso-iabd`).

!!! tip "Abre la carpeta, no un fichero suelto"
    Si abres solo un fichero, VS Code no encuentra el entorno `.venv` que está junto a él.

## Elegir el intérprete

El **intérprete** es el Python que ejecutará tus scripts `.py`.

1. Pulsa `Ctrl+Shift+P` (`Cmd+Shift+P` en macOS).
2. Escribe **Python: Select Interpreter** y pulsa Enter.
3. Elige el que lleva `.venv` en su ruta.

## Elegir el kernel de un cuaderno

El **kernel** es el Python que ejecuta un cuaderno `.ipynb`. Se elige aparte del intérprete:

1. Abre un fichero `.ipynb`.
2. Arriba a la derecha pulsa **Select Kernel**.
3. Elige *Python Environments…* y después el que lleva `.venv`.

Si VS Code te propone instalar `ipykernel`, acepta. (Si instalaste las librerías de la [página 3](03-librerias-pip.md), ya lo tienes.)

## Probar que todo funciona

Crea un fichero `prueba.ipynb`, elige el kernel `.venv` y ejecuta esta celda con `Mayús+Enter`:

```python
import sys
print(sys.prefix)
```

La ruta debe terminar en `.venv`. Si es así, el entorno está bien montado.

## Terminal integrada

*Terminal → Nueva terminal.* Si el intérprete está bien elegido, la terminal activa `(.venv)` automáticamente. Si no aparece, actívalo a mano como en la [página 2](02-entorno-virtual.md).

## Intérprete y kernel: resumen

| Qué ejecutas | Qué eliges | Dónde |
|---|---|---|
| Scripts `.py` | Intérprete | `Ctrl+Shift+P` → *Python: Select Interpreter* |
| Cuadernos `.ipynb` | Kernel | Botón *Select Kernel* del cuaderno |

Siguiente: [Problemas habituales](05-problemas.md)
