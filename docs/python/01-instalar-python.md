# 1. Instalar Python

!!! note "Versión"
    En clase se indicará la versión de Python que usamos. Si no se ha dicho otra cosa, instala **Python 3.12**.

## Comprobar si ya lo tienes

Abre una terminal (en Windows, *PowerShell*; en macOS, *Terminal*) y escribe:

=== "Windows"

    ```powershell
    py --version
    ```

=== "macOS / Linux"

    ```bash
    python3 --version
    ```

Si aparece algo como `Python 3.12.x`, ya lo tienes y puedes pasar a la [página siguiente](02-entorno-virtual.md). Si da error, o sale una versión muy distinta de la que se pide, instálalo así.

## Instalación

=== "Windows"

    1. Descarga el instalador desde [python.org/downloads](https://www.python.org/downloads/).
    2. Ábrelo y, **antes de pulsar nada más**, marca la casilla **Add python.exe to PATH**.
    3. Pulsa *Install Now*.
    4. Cierra la terminal y abre una nueva. Comprueba con `py --version`.

    Alternativa desde la terminal:

    ```powershell
    winget install Python.Python.3.12
    ```

=== "macOS"

    1. Descarga el instalador desde [python.org/downloads](https://www.python.org/downloads/) y ejecútalo.
    2. Abre una terminal nueva y comprueba con `python3 --version`.

    Si usas Homebrew:

    ```bash
    brew install python@3.12
    ```

=== "Linux (Ubuntu/Debian)"

    ```bash
    sudo apt update
    sudo apt install python3 python3-venv python3-pip
    python3 --version
    ```

    El paquete `python3-venv` es necesario para crear entornos virtuales.

## Comprobar que funciona

```bash
python3 -c "print('Hola desde Python')"
```

En Windows usa `py` en lugar de `python3`.

!!! warning "Un detalle de nombres"
    En Windows el comando habitual es `py` (o `python`). En macOS y Linux es `python3`. En el resto del mini-curso escribiremos `python`; sustitúyelo por el tuyo si hace falta. **Dentro de un entorno virtual activado, `python` funciona en los tres sistemas.**

Siguiente: [Entornos virtuales](02-entorno-virtual.md)
