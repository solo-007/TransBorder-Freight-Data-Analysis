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
<img width="768" height="577" alt="CRISP-DM" src="https://github.com/user-attachments/assets/899f4b12-7e59-4ba7-ad4b-9648be0c7d29" />

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

## Business Questions & Findings  
**Below are the business questions explored:**  

### **1) What is the highest mode of transportation over the years?**  
**Visualization:**![image](https://github.com/user-attachments/assets/75672475-97c4-4efb-a9fb-d46d5d2442ae)

**Key Findings:**  
- **Road mode of transport dominates (2020-2024) by trade value**
- **Vessel and Pipeline** dominates as the highest mode of transport by Shipment weight (2020-2024)
- **Truck and Pipeline mode of transport** spans across the years (2020-2024) as the leading by freight charges.

---

### **2) How is freight movement across different transportation modes over time and regions?**  
**Visualization:**![image](https://github.com/user-attachments/assets/72db2c48-1075-4752-9ce3-1c8ce1050a5f)
  
**Key Findings:**  
- **Road Transport increased** at a Trade Cost Value of 827Billion USD from the year 2021 uptill 2023 at a Trade Cost Value of 996Billion USD untill its decreasing value of 703Billion USD.
- **Port Laredo** in the Texas dominated with Truck mode of transport at a value of $962.31 Billion
- **Imports favor bulk and volume**, hence the dominance of truck and rail.

---

### **3) How much freight cost is incurred per dollar of trade value moved?**
**Visualization:**![image](https://github.com/user-attachments/assets/40854ca2-68d1-448e-b4a6-7c737a3eccb5)

**Key Findings:**
-**On average, $0.05 - $0.08 of freight cost** is incurred for every $1 of trade value moved, based on aggregate analysis across all transport modes.

---

### **4) How has the total trade value evolved from 2020 to 2024?**
**Visualization:**![image](https://github.com/user-attachments/assets/06686f0b-09f8-4dfb-b848-7218be5b0b7d)

**Key Findings:**
-**2020 to 2021:** Major surge — trade value increased by ~73%
-**2021 to 2022:** Continued growth — up ~18.6%
-**2022 to 2023:** Plateaued — very slight increase (~0.05%)
-**2023 to 2024:** Notable drop — trade value fell ~31.9%

---

### **5) Which mode of transportation dominates trade, and how has its share changed over time?**
**Visualization:**![image](https://github.com/user-attachments/assets/9457cc3a-ef45-4a22-9ac8-879ab2aa2633)

**Key Findings:**
-**Truck mode of transport** not only dominates but has grown in absolute trade value every year—reinforcing its role as the backbone of the transportation network.

---

### **6) Which U.S. ports (by state or code) handle the most freight, and what are the bottlenecks?**
**Visualization:**![image](https://github.com/user-attachments/assets/82900e42-39ed-459b-a1ce-b0fade2603f9)

**Key Findings:**
-**Port Laredo in Texas** with shipment weight of 1.2Trillion kilograms handles the most freight.
-It leads in land-based freight, especially cross-border trade with Mexico.
-**Customs Delays:** Despite improvements, peak-hour truck wait times still challenge throughput

---

### **7) Is there any seasonal pattern in freight movement (e.g., more trade in Q4)?**
**Visualization:**![image](https://github.com/user-attachments/assets/75835153-a43a-4f12-be61-44d199379823)

**Key Findings:**
-**Higher movement in Q2–Q4 (April–October)**: Likely due to increased production, trade cycles, and holiday stocking.
-**Lower movement in January & February:** Common slowdown due to post-holiday demand drop, cold weather, and planning periods.
-Freight movement shows a clear seasonal pattern, peaking from May to September, which aligns with economic and trade cycles.

---

### **8) How much does each mode contribute to economic productivity across regions (e.g., by border state)?**
**Visualization:**![image](https://github.com/user-attachments/assets/09dc364c-7272-47bb-900a-72554139739e)

**Key Findings:**
-**Texas (TX)** dominates by far in total trade value—highlighting its key role as a central freight hub, likely due to extensive border trade with Mexico.
-**Michigan (MI), California (CA), and Illinois (IL)** also stand out with significant multimodal contributions

---

### **9) What are the top 10 U.S. states (USASTATE) by total freight value?**
**Visualization:**![image](https://github.com/user-attachments/assets/ba79c066-b79d-4f0e-a01b-b24b726a79d0)

**Key Findings:**
-Texas among the top 10 states has a freight value of 1,407,813,385,112 USD

---

### **10) How has the total freight value changed over time?**
**Visualization:**![image](https://github.com/user-attachments/assets/30b2ca01-6902-4ec9-98ef-a613e2bc3633)

**Key Findings:**
-Across all years, freight value tends to rise mid-year (May–August) and taper off slightly toward December, suggesting seasonal demand cycles.
-Freight value has grown steadily year-over-year, with 2023 and 2024 showing the strongest performance. This reflects expanding trade activity, possibly driven by economic recovery, infrastructure improvements, or increased cross-border flows.

---

### **11) What commodities (COMMODITY2) contribute the most to freight value?**
**Visualization:**![image](https://github.com/user-attachments/assets/25f3bb65-d918-4e93-a293-557706238247)

**Key Findings:**
-**Vehicles (87)** lead the pack, likely driven by strong automotive trade with Mexico and Canada.
-**Mineral fuels (27)** reflect the high value of energy commodities, especially pipeline and vessel shipments.
-**Machinery (84 & 85)** show the backbone of industrial and consumer electronics trade.

---


### **12) Which country is the biggest trade partner based on freight value?**
**Visualization:**![image](https://github.com/user-attachments/assets/40fd1bcc-871f-4b48-ae96-708f7cd41432)

**Key Findings:**
-Mexico is the top trading partner to the United State with a trade value of $3,189,151,996,082.

---

### **13) What is the trend of freight weight (SHIPWT) vs value (VALUE) over the years?**
**Visualization:**![image](https://github.com/user-attachments/assets/7c416050-acb0-4cc9-802f-970f39f04dc4)

**Key Findings**
-**Divergence:** If VALUE is increasing faster than SHIPWT, it indicates shipping of higher-value goods. (e.g., electronics vs raw materials).
-**Parallel Movement:** If both increase or decrease together, volume and economic activity are scaling proportionally.
-**Yearly Anomalies:** Sudden drop in 2020, might indicate events like COVID-19’s impact on trade.

---

### **14) Which modes or routes are least environmentally friendly?**
**Visualization:**![image](https://github.com/user-attachments/assets/30b2ca01-6902-4ec9-98ef-a613e2bc3633)

**Key Findings:**
-**Cross-border routes like New Jersey→Mexico and Kentucky→Canada are among the least offenders—likely due to heavy reliance on air/truck and high freight costs per kg.

---

## How to Run

1. Download the notebook: `Transborder_Freight_DataAnalysis.ipynb`
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn
   ```
3. Run in Jupyter or any compatible Python environment.

---
