# 5. Problemas habituales

Busca tu síntoma. Casi todos tienen la misma causa: **el entorno no está activado o VS Code usa otro Python**.

## `No module named numpy` (o cualquier otra librería)

1. ¿Ves `(.venv)` en la terminal? Si no, actívalo ([página 2](02-entorno-virtual.md)) y repite `python -m pip install ...`.
2. En VS Code, ¿el intérprete o el kernel es el de `.venv`? Compruébalo ([página 4](04-vscode-jupyter.md)).
3. Ejecuta `python -c "import sys; print(sys.prefix)"` en el sitio donde falla. Si la ruta no acaba en `.venv`, usas otro Python.

## `python` o `py` no se reconoce como comando

- **Windows:** reinstala Python marcando *Add python.exe to PATH* y abre una terminal nueva.
- **macOS / Linux:** usa `python3`, no `python`, mientras no tengas el entorno activado.

## En PowerShell: «la ejecución de scripts está deshabilitada»

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

Después vuelve a activar el entorno.

## En Ubuntu/Debian: `ensurepip is not available` al crear el entorno

```bash
sudo apt install python3-venv
```

## No aparece `.venv` en la lista de intérpretes de VS Code

- ¿Abriste la **carpeta** del proyecto (no un fichero suelto)?
- Pulsa *Enter interpreter path…* → *Find…* y navega a `.venv/Scripts/python.exe` (Windows) o `.venv/bin/python` (macOS/Linux).
- Si acabas de crear el entorno, ejecuta *Developer: Reload Window* desde `Ctrl+Shift+P`.

## El cuaderno no encuentra el kernel o pide instalar algo

Con el entorno activado:

```bash
python -m pip install ipykernel
```

Y vuelve a elegir el kernel en el cuaderno.

## Creé el entorno en la carpeta equivocada

Borra la carpeta `.venv` y vuelve a crearla desde la carpeta correcta. No pasa nada: un entorno virtual es desechable.

## Antes de pedir ayuda

Prepara estas tres cosas. Con ellas se resuelve casi todo en un minuto:

1. El **mensaje de error completo** (copia el texto, no una foto recortada).
2. La salida de `python -c "import sys; print(sys.prefix)"`.
3. Qué sistema operativo usas.
