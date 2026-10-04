# 5. Problemas habituales

## `git: command not found` / `git no se reconoce`

Git no está instalado o la terminal se abrió antes de instalarlo. Instálalo ([página 2](02-instalar-configurar.md)) y **abre una terminal nueva**.

## `Please tell me who you are` al hacer commit

Falta la configuración de identidad:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-correo@ejemplo.com"
```

## `fatal: not a git repository`

No estás dentro de un repositorio. Comprueba con `pwd` en qué carpeta estás y entra en la correcta con `cd`.

## `nothing to commit, working tree clean`

No hay cambios desde el último commit. Si esperabas verlos, comprueba que has **guardado** los ficheros en el editor.

## `git push` dice `Authentication failed` o `Permission denied`

1. Ejecuta `gh auth status`. Si no hay sesión, repite `gh auth login`.
2. Comprueba que usas la cuenta correcta de GitHub.
3. Si es un repositorio del curso, asegúrate de haber **aceptado la invitación**.

## Error 404 al clonar un repositorio

Casi siempre es una de estas dos cosas:

- No has aceptado la invitación al repositorio o a la organización.
- Has iniciado sesión con otra cuenta de GitHub.

Comprueba tu usuario con `gh auth status`.

## `error: failed to push some refs` / `rejected`

Hay cambios en GitHub que no tienes en tu ordenador. Haz:

```bash
git pull
git push
```

## `src refspec main does not match any`

Todavía no has hecho ningún commit, o tu rama se llama `master`. Comprueba:

```bash
git status
git log --oneline
```

Si no hay commits, hazlos primero ([página 3](03-primer-repositorio.md)).

## He subido por error un fichero que no debía

Avisa antes de hacer nada más, sobre todo si contiene contraseñas, claves o datos personales: borrarlo en un commit nuevo **no lo elimina del historial**.

## Antes de pedir ayuda

Prepara estas tres cosas:

1. El **mensaje de error completo** (texto copiado).
2. La salida de `git status`.
3. La salida de `git remote -v`.
