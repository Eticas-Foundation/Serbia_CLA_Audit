# Community-Led Audit: Serbian Social Card Registry

**Eticas Foundation** | Independent AI Audit  
**Partner:** A11 – Initiative for Economic and Social Rights (Belgrade, Serbia)  
**Audit type:** Black-box adversarial audit  
**Status:** Completed (2025)

---

## Overview

This repository contains the data and analysis code supporting Eticas Foundation's independent audit of Serbia's **Social Card Registry** — a centralised information system established under the Law on the Social Card (2021) that automates eligibility decisions for financial social assistance.

The audit examined whether the Registry's design and operation causes unjust exclusion of vulnerable beneficiaries, with a focus on Roma communities and households engaged in informal or seasonal labour. It was conducted in close collaboration with A11, drawing on their case files, legal analysis, and community engagement.

A full description of the audit methodology, findings, and recommendations is contained in the **Audit Report** (see `docs/`).

---

## Repository Structure

```
.
├── data/
│   ├── micro-dataset.csv          # Structured case-level dataset (N=15), compiled from A11 case files
│   └── README.md                  # Data provenance, field definitions, and macro-level sources
│
├── analysis/
│   └── descriptive_analysis.ipynb # Reproducible analysis notebook (Python)
│
├── docs/
│   └── [Audit Report and supporting documents — see below]
│
└── README.md
```

---

## Data

The quantitative analysis is based on a **micro-dataset of 15 cases** compiled by A11 from case files, administrative decisions, and direct beneficiary contact. Cases were coded into three analytical categories corresponding to the audit's harm hypotheses:

| Category | Cases | % | Hypothesis |
|---|---|---|---|
| Income misclassification / donations | 7 | 47% | Accuracy |
| Seasonal work income (legally exempt) | 6 | 40% | Compliance |
| Vehicle-related flags | 4 | 27% | Discrimination |
| Action without written decision | 3 | 20% | Transparency |

Macro-level analysis draws on publicly available data from SORS, the World Bank, UNICEF Serbia, and EAPN Serbia. See `data/README.md` for full source list and links.

> ⚠️ The micro-dataset is not a representative sample. See `data/README.md` for limitations.

---

## Analysis

The Jupyter notebook at `analysis/descriptive_analysis.ipynb` reproduces all descriptive statistics reported in the Audit Report (Section 2). It requires Python 3.9+ and the following packages:

```
pandas
matplotlib
seaborn
jupyter
```

Install dependencies:

```bash
pip install pandas matplotlib seaborn jupyter
```

Run the notebook:

```bash
jupyter notebook analysis/descriptive_analysis.ipynb
```

---

## Audit Scope and Methodology

This was a **black-box audit** — conducted without access to the Registry's source code or internal database. The methodology combined:

- **Documentary analysis:** procurement records, user manuals, legal opinions, A11 case files, World Bank complaint materials
- **Micro-level quantitative analysis:** structured coding of 15 documented exclusion cases
- **Macro-level contextual analysis:** national poverty, inequality, and social protection indicators
- **Qualitative data collection:** focus groups and interviews with beneficiaries and social workers

---

## Key Findings

- The Registry systematically misclassifies legally exempt income (seasonal wages, funeral donations, recycling earnings) as disqualifying, in apparent violation of the Law on Seasonal Workers and the Law on Social Protection.
- Vehicle flags based on outdated registration data trigger automated exclusions unconnected to actual asset ownership.
- A minimum of 20% of documented cases involved benefit suspension or reduction without a formal written decision, breaching beneficiaries' right to appeal.
- The audit's semi-automated decision architecture effectively removes meaningful professional discretion from social workers.

Full findings and recommendations are contained in the Audit Report.

---

## Team

**Project Lead & Research Director:** Dr. Gemma Galdon-Clavell, Founder of Eticas Foundation  
**Project Team:** Oliver Smith (Head of Innovation), Catalina María Bernal Murcia (Data Scientist), Melissa Robles Carmona (Data Scientist)  
**Community Partner:** A11 – Initiative for Economic and Social Rights

---

## License

The audit report and supporting documents are © Eticas Foundation. The dataset and analysis code are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) for research and accountability purposes. Attribution required: *Eticas Foundation / A11 – Initiative for Economic and Social Rights*.

The micro-dataset contains anonymised case data shared by A11 under a confidentiality agreement. Do not attempt to re-identify individuals.
