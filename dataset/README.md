# Data

## micro-dataset.csv

### Provenance

This dataset was compiled by **A11 – Initiative for Economic and Social Rights** (Belgrade, Serbia) from case files, administrative decisions, and direct contact with affected beneficiaries of Serbia's Social Card Registry. It was shared with Eticas Foundation under a confidentiality agreement for the purposes of this audit.

The original data was structured as a table ("Table – Socioeconomic data on excluded individuals") and harmonised into machine-readable CSV format by Eticas Foundation for reproducibility purposes.

**N = 15 cases**

Initials have been retained as provided by A11. No further re-identification has been performed. Do not attempt to re-identify individuals.

### Field Definitions

| Field | Type | Description |
|---|---|---|
| `id` | integer | Row identifier (1–15) |
| `initials` | string | Anonymised initials of the affected individual, as provided by A11 |
| `location` | string | Municipality or city of residence |
| `gender` | string | M / F as recorded in case files |
| `age` | integer | Age at time of case documentation |
| `household_size` | integer | Number of family members in the household |
| `employment_status` | string | Reported employment status at time of exclusion |
| `exclusion_reason_raw` | string | Verbatim exclusion reason as recorded by A11 |
| `exclusion_category_vehicle` | boolean | TRUE if vehicle ownership or registration was a stated factor in the exclusion |
| `exclusion_category_income_misclassification` | boolean | TRUE if misclassification of income (including donations treated as income) was a stated factor |
| `exclusion_category_seasonal_work` | boolean | TRUE if seasonal work income was a stated factor (legally exempt under the Law on Seasonal Workers) |
| `exclusion_without_written_decision` | boolean | TRUE if benefit was suspended or reduced without a written administrative decision |
| `notes` | string | Additional contextual notes |

### Macro-Level Data Sources

The macro-level analysis in the audit report draws on publicly available sources only. No proprietary datasets were used. Key sources:

- **Statistical Office of the Republic of Serbia (SORS)** – Poverty and Social Inequality Indicators 2024. https://www.stat.gov.rs
- **World Bank – Poverty and Inequality Platform** – Gini Index for Serbia (2023). https://pip.worldbank.org
- **UNICEF Serbia** – Poverty Projections: Economic Impact of the Ukraine Crisis, 2023. https://www.unicef.org/serbia
- **EAPN Serbia** – Poverty Watch 2023. https://www.eapn.eu/wp-content/uploads/2023/10/eapn-Poverty-Watch-Serbia-2023.pdf
- **World Bank** – Western Balkans Regular Economic Report, 2024. https://www.worldbank.org/en/region/eca/publication/western-balkans-regular-economic-report

### Limitations

- The micro-dataset (N=15) is not a random or representative sample. It reflects cases brought to A11's attention through complaints and community outreach, and is therefore likely to overrepresent the most severe or well-documented exclusions.
- The dataset does not permit statistical inference or generalisation to the broader population of Social Card Registry beneficiaries.
- The audit was conducted as a black-box exercise; no direct access to the registry's source code or internal data was granted.
