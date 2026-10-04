# 3. Librerías con pip

`pip` es el gestor de paquetes de Python. Descarga librerías desde [PyPI](https://pypi.org/) (el repositorio oficial) e instala también las que esa librería necesita.

!!! warning "Antes de cualquier `pip install`"
    Comprueba que ves **`(.venv)`** al principio de la línea. `pip install` solo afecta al entorno que está activo. Sin `(.venv)`, instalas en el Python del sistema y luego aparece el típico error *No module named ...* dentro de VS Code.

## Instalar las librerías básicas

Con el entorno activado:

```bash
python -m pip install --upgrade pip
python -m pip install numpy pandas matplotlib ipykernel
```

Escribimos `python -m pip` en vez de solo `pip` porque así nos aseguramos de usar el `pip` del Python que está activo.

| Librería | Para qué |
|---|---|
| `numpy` | Cálculo numérico con arrays |
| `pandas` | Tablas de datos |
| `matplotlib` | Gráficas |
| `ipykernel` | Permite ejecutar cuadernos Jupyter en este entorno |

## Comprobar la instalación

```bash
python -c "import numpy, pandas, matplotlib; print('Todo correcto')"
```

## Comandos útiles

```bash
python -m pip list                  # librerías instaladas en este entorno
python -m pip show numpy            # versión y datos de una librería
python -m pip install pandas==2.2.3 # una versión concreta
python -m pip uninstall pandas      # desinstalar
```

## Compartir tu entorno: `requirements.txt`

Cuando trabajes en equipo necesitaréis que el entorno de un compañero sea igual al tuyo. Para eso se guarda la lista de librerías:

```bash
python -m pip freeze > requirements.txt
```

Y quien reciba el proyecto la instala de golpe, en su propio entorno activado:

```bash
python -m pip install -r requirements.txt
```

!!! note "Para más adelante"
    No hace falta usar `requirements.txt` el primer día. Lo necesitarás cuando empiecen los trabajos en equipo.

Siguiente: [VS Code y Jupyter](04-vscode-jupyter.md)
