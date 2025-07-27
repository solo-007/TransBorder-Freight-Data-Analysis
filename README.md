
# Freight Transportation Data Analysis – BTS Project

This project analyzes freight transportation data from the **Bureau of Transportation Statistics (BTS)** to extract business insights, identify operational inefficiencies, and propose sustainability recommendations. It follows the **CRISP-DM framework**, using real-world data spanning multiple years across various transportation modes and trade routes.

---

## Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| **Python (Jupyter Notebook)** | Main language for data exploration and analysis |
| **Pandas** | Data loading, cleaning, aggregation |
| **NumPy** | Numerical operations |
| **Matplotlib & Seaborn** | Data visualization |
| **Plotly** *(optional, for Sankey or interactive plots)* | Advanced visualization |
| **CRISP-DM** | Data science project workflow |

---

## Data Source

- Data used was extracted from the **Bureau of Transportation Statistics (BTS)**
- Dataset includes monthly/yearly trade summaries categorized by:
  - Transportation mode (`DISAGMOT`)
  - Trade type (import/export via `TRDTYPE`)
  - Freight charges
  - Commodity, country, and port of entry/exit
  - Route-level data

---

## Project Objectives

1. **Uncover Freight Movement Patterns**
   - Trends by transportation mode across years
   - Port-to-country trade routes using Sankey and bar charts
   - Seasonal shifts (by `MONTH`)

2. **Identify Operational Inefficiencies**
   - Spot routes or modes with rising cost but lower freight volume
   - Evaluate underused vs overused trade lanes
   - Freight cost anomalies by mode and region

3. **Analyze Environmental Impact**
   - Estimate CO₂ emissions using emission factors per mode
   - Identify less sustainable trade patterns
   - Suggest greener alternatives or optimizations

---

## Key Insights

- Certain transportation modes (e.g. rail, truck) dominate in trade value, but air may incur higher costs per shipment weight.
- Domestic vs foreign (`DF`) classification impacts trade type.
- Missing data was more prevalent in regional breakdowns (e.g. `MEXSTATE`, `CANPROV`) but not at the national level.
- Top trade routes and partners identified by combined freight and value cost.
- Seasonal variation affects some modes more than others.

---

## How to Run

1. Download the notebook: `Transborder_Freight_DataAnalysis.ipynb`
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn
   ```
3. Run in Jupyter or any compatible Python environment.

---
