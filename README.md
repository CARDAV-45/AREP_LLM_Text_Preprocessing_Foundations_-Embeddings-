# Embeddings y Preprocesamiento de Texto – LLMs desde Cero

- **Autor**: Carlos David Barrero Velasquez
- **Universidad**: Escuela Colombiana de Ingenieria Julio Garavito
- **Asignatura**: Arquitecturas Empresariales (AREP)
- **Fecha**: Febrero 2026

## Introducción

Un token es un número. Un embedding es un vector. La pregunta es: ¿por qué ese vector "significa" algo?

Porque durante el entrenamiento, el modelo ajusta esos vectores para predecir bien. Tokens que usan contextos similares terminan pareciéndose. Eso es significado.

## Qué se hace aquí

1. Cargamos un texto
2. Lo convertimos a tokens (números del 0 al 50k)
3. Hacemos ventanas deslizantes (para tener pares: entrada → siguiente token)
4. Generamos una tabla gigante de embeddings (50k × 768)
5. Vemos qué tan similares son entre sí
## Requisitos

- Python 3.x
- torch
- tiktoken

## Cómo lo corrí

1. Abrí `ch02.ipynb` en VS Code 
2. Ejecuté las celdas de arriba hacia abajo (o Run All)
3. Si falta algo, `pip install torch tiktoken`
4. Los outputs te muestran tokens, datasets, embeddings, tos celdas de arriba hacia abajo (o Run All)
3. Si falta algo, `pip install torch tiktoken`
4. Los outputs te muestran tokens, datasets, embeddings, todo

## El experimento

Variamos `max_length` y `stride` para ver cómo cambia:
- Cantidad de muestras de entrenamiento
- Cuánto se solapan los fragmentos
- El trade-off entre datos y redundancia

## Por qué importa

Sin embeddings, no hay LLMs.
Sin LLMs, no hay agentes que razonan.
Sin agentes buenos, la IA no escala.

Los embeddings son el bloque más fundamental. Por eso este notebook existe.
