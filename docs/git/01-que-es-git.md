# 1. Qué es Git

Git guarda **fotos del estado de tu proyecto** a lo largo del tiempo. Cada foto se llama **commit**.

Con ellos puedes:

- Volver a cómo estaba el proyecto hace una semana.
- Ver qué cambiaste y cuándo.
- Trabajar sin miedo a estropear algo que ya funcionaba.

## Las ideas que necesitas

| Término | Qué es |
|---|---|
| **Repositorio** | Una carpeta de proyecto a la que Git hace seguimiento |
| **Commit** | Una foto guardada del proyecto, con un mensaje que explica el cambio |
| **Working directory** | Tus ficheros tal como están ahora mismo |
| **Remoto** | La copia del repositorio que está en GitHub |
| **push** | Enviar tus commits a GitHub |
| **pull** | Traer a tu ordenador los commits que hay en GitHub |
| **clone** | Descargar un repositorio de GitHub por primera vez |

## El ciclo básico

```text
editas ficheros  →  git add  →  git commit  →  git push
```

1. Trabajas con normalidad.
2. Eliges qué cambios entran en la foto (`git add`).
3. Haces la foto con un mensaje (`git commit`).
4. Subes las fotos a GitHub (`git push`).

!!! tip "Un repositorio es una carpeta normal"
    Dentro hay una carpeta oculta llamada `.git` donde Git guarda el historial. No la toques ni la borres. En el explorador de archivos no verás nada distinto: es normal.

Siguiente: [Instalar y configurar](02-instalar-configurar.md)
