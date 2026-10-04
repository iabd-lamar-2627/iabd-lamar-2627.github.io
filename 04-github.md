# 4. Trabajar con GitHub

Ahora conectamos tu repositorio local con una copia en GitHub.

## Iniciar sesión desde tu ordenador

Para subir cosas, Git tiene que demostrar a GitHub que eres tú. La forma más sencilla es el **GitHub CLI**, que abre el navegador para que autorices.

=== "Windows"

    ```powershell
    winget install GitHub.cli
    ```

=== "macOS"

    ```bash
    brew install gh
    ```

    Sin Homebrew, descárgalo desde [cli.github.com](https://cli.github.com/).

=== "Linux"

    Sigue las instrucciones de [cli.github.com](https://cli.github.com/) para tu distribución.

Cierra y abre la terminal, y después:

```bash
gh auth login
```

Elige *GitHub.com*, protocolo **HTTPS**, y *Login with a web browser*. Copia el código que te muestra, pégalo en la página que se abre y autoriza.

Comprueba:

```bash
gh auth status
```

!!! note "En Windows, alternativa sin instalar nada más"
    Git para Windows incluye *Git Credential Manager*. La primera vez que hagas `git push` a un repositorio, abrirá una ventana del navegador para iniciar sesión.

## Caso A: ya existe un repositorio en GitHub → `clone`

Es el caso cuando el profesorado te ha creado el repositorio.

```bash
git clone https://github.com/ORGANIZACION/NOMBRE-DEL-REPO.git
cd NOMBRE-DEL-REPO
```

Copia la dirección desde el botón verde **Code** de la página del repositorio. Se descarga ya conectado a GitHub.

!!! info "Si ves un error 404"
    En los repositorios privados, GitHub responde 404 a quien no tiene acceso. Comprueba que has aceptado la **invitación** (llega a tu correo y a las notificaciones de GitHub) y que has iniciado sesión con la cuenta correcta.

## Caso B: tienes un repositorio local y quieres subirlo

1. En GitHub, crea un repositorio nuevo **vacío**: sin README, sin `.gitignore`, sin licencia. (Tu copia local ya los tiene.)
2. Conéctalo y súbelo:

```bash
git remote add origin https://github.com/TU-USUARIO/NOMBRE-DEL-REPO.git
git push -u origin main
```

`origin` es el nombre habitual del remoto. `-u` hace que la próxima vez baste con `git push`.

Alternativa con una sola orden (desde la carpeta del repositorio):

```bash
gh repo create NOMBRE-DEL-REPO --private --source=. --push
```

## El día a día

```bash
git status                     # qué ha cambiado
git add .                      # prepara los cambios
git commit -m "Qué he hecho"   # guarda la foto
git push                       # sube a GitHub
git pull                       # trae lo que haya nuevo en GitHub
```

!!! tip "Haz `git pull` antes de empezar a trabajar"
    Si trabajas desde dos ordenadores, o tienes compañeros en el mismo repositorio, empieza siempre por `git pull`.

## Comprobar que ha funcionado

Abre la página de tu repositorio en GitHub y recarga. Deben aparecer tus ficheros y, en *Commits*, tu mensaje.

Siguiente: [Problemas habituales](05-problemas.md)
