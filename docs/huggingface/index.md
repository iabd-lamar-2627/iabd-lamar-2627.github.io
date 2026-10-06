# Hugging Face

Hugging Face es una web donde cualquiera puede publicar modelos de IA ya entrenados, listos para probar sin instalar nada. Es el sitio de referencia para encontrar modelos de texto, imagen, voz o visión, y para las demos que usaremos en varias prácticas del curso.

## Qué tendrás al terminar

- Saber la diferencia entre un **modelo** y un **Space**.
- Saber buscar una demo por tarea (análisis de sentimiento, clasificación de imágenes...).
- Saber probarla sin instalar nada, directamente en el navegador.

## Modelo y Space no son lo mismo

| | Qué es | Cómo se usa |
|---|---|---|
| **Model** (`huggingface.co/<usuario>/<modelo>`) | El modelo en sí: sus pesos, su Model Card con los datos de entrenamiento y sus límites | Hace falta código (`pip install transformers`) para usarlo |
| **Space** (`huggingface.co/spaces/<usuario>/<demo>`) | Una pequeña aplicación (casi siempre Gradio) que ya usa un modelo por dentro | Se usa en el navegador: escribes texto o subes una imagen y ves el resultado |

Para las prácticas del curso, casi siempre usaréis un **Space**, no un Model.

## Buscar y probar un Space

1. Entra en `huggingface.co/spaces`.
2. Busca por tarea (categorías como Image Classification, Sentiment Analysis, Object Detection...).
3. Comprueba que esté marcado como **Running** (verde). Si pone *Sleeping*, *Paused* o *Runtime error*, prueba otro.
4. Escribe tu texto o sube tu imagen, y pulsa el botón de enviar (algunos responden solo al escribir).

!!! warning "No todos funcionan a la primera"
    Un Space es código subido por otra persona, no un servicio oficial de Hugging Face. Algunos tardan en cargar (sobre todo si el modelo corre dentro de tu propio navegador, puede pesar cientos de MB), otros están "dormidos" y tardan en despertar, y algunos están rotos sin más. Si uno no responde en medio minuto, prueba con otro antes de dar por hecho que el fallo es tuyo.

## Leer una Model Card

Cada modelo tiene una página (Model Card) con tres cosas que te interesan:

- **Datos**: con qué se entrenó (el dataset).
- **Modelo**: arquitectura y tamaño.
- **Límites**: para qué no sirve bien (sección "Risks, Limitations and Biases" o similar).

Saber leer esto es parte de entender un sistema de IA, no solo de usarlo.
