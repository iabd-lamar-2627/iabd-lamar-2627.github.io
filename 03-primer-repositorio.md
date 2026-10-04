# 3. Tu primer repositorio

Vamos a crear un repositorio **en tu ordenador** y hacer un commit. Todavía sin GitHub.

## Crear el repositorio

```bash
mkdir mi-primer-repo
cd mi-primer-repo
git init
```

`git init` crea la carpeta oculta `.git`. Desde ahora esta carpeta es un repositorio.

## El comando que más vas a usar: `git status`

```bash
git status
```

Te dice **qué ha cambiado desde el último commit**. Cuando tengas dudas, ejecútalo antes que ningún otro comando de Git.

## Crear ficheros

Crea un fichero de texto con el contenido que quieras:

=== "Windows (PowerShell)"

    ```powershell
    "# Mi primer repositorio" | Out-File -Encoding utf8 README.md
    ```

=== "macOS / Linux"

    ```bash
    echo "# Mi primer repositorio" > README.md
    ```

Añade también un `.gitignore` para que Git ignore lo que no debe guardar:

=== "Windows (PowerShell)"

    ```powershell
    ".venv/`n__pycache__/" | Out-File -Encoding utf8 .gitignore
    ```

=== "macOS / Linux"

    ```bash
    printf ".venv/\n__pycache__/\n" > .gitignore
    ```

Ejecuta `git status`: verás los dos ficheros en rojo como *Untracked files*. Git los ve pero todavía no los guarda.

## Preparar y guardar: `add` y `commit`

```bash
git add .
git commit -m "Primer commit"
```

- `git add .` marca **todo lo que ha cambiado** para la próxima foto.
- `git commit -m "..."` hace la foto. El mensaje debe explicar **qué** hiciste, en pocas palabras.

Ejecuta de nuevo `git status`: debe decir *nothing to commit, working tree clean*.

## Ver el historial

```bash
git log --oneline
```

Verás tu commit con un código corto, su mensaje y tu nombre.

## Resumen del ciclo

| Comando | Qué hace |
|---|---|
| `git status` | Qué ha cambiado |
| `git add .` | Prepara todos los cambios |
| `git commit -m "mensaje"` | Guarda la foto |
| `git log --oneline` | Muestra el historial |

Siguiente: [Trabajar con GitHub](04-github.md)
