
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
## BUSINESS QUESTIONS
### Analytical Questions to Address:
1.	What is the highest mode of transportation over the years?
2.  How is freight moving across different transportation modes over time and regions?
3.  How much freight cost is incurred per dollar of trade value moved?
4.	How has the total trade value evolved from 2020 to 2024?
5.	Which mode of transportation dominates trade, and how has its share changed over time?
6.	Which U.S. ports (by state or code) handle the most freight, and what are the bottlenecks? 
7.	Is there any seasonal pattern in freight movement (e.g., more trade in Q4)?
8.	How much does each mode contribute to economic productivity across regions (e.g., by border state)?
9.	What are the top 10 U.S. states (USASTATE) by total freight value?
10.	How has the total freight value changed over time?
11.	What commodities (COMMODITY2) contribute the most to freight value?
12. Which country is the biggest trade partners based on freight value?
13. What is the trend of freight weight (SHIPWT) vs value (VALUE) over the years?
14. Which modes or routes are least environmentally friendly?

---
## CRISP-DM Framework
<img width="768" height="1125" alt="CRISP-DM" src="https://github.com/user-attachments/assets/8493db5b-8c9b-49f2-b3a7-d85ca50a00f0" />

### 1. Business Understanding
Establish objectives and research questions to tackle BTS's problems, with an emphasis on inefficiencies, safety issues, and environmental effects.

### 2. Data Understanding
-Examine the properties and structure of the dataset.
-Evaluate the quality of the data (anomalies, missing values).
-Tools: Tableau Prep, Pandas Profiling.

### 3. Data Preparation
-**Cleaning:** Address missing values, standardize units, and fix irregularities.
-Combine datasets into a single database through **Integration:**.
- **Feature Engineering:** Develop metrics such as congestion indices and emission estimations.
- Tools: Python (Pandas, NumPy)

### 4. Modeling and Analysis
- **Trend Analysis:** Identify freight trends over time.
- **Geospatial Analysis:** Map freight flows and bottlenecks using GeoPandas.
- **Pattern Recognition:** Use clustering to group regions or commodities.
- **Environmental and Safety Assessment:** Analyze emissions and safety incidents.
- Tools: Matplotlib, Plotly, Scikit-learn.

### 5. Evaluation
Validate findings through cross-referencing benchmarks and stakeholder feedback to ensure actionable insights

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
