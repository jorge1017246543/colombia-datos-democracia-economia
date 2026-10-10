# Extensión opcional: asociación entre medios informativos y voto

## Estado

Esta investigación aún **no** estima una relación individual entre usar redes sociales para informarse y reportar haber votado. La publicación agregada de la ECP no proporciona el cruce. El catálogo del DANE requiere completar el proceso de descarga web con CAPTCHA; no se automatiza ni se sortea.

## Descarga y privacidad

1. Abre el [catálogo de microdatos anonimizados ECP 2023 del DANE](https://microdatos.dane.gov.co/index.php/catalog/822/get-microdata).
2. Revisa la declaración de uso, resuelve el CAPTCHA y descarga las tablas necesarias: características generales, elecciones y partidos, democracia y, si se necesitan covariables, participación/capital social.
3. Descomprime los archivos localmente dentro de `data/raw/`. Conserva los archivos originales sin modificarlos.
4. **No subas** microdatos ni filas de personas a GitHub. El DANE advierte restricciones de reproducción y confidencialidad; consulta condiciones y autorización antes de compartir cualquier derivado.
5. Revisa diccionario, llaves de persona/hogar, ponderadores, estratos, conglomerados y coeficientes de variación de la ronda 2023. No reutilices nombres de variables de rondas anteriores.

## Análisis que debe ejecutarse después

1. Unir módulos mediante identificadores documentados; comprobar unicidad, cobertura del cruce, valores perdidos y población elegible.
2. Identificar en el diccionario el indicador de selección de redes y el indicador de voto presidencial 2022. Restringir el análisis de voto al universo elegible/inscrito que define el cuestionario.
3. Estimar proporciones ponderadas y diferencias en puntos porcentuales entre quienes seleccionaron redes y quienes no, incluyendo intervalos de confianza acordes al diseño complejo.
4. Si el tamaño y la documentación lo permiten, estimar regresión logística ponderada con covariables disponibles (edad, sexo, educación, región, área y otras justificadas), reportando razones de momios y efectos marginales con intervalos.
5. Hacer análisis de sensibilidad por edad, sexo y dominio geográfico; agrupar categorías solo con criterio sustantivo y precisión suficiente.
6. Presentar el resultado como **asociación ajustada**. Una encuesta transversal retrospectiva no elimina causalidad inversa, sesgo de recuerdo, selección de canal, confusión no medida ni error de medición.

## Supuestos y controles

- Una respuesta “redes sociales” no equivale a una medida de intensidad, plataforma específica, exposición a una publicación o persuasión.
- Un voto reportado en 2023 sobre una elección de 2022 puede tener error de recuerdo o deseabilidad social.
- “No seleccionó redes” no significa “no usa redes”; significa que no las seleccionó como canal de información política en ese ítem.
- Los pesos de expansión no corrigen por sí solos toda incertidumbre; se debe incorporar el diseño y documentar CV/intervalos.
- Si falta información de varianza o no es posible reconstruir el diseño, la salida se rotula exploratoria y no se presenta como estimación poblacional precisa.

