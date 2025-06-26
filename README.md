# Tamil Nadu Crime Data Analysis (2014 – 2022)

A systematic, data-driven exploration of crime trends in Tamil Nadu, India, covering the period 2014 – 2022.  
The repository contains cleaned data, reproducible code, a full analytical report, and interactive dashboards that together provide a foundation for evidence-based public-safety decision-making.

---

## Contents

| Folder | Purpose |
|--------|---------|
| `data/` | Raw and cleaned datasets (`Crime report.xlsx`, `TN_Crime_Data_2014_2022.csv`). |
| `figures/` | Publication-ready PNGs of all charts (line, stacked area, waterfall, heatmap, etc.). |
| `notebooks/` | Jupyter notebooks for data preparation, exploratory analysis, and visualisation. |
| `reports/` | Word/PDF deliverables: technical analysis report, executive summary. |


---

## Objectives

1. **Quantify longitudinal trends** across seven aggregated crime categories and 56 specific offences.  
2. **Detect shifts in crime composition** to highlight emerging threats such as cyber-crime.  
3. **Model intra-category correlations** to reveal co-movement clusters.  
4. **Translate statistical findings into policy-grade recommendations** for law-enforcement and civic planners.

---

## Data Source

* Primary file: `Crime report.xlsx` (Sheet 2).  
* Fields: `Specific Crime Type`, `Category`, annual case counts for `2014 – 2022`.  
* Integrity checks: forward-filled category labels, numeric type enforcement, no suppression of outliers.

---

## Analytical Workflow

1. **Ingestion & Cleaning**  
   * Load Excel → pandas, handle null categories, verify numeric columns.

2. **Exploratory Data Analysis**  
   * Multi-line and stacked-area plots for year-on-year trends.  
   * Heatmaps for top-volume offences.  
   * Waterfall chart for annual deltas.  
   * Calculation of long-run percent change and 3-year CAGR.  
   * Pearson correlation matrix across categories.

3. **Visual Dashboard**  
   * Nine interactive Plotly figures assembled into a two-column HTML dashboard.  
   * Pie-chart add-on for 2022 composition.  
   * Instructions and field mapping for a Power BI `.pbix` build.

4. **Reporting**  
   * Technical report with “Data Input → Transformation → Insight → Recommendation” tables.  
   * Executive narrative report with introduction, objectives, findings, and safety-measure roadmap.

---

## Key Findings (Brief)

| Theme | Core Insight |
|-------|--------------|
| Cyber-crime | +263 % growth since 2014; highest CAGR in last three years. |
| Property & Traffic | Dominant in absolute volume; traffic cases dipped during COVID, rebounded in 2022. |
| Concentration | Top three specific offences contribute >50 % of total cases (Pareto). |
| Correlations | Violent and white-collar crimes move together (r≈0.66), suggesting socio-economic linkage. |

Full details appear in `reports/`.

---

## Reproducing the Analysis

```bash
# clone repository
git clone https://github.com/your-org/tn-crime-analysis.git
cd tn-crime-analysis

# create virtual environment (optional)
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# install requirements
pip install -r requirements.txt

# run notebooks or scripts
jupyter notebook notebooks/EDA.ipynb
python scripts/generate_dashboard.py
```
Dependencies: `pandas`, `numpy`, `plotly`, `openpyxl`, `python-docx`.

## Using the Dashboard
1. Open dashboards/TN_Crime_Dashboard.html in any modern browser.

2. Hover, zoom, and filter charts interactively.

3. For Power BI users, load TN_Crime_Data_2014_2022.csv and follow the PowerBI_blueprint.md for visual setup.

## Recommended Safety Measures
- Cyber-crime: district-level cyber desks, quarterly phishing-awareness campaigns.

- Traffic: AI-based speed-camera expansion, “No Helmet – No Fuel” state-wide enforcement.

- Property/Violet: hotspot policing guided by theft density maps, community mediation centres.

- Women & Children: one-stop crisis centres, school cyber-tipline integration.

See reports/Comprehensive_Crime_Analysis_Report.docx for the full action plan.

## License
This project is released under the MIT License.
