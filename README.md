# Web de mini-cursos · IABD · IES La Mar

Código fuente de https://iabd-lamar-2627.github.io/

El contenido está en `docs/` en markdown. MkDocs Material lo convierte en web.

## Probar en local

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\Activate.ps1
pip install -r requirements.txt
mkdocs serve                     # abre http://127.0.0.1:8000
```

## Publicar

Cada `git push` a `main` ejecuta `.github/workflows/deploy.yml`, que reconstruye la web y la sube a la rama `gh-pages`.

Primera vez: en el repositorio, *Settings → Pages → Build and deployment → Source: Deploy from a branch → `gh-pages` / `(root)`*.

## Añadir un mini-curso

1. Crea `docs/<nombre>/` con un `index.md` y las páginas.
2. Añade su bloque en `nav:` de `mkdocs.yml`.
3. Añade su enlace en `docs/index.md` y en el README de la organización (`profile/README.md` del repositorio `.github`).

## Qué NO va aquí

Este repositorio es público. Nada de soluciones, rúbricas, exámenes ni datos del alumnado.
