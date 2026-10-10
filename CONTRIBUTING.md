# Contributing and learning path

This is an educational portfolio project. Small, traceable improvements are welcome.

## Beginner-friendly sequence

1. Read `docs/diccionario_datos.md` and identify the population/denominator for each metric.
2. Run `python src/build_dashboard.py` and open `index.html` locally.
3. Explore `notebooks/01_exploracion_colombia.ipynb`: inspect missing values, compare years, and calculate percentage-point differences.
4. Add one new official aggregate indicator with its source URL, release date, unit, and denominator. Never mix periods or definitions without documenting the choice.
5. Add one visualization and explain the insight and its limitation in `docs/hallazgos_es.md`.
6. For the ECP individual-level extension, follow `docs/microdata_extension.md`; do not place microdata in a commit.

## Contribution standards

- Prefer DANE, Registraduría, Banco de la República, or other primary public sources.
- Add provenance in the source CSV and source manifest for every new value.
- Label derived calculations and keep formulas reproducible.
- Use neutral language about political actors and avoid causal claims without a design that supports them.
- Do not commit raw microdata, credentials, local download links, or personal information.
- Keep the dashboard usable on mobile and include alt/accessible labels for visual elements.

