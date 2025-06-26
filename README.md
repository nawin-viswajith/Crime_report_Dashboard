# Tamil Nadu Crime Data Analysis (2014 – 2022)

A **longitudinal, data-driven study** of crime trends in Tamil Nadu, India.  
This repository contains the cleaned dataset, a fully commented exploratory notebook, publication-ready figures, and formal reports - everything required to reproduce the analysis or extend it with additional years.

---

## Table of Contents

1. [Objectives](#objectives)  
2. [Repository Structure](#repository-structure)  
3. [Quick Start](#quick-start)  
4. [Requirements](#requirements)  
5. [Key Findings (Brief)](#key-findings-brief)  
6. [Reproduce / Extend](#reproduce--extend)  
7. [License](#license)  

---

## Objectives

* **Quantify nine-year crime trends** across seven major categories and 56 specific offences.  
* **Detect composition shifts** to highlight emerging threats (e.g., cyber-crime).  
* **Model category correlations** to reveal co-moving clusters.  
* **Translate insights into policy-grade recommendations** for law-enforcement and civic planners.

---

## Repository Structure

| Path | Contents |
|------|----------|
| `data/raw/` | Original Excel file (`Crime report.xlsx`). |
| `data/processed/` | Cleaned CSV (`TN_Crime_Data_2014_2022.csv`). |
| `notebooks/` | **`EDA_with_descriptions.ipynb`** – step-by-step exploratory analysis with explanatory markdown. |
| `figures/` | PNG exports of all charts (trend lines, stacked area, heatmap, etc.). |
| `reports/` | PDF versions of the technical report and executive summary. |
| `.gitignore` | Excludes checkpoints, virtual-envs, and OS artefacts. |
| `requirements.txt` | Minimal Python dependencies. |
| `LICENSE` | MIT license. |
| `README.md` | This document. |

---

## Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/nawin-viswajith/Crime_report_Dashboard.git
cd Crime_report_Dashboard

# 2. (Optional) Create a virtual environment
python -m venv .venv
# macOS / Linux
source .venv/bin/activate
# Windows
.venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the exploratory notebook
jupyter notebook notebooks/EDA_with_descriptions.ipynb
```
All charts are interactive inside Jupyter.
If you prefer VS Code, simply open the notebook and run the cells.

## Requirements
- Python 3.9 +
- `pandas`, `numpy`, `plotly`, `openpyxl`, `jupyterlab` (listed in `requirements.txt`)

## Key Findings (Brief)

---

| Theme              | Insight                                                                            |
| ------------------ | ---------------------------------------------------------------------------------- |
| Cyber-crime        | Grew **+263 %** since 2014; highest three-year CAGR (+17 %).                       |
| Property & Traffic | Largest absolute volume; traffic dipped during COVID, rebounded in 2022.           |
| Concentration      | Top three specific offences = **> 50 %** of 2022 cases.                            |
| Correlations       | Violent & white-collar crimes co-move (r≈0.66), hinting at socio-economic linkage. |

---

## Reproduce / Extend
- **Add new years:** append additional columns (e.g., 2023) to data/processed/TN_Crime_Data_2014_2022.csv, adjust the years list in the notebook, rerun.
- **District-level drill-down:** supply FIR-level data in data/raw/, group by District, and replicate the aggregation cells.
- **Alternate visualisations:** the notebook is modular—swap Plotly for Matplotlib or export to Tableau/Power BI as desired.

## Disclaimer
The Excel file is sourced from publicly available NCRB tables; redistributed here under fair-use for academic analysis.

## License
This project is released under the MIT License.
You are free to use, modify, and distribute the code and data with proper attribution.
