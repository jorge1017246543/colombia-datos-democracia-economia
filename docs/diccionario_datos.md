# Diccionario de datos

## Archivos de resultados

| Archivo | Granularidad | Campos principales | Precaución |
|---|---|---|---|
| `political_media.csv` | Canal × año | `channel`, `year`, `share_percent`, `denominator` | Respuesta múltiple; solo personas que sí se informan de política |
| `political_attention.csv` | Año | `responded_yes_percent`, `responded_no_percent` | Adultos 18+; el enrutamiento de canales usa solo “sí” |
| `election_participation.csv` | Métrica × grupo territorial | `measure`, `group`, `value_percent` | Autorreporte ECP 2023 sobre voto presidencial 2022 |
| `abstention_reasons_by_region.csv` | Razón × región | `reason`, `region`, `share_percent`, `precision_note` | Respuesta múltiple entre no votantes; respetar advertencia de precisión |
| `public_opinion.csv` | Indicador × año × grupo | `indicator`, `group`, `year`, `value_percent` | Preguntas/universos distintos; comparar solo la misma definición |
| `election_results_2022.csv` | Categoría de escrutinio | `candidate_or_status`, `votes`, `share_percent`, `denominator` | Segunda vuelta; porcentajes calculados sobre candidaturas + voto en blanco |
| `election_summary_2022.csv` | Métrica electoral nacional | `metric`, `value`, `unit`, `denominator` | Participación/censo y votos emitidos según nota del escrutinio |
| `election_summary_2022.csv` | Métrica electoral nacional | `metric`, `value`, `unit`, `denominator` | Participación/censo y votos emitidos según nota del escrutinio |
| `economic_indicators.csv` | Indicador × periodo | `indicator`, `period`, `value`, `frequency`, `comparison_basis` | No fusionar frecuencias ni interpretar como causalidad |
| `gdp_sector_contributions_2026q2.csv` | Actividad económica | `activity`, `value_growth_percent`, `contribution_pp` | Tres actividades destacadas, no la lista total |
| `demographic_context.csv` | Métrica × grupo × fecha | `indicator`, `group`, `period`, `value`, `unit` | Población total 2025 y universo ECP adulto 2023 son periodos distintos |
| `community_participation.csv` | Grupo × dominio | `measure`, `group`, `share_percent` | Estimaciones de la ECP para personas de 18+ |

Todas las tablas contienen una URL de origen por fila. Los valores son porcentajes en escala 0–100, excepto conteos de población/votos y contribuciones expresadas en puntos porcentuales.

