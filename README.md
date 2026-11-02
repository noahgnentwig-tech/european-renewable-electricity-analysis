# European Renewable Electricity Analysis (2015–2025)

**A data analytics portfolio project by Noah Nentwig**

An exploratory study of recorded renewable electricity generation across European countries, combining Python data preparation, measurement validation, country comparisons and dashboard reporting.

The project asks how recorded generation changes over time, how renewable technologies compare, and how country rankings change when generation is measured per person.

## Explore the project

| Deliverable | Contents |
| --- | --- |
| [Analysis notebook](notebooks/european-renewable-electricity-analysis.ipynb) | Data inspection, cleaning, validation, trends and country comparisons |
| [Dashboard PDF](reports/renewable-electricity-dashboard.pdf) | Four-page export covering trends, countries, supplied targets and data quality |
| [Presentation](reports/renewable-electricity-presentation.pptx) | Original project presentation |

The original project was titled **“Is Europe Getting Greener?”** The repository uses a more precise title because absolute renewable generation alone cannot establish changes in renewable electricity share or emissions intensity. The original report exports retain their original internal titles.

## Skills demonstrated

- Python analysis with pandas and NumPy.
- Category standardization, duplicate inspection and validated country joins.
- Quality flags for negative values and generation exceeding a monthly capacity-based maximum.
- Time-series and country comparisons with matplotlib and seaborn.
- Communication through a presentation and dashboard export.

## Method and interpretation

The workflow joins electricity readings to country metadata, flags suspect measurements, excludes invalid generation from aggregates, and compares recorded generation by year, technology and country. It also examines a country cohort represented in every year from 2018 through 2025.

Absolute generation and generation per person describe different aspects of the dataset. Per-person generation is calculated as **GWh / (population in millions × 1,000)**, yielding MWh/person.

## Run locally

Use Python 3.10 or newer. From the repository root:

```bash
python -m venv .venv
```

Activate the environment (`.venv\Scripts\activate` on Windows or `source .venv/bin/activate` on macOS/Linux), then run:

```bash
python -m pip install -r requirements.txt
jupyter lab notebooks/european-renewable-electricity-analysis.ipynb
```

Place the original `renewable_energy_readings.csv` and `countries.csv` files in `data/raw/` before running all notebook cells in order. These CSVs were not included in the recovered project attachments. This repository is therefore a documented portfolio submission with a prepared notebook, rather than a fully reproducible data release.

## Preparation and validation status

For this repository, the notebook's per-capita conversion was corrected before its chart, input paths were made relative, and explanatory Markdown was added. Saved notebook outputs were cleared to avoid displaying results from an earlier execution beside changed code. Code cells were checked for Python syntax; the analysis has **not** been rerun because its source data is unavailable. The PDF and PowerPoint are original exports, not regenerated results.

## Limitations and next steps

- Country coverage changes over time; aggregate changes are not a like-for-like European growth estimate.
- A fixed country cohort does not guarantee complete month or technology coverage. A stricter comparable panel remains a next step.
- Data provider, provenance, reporting definitions and redistribution rights require documentation. No official source attribution is claimed here.
- Supplied population and 2030 targets require independent verification. Target metadata is not evidence of verified policy or a valid target gap.
- Estimated and provisional readings remain included where generation passes validation; a final-only sensitivity analysis remains outstanding.
- Duplicate removal precedes category standardization in the submitted workflow; normalized observation keys should be reviewed before interpreting a rerun.
- Additional data is needed to assess renewable share, fossil-fuel displacement or emissions intensity.

## Data and licensing

See [data/raw/README.md](data/raw/README.md) for required inputs. No open-source license or redistribution rights are asserted for the supplied data or third-party presentation template.
