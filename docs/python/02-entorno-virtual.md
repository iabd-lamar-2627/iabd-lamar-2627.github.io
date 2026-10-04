# 2. Entornos virtuales

Un entorno virtual es una carpeta (`.venv`) que contiene su propia copia de Python y sus propias librerías.

## Paso 1: crear la carpeta del proyecto

Crea una carpeta para trabajar y entra en ella desde la terminal.

=== "Windows"

    ```powershell
    mkdir curso-iabd
    cd curso-iabd
    ```

=== "macOS / Linux"

    ```bash
    mkdir curso-iabd
    cd curso-iabd
    ```

!!! tip "Comprueba en qué carpeta estás"
    `pwd` te dice la carpeta actual (funciona en PowerShell, macOS y Linux). El entorno se crea **en la carpeta donde estás**, así que mira antes de crearlo.

## Paso 2: crear el entorno

=== "Windows"

    ```powershell
    py -m venv .venv
    ```

=== "macOS / Linux"

    ```bash
    python3 -m venv .venv
    ```

Verás que aparece una carpeta `.venv`. Solo se crea una vez por proyecto.

## Paso 3: activarlo

Esto hay que hacerlo **cada vez que abras una terminal nueva**.

=== "Windows (PowerShell)"

    ```powershell
    .venv\Scripts\Activate.ps1
    ```

=== "Windows (cmd)"

    ```bat
    .venv\Scripts\activate.bat
    ```

=== "macOS / Linux"

    ```bash
    source .venv/bin/activate
    ```

Sabrás que está activo porque la línea de la terminal empieza por **`(.venv)`**:

```text
(.venv) C:\Users\tu-nombre\curso-iabd>
```

!!! failure "Si en PowerShell sale un error rojo de «ejecución de scripts deshabilitada»"
    Ejecuta esto una sola vez y vuelve a activar:

    ```powershell
    Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
    ```

## Paso 4: comprobar que usas el Python del entorno

```bash
python -c "import sys; print(sys.prefix)"
```

La ruta que aparece debe terminar en `.venv`. Si no es así, el entorno no está activado.

## Desactivarlo

```bash
deactivate
```

## Qué guardar y qué no

La carpeta `.venv` **no se sube a Git** ni se copia a otros ordenadores: pesa mucho y depende de tu sistema. Lo que se comparte es la *lista* de librerías (lo verás en la [página 3](03-librerias-pip.md)) y, en Git, un fichero `.gitignore` que la excluye.

Siguiente: [Librerías con pip](03-librerias-pip.md)
