# 2. Instalar y configurar

## Comprobar si ya tienes Git

```bash
git --version
```

Si muestra una versión, salta a *Configurar tu identidad*.

## Instalar

=== "Windows"

    1. Descarga el instalador desde [git-scm.com/download/win](https://git-scm.com/download/win).
    2. Acepta las opciones por defecto en todas las pantallas.
    3. Abre una terminal nueva y comprueba con `git --version`.

    Alternativa:

    ```powershell
    winget install Git.Git
    ```

=== "macOS"

    ```bash
    git --version
    ```

    Si Git no está instalado, macOS te ofrecerá instalar las *Command Line Tools*. Acepta.

    Con Homebrew: `brew install git`.

=== "Linux (Ubuntu/Debian)"

    ```bash
    sudo apt update
    sudo apt install git
    ```

## Configurar tu identidad

Git pone tu nombre y correo en cada commit. Se hace **una sola vez** por ordenador:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-correo@ejemplo.com"
git config --global init.defaultBranch main
```

!!! tip "Usa el mismo correo que en GitHub"
    Así GitHub asocia tus commits con tu cuenta. Si prefieres no mostrar tu correo, GitHub ofrece una dirección privada en *Settings → Emails*.

Comprueba lo guardado:

```bash
git config --global --list
```

## Crear tu cuenta de GitHub

1. Entra en [github.com](https://github.com/) y pulsa *Sign up*.
2. Elige un **nombre de usuario** que puedas enseñar con normalidad: aparecerá en tus repositorios.
3. Verifica tu correo.
4. Activa la verificación en dos pasos desde *Settings → Password and authentication*.

Anota tu nombre de usuario: tendrás que comunicarlo al profesorado para que te den acceso a los repositorios del curso.

Siguiente: [Tu primer repositorio](03-primer-repositorio.md)
