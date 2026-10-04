# Python y entorno de trabajo

Este mini-curso deja tu ordenador listo para programar en Python durante todo el curso. No enseña Python como lenguaje: enseña a **montar el entorno** donde vas a trabajar.

## Qué tendrás al terminar

- Python instalado y funcionando desde la terminal.
- Un **entorno virtual** (`.venv`) propio para cada proyecto.
- Las librerías básicas instaladas con `pip`.
- **VS Code** configurado para ejecutar scripts y cuadernos Jupyter dentro de ese entorno.

## Orden recomendado

1. [Instalar Python](01-instalar-python.md)
2. [Entornos virtuales](02-entorno-virtual.md)
3. [Librerías con pip](03-librerias-pip.md)
4. [VS Code y Jupyter](04-vscode-jupyter.md)
5. [Problemas habituales](05-problemas.md)

## Por qué un entorno virtual

Imagina que tienes una única cocina compartida por todos tus proyectos. Si un proyecto necesita una versión de una librería y otro necesita otra, se pisan. El entorno virtual es **una cocina separada por proyecto**: lo que instalas en uno no afecta a los demás ni a Python del sistema.

!!! tip "La regla que más tiempo ahorra"
    Antes de ejecutar `pip install` mira si ves **`(.venv)`** al principio de la línea de la terminal. Si no lo ves, el entorno no está activado y estás instalando en el sitio equivocado.
