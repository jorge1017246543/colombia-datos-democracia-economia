# Colombia in Data: Democracy, Digital Conversation & the Economy

**Bilingual analytics portfolio project · Research cut-off: October 8, 2026**

An educational data analytics project combining official DANE and National Civil Registry statistics to explore political information channels, participation, public opinion, demographics, and recent economic conditions in Colombia. The repository includes an interactive dashboard, traceable aggregate datasets, a qualitative evidence review, and a responsible plan for extending the work with survey microdata.

> **Research question:** What patterns describe the evolution of political information sources, participation, and democratic perceptions in Colombia, and how can they be read alongside recent demographic and economic context?

## Explore

- [Interactive dashboard](index.html)
- [Initial findings](docs/hallazgos_es.md) (Spanish)
- [Analytical design](docs/metodologia_es.md) (Spanish)
- [Qualitative framework](docs/metodo_cualitativo_es.md) (Spanish)
- [Data dictionary](docs/diccionario_datos.md) (Spanish)
- [Learning guide](docs/guia_de_aprendizaje_es.md) (Spanish)
- [Microdata extension](docs/microdata_extension.md)
- [Source manifest](data/sources.csv)
- [Spanish README](README.md)

## Executive summary

- Among respondents who said they followed political news, reported social-media use rose from **55.0% in 2021 to 62.9% in 2023**. Television remained the most frequently selected channel, at **87.9% in 2023**.
- In the 2023 Political Culture Survey, **89.5% of registered respondents** said they voted in the 2022 presidential election. The official second-round turnout was **58.17% of the electoral roll**. These measures use different populations and methods and are not directly comparable.
- Across selected comparable periods, annual Q2 real GDP growth was **2.1%, 2.1%, and 3.5%** (2024–2026); September annual CPI inflation was **5.81%, 5.18%, and 6.29%**; August unemployment was **9.7%, 8.6%, and 9.4%**.
- The evidence supports descriptive findings and hypotheses for further research; it does **not** show that social media caused voting choices or particular opinions.

## Analytics skills demonstrated

- Translating a business question into measurable analytical questions.
- Selecting, documenting, and triangulating official data sources.
- Structuring aggregate indicators as traceable CSV tables.
- Defining populations, units, frequencies, and denominators.
- Comparative analysis and descriptive regional segmentation.
- Building accessible interactive visualizations with HTML, SVG, and JavaScript.
- Qualitative synthesis of source methods, research literature, and inference limits.
- Communicating neutral findings and a clear next-step analysis plan.

## Open and reproduce

The static dashboard can be opened directly from `index.html`. Rebuild it from the repository CSVs with Python 3.10 or later:

```bash
python src/build_dashboard.py
```

Dashboard generation uses only Python's standard library. The optional learning notebook uses pandas and Plotly:

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_exploracion_colombia.ipynb
```

The GitHub Actions workflow in `.github/workflows/pages.yml` publishes the dashboard to GitHub Pages once this repository is created and Pages is enabled.

## Project structure

```text
data/
  processed/        # Published official aggregate extracts for exploration
  raw/              # Empty in Git; local microdata are never versioned
  sources.csv       # Source inventory, period, and access notes
docs/               # Findings, method, qualitative review, and data guide
notebooks/          # Guided pandas/Plotly learning notebook
src/                # Reproducible dashboard builder
index.html          # Self-contained interactive dashboard
```

## Scope and limitations

Political culture is measured mainly through the 2023 ECP, with published comparisons for 2019/2021/2023. The economic snapshot uses GDP through Q2 2026, CPI through September 2026, and labor-market data through August 2026. These domains do not have identical observation periods. Economic indicators describe activity, prices, and employment; this project does not attribute them to parties, elections, or specific policies.

DANE anonymized microdata are available through its catalog, which requires a CAPTCHA and sets conditions of use. The individual-level extension is documented as a manual download and a survey-weighted analysis. No microdata are included in this repository.

## Sources and licensing

Primary data sources are DANE (Political Culture Survey, GDP, CPI, GEIH, and population projections) and Colombia's National Civil Registry (2022 presidential vote count). Academic papers cited in [the qualitative review](docs/metodo_cualitativo_es.md) provide context, not replacement estimates.

Project code is licensed under MIT. Source publications, data, and trademarks remain subject to their original attribution and use conditions; see [LICENSE](LICENSE) and [SOURCES.md](SOURCES.md).

