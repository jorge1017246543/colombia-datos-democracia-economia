# Guía para aprender con el proyecto

Este proyecto está pensado para que puedas explicar cada decisión en una entrevista y construirlo por etapas.

## Ruta sugerida

### 1. Entender la pregunta

Lee la [pregunta de negocio](metodologia_es.md) y separa sus dimensiones: comunicación política, participación, opinión, demografía y economía. No intentes unirlas en una sola métrica.

### 2. Leer las fuentes

Abre los boletines y el [diccionario](diccionario_datos.md). Para cada número, responde:

- ¿Quién integra la población de referencia?
- ¿A qué año o periodo corresponde?
- ¿La respuesta era única o múltiple?
- ¿Es un autorreporte, un conteo administrativo o un indicador macro?

### 3. Practicar con pandas

En el notebook, filtra una fuente, inspecciona sus columnas y compara dos periodos. La diferencia entre porcentajes se expresa en **puntos porcentuales**: pasar de 55% a 62,9% son 7,9 p.p. El crecimiento relativo sería otra operación.

### 4. Contar el resultado con una visualización

En el dashboard, activa o desactiva canales en la leyenda; cambia el indicador económico; filtra una región en la matriz de razones para no votar. Anota qué insight aparece y qué no se puede concluir.

### 5. Explicar los límites

Una asociación entre canal e intención/voto no prueba que el canal causó el resultado. Para el siguiente paso, estudia ponderadores, diseño de encuesta, intervalos de confianza y modelos logísticos antes de usar microdatos. La [guía de microdatos](microdata_extension.md) detalla los pasos.

## Habilidades que puedes mencionar en LinkedIn o entrevistas

- Descomposición de una pregunta de negocio en preguntas analíticas.
- Curaduría, limpieza y documentación de fuentes oficiales.
- Interpretación de denominadores, respuestas múltiples y diferencias en puntos porcentuales.
- Segmentación descriptiva por regiones y dominios territoriales.
- Visualización interactiva con filtros y leyendas.
- Comunicación ejecutiva y límites de inferencia.

