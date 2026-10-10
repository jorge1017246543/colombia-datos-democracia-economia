# Colombia en datos: democracia, conversación digital y economía

**Análisis de datos · Corte de investigación: 8 de octubre de 2026**

Un proyecto educativo de analítica de datos que integra indicadores oficiales del DANE y la Registraduría para estudiar fuentes de información política, participación, opinión pública, demografía y economía reciente en Colombia. Incluye un dashboard interactivo, datos agregados con trazabilidad y una guía para ampliar el análisis con microdatos sin publicar filas individuales.

> **Pregunta de investigación:** ¿Qué patrones describen la evolución de las fuentes de información política, la participación y las percepciones democráticas en Colombia, y cómo se leen junto con el contexto demográfico y económico más reciente?

## Explora el proyecto

- [Abrir dashboard interactivo](index.html)
- [Hallazgos iniciales](docs/hallazgos_es.md)
- [Diseño analítico](docs/metodologia_es.md)
- [Marco cualitativo](docs/metodo_cualitativo_es.md)
- [Diccionario de datos](docs/diccionario_datos.md)
- [Guía de aprendizaje](docs/guia_de_aprendizaje_es.md)
- [Extensión con microdatos](docs/microdata_extension.md)
- [Manifiesto de fuentes](data/sources.csv)
- [English README](README.en.md)

## Resumen ejecutivo

- Entre las personas que sí se informan de actualidad política, el uso reportado de redes sociales creció de **55,0% en 2021 a 62,9% en 2023**; la televisión continuó como canal más citado (**87,9% en 2023**).
- En la ECP 2023, **89,5% de las personas inscritas** reportó haber votado en las presidenciales de 2022. La participación oficial de la segunda vuelta fue **58,17% del censo electoral**; son medidas con denominadores y métodos distintos.
- En los periodos comparables seleccionados, el crecimiento anual del PIB en Q2 fue **2,1%, 2,1% y 3,5%** (2024–2026); el IPC anual de septiembre **5,81%, 5,18% y 6,29%**; y la desocupación de agosto **9,7%, 8,6% y 9,4%**.
- Los datos disponibles respaldan descripciones y asociaciones potenciales, pero **no** prueban que las redes hayan causado una decisión de voto o una opinión.

## Qué demuestra este portafolio

- Traducción de una pregunta de negocio a preguntas analíticas medibles.
- Selección, documentación y contraste de fuentes oficiales.
- Limpieza y estructuración de indicadores agregados en tablas CSV trazables.
- Definición de población, unidad de análisis, frecuencia y denominadores.
- Análisis comparativo y segmentación descriptiva por región y área.
- Visualización interactiva y accesible en HTML, SVG y JavaScript sin librerías externas.
- Síntesis cualitativa de metodología, literatura y límites de inferencia.
- Comunicación de hallazgos con lenguaje neutral y recomendaciones de análisis posterior.

## Cómo abrir y reproducir

El dashboard publicado es un archivo estático y puede abrirse directamente como `index.html`. Para regenerarlo con los CSV del repositorio se requiere Python 3.10 o superior:

```bash
python src/build_dashboard.py
```

La construcción del dashboard usa únicamente la biblioteca estándar de Python. El notebook de aprendizaje es opcional; para usarlo, instala las dependencias:

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_exploracion_colombia.ipynb
```

El workflow de GitHub Actions en `.github/workflows/pages.yml` publica el dashboard como sitio de GitHub Pages cuando este repositorio esté creado y habilitado para Pages.

## Estructura

```text
data/
  processed/        # Resúmenes oficiales agregados listos para explorar
  raw/              # Vacía en Git; microdatos locales no se versionan
  sources.csv       # Catálogo de fuentes, periodo y notas de acceso
docs/               # Hallazgos, metodología, lectura cualitativa y guía de datos
notebooks/          # Recorrido de aprendizaje en pandas y Plotly
src/                # Generador reproducible del dashboard
index.html          # Dashboard interactivo autocontenido
```

## Alcance y limitaciones

La cultura política se observa principalmente con la ECP 2023 (y comparaciones publicadas 2019/2021/2023); el contexto económico se actualiza hasta Q2 2026 para el PIB, septiembre 2026 para IPC y agosto 2026 para empleo. Los periodos no coinciden exactamente entre dominios. Los resultados económicos describen actividad, precios y trabajo; no se atribuyen a partidos, elecciones o políticas específicas.

El DANE pone microdatos anonimizados a disposición mediante su portal, que requiere CAPTCHA y establece condiciones de uso. La extensión individual queda documentada para descarga manual, verificación del diseño muestral y análisis ponderado. No se suben microdatos a este repositorio.

## Fuentes y créditos

Fuentes primarias: Departamento Administrativo Nacional de Estadística (DANE), Encuesta de Cultura Política, PIB, IPC, GEIH y proyecciones de población; Registraduría Nacional del Estado Civil, escrutinio presidencial de 2022. El contexto cualitativo incluye literatura académica colombiana citada en [docs/metodo_cualitativo_es.md](docs/metodo_cualitativo_es.md).

El código del proyecto se publica bajo licencia MIT. Las fuentes, marcas, publicaciones y datos conservan sus términos y atribución originales; ver [LICENSE](LICENSE) y [SOURCES.md](SOURCES.md).

---

## English overview

This beginner-friendly data analytics portfolio project combines official Colombian statistics from DANE and the National Civil Registry to explore political information channels, participation, public opinion, demographics, and recent economic indicators. It includes an interactive dashboard, documented aggregate data, a qualitative evidence review, and a responsible plan for extending the work with survey microdata.

### Key findings

- Among adults who said they followed political news, reported social-media use rose from **55.0% in 2021 to 62.9% in 2023**. Television remained the most frequently selected channel (**87.9% in 2023**).
- In the 2023 Political Culture Survey, **89.5% of registered respondents** said they voted in the 2022 presidential election. The official second-round turnout was **58.17% of the electoral roll**; these figures use different populations and methods.
- For comparable periods, annual Q2 real GDP growth was **2.1%, 2.1%, and 3.5%** (2024–2026); September annual CPI inflation was **5.81%, 5.18%, and 6.29%**; August unemployment was **9.7%, 8.6%, and 9.4%**.
- These public aggregates describe trends and motivate further analysis. They do **not** establish that social media caused a voting choice or a specific opinion.

See [README.en.md](README.en.md) for the full English documentation.

