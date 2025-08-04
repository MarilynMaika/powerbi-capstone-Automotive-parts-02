# 🚗 Predictive Maintenance for Automotive Equipment – 2024 Capstone Project  
**Group 3** | DSA 2040A – Semester Project

---

## 👩🏽‍💻 Group Members  
- Student 1 – Marilyn S
- Student 2 – Gracy K
- Student 3 – Amy N 

---

## 📘 Project Summary  
This project focuses on predictive maintenance in an automotive parts manufacturing setting. Using simulated IoT sensor data, we aim to reduce unplanned downtime and optimize maintenance costs by predicting potential equipment failures before they occur.

The objective is to assist the maintenance and operations team in proactively managing repairs and minimizing expensive reactive interventions, ultimately improving production efficiency.

---

## 📈 Key Deliverables  
- ✅ Business KPIs for failure reduction and cost performance  
- ✅ Top 3 insights to support strategic maintenance decisions  
- ✅ ROI (Return on Investment) summary to justify predictive strategy

---

## Explanation of terms
✅ **Preventive Cost**

Preventive costs refer to the expenses incurred to prevent equipment failure or reduce the risk of breakdown. These are planned, scheduled maintenance activities performed regularly, even if the equipment appears to be working well.

Examples:
Routine inspections, Lubrication and cleaning, Replacing parts before failure, Calibration of machinery

Goal: To avoid breakdowns, extend equipment life, and reduce long-term costs.

⚠️ **Reactive Cost**

Reactive costs are the expenses incurred when equipment fails unexpectedly, and action is taken after the failure. This is also called run-to-failure or corrective maintenance.

Examples: Emergency repair services, Replacement of damaged components, Downtime and lost productivity, Extra labor or overtime

---

## 🛠️ Process Overview  

### 1. **Data Simulation**  
Since actual sensor data was not available, we generated synthetic IoT sensor readings for:
- Vibration, pressure, temperature  
- Maintenance types (preventive vs reactive)  
- Equipment criticality and failure status  

This ensured realistic variation for failure prediction modeling.

- #### The Health Score was calculated as follows

**HealthScore = 100 -
  ((|Temperature - 75| × 0.5) +
   (|Vibration - 5| × 2) +
   (|Pressure - 2| × 10) +
   (|Voltage - 220| × 0.1))**
   
 **This formula penalizes readings deviating from optimal operating ranges, with higher penalties for parameters like pressure or vibration that impact failure more significantly.**  


### 2. **Data Cleaning**  
Cleaning steps included:  
- Handling nulls and outliers  
- Formatting datetime and categorical values  
- Removing duplicates  
- Validating types (e.g., numeric formats) and saving the transformed data in the cleaned folder


### 3. **Data Modeling in Power BI**  
- Built a **star schema** with central `fact_table_cleaned` and surrounding dimension tables (`dim_equipment_cleaned`, `dim_date`, etc.)  
- Established relationships and cardinalities  
- Implemented **Row-Level Security (RLS)** for user access control  

### 4. **Calculated Columns**  
Created new columns inside Power BI to enhance analysis:
- `TemperatureCategory`: categorized values into **Low**, **Medium**, and **High** ranges for insight into environmental impact on failures.

---

## 💰 ROI (Return on Investment) Calculation  

**ROI** quantifies the benefit gained from using predictive maintenance relative to its cost.  
We used the formula:  

ROI = ((Cost Avoided - Preventive Cost) / Preventive Cost ) * 100



- **Cost Avoided**: Estimated costs saved by avoiding reactive maintenance  
- **Preventive Cost**: Cost incurred by scheduled or predictive maintenance actions

### 📌 Example Interpretation  
An ROI of **300** means that for every 1 unit spent on preventive maintenance, the company avoided 3 units of potential reactive maintenance cost — a **300% return**, which justifies the investment in prediction models.

---

## 📊 Technical Features  
- ✅ Star schema model with full RLS implementation  
- ✅ 30+ DAX measures (e.g., failure rates, monthly breakdowns, cost ratios)  
- ✅ Calculated columns (e.g., temperature categories)  
- ✅ Drill-through filters, parameters, and mobile layout  
- ✅ KPI cards and trend visuals  

---

## 🔍 Top 3 Insights  
1. **Reactive to Preventive Cost Ratio = 4.7**  
   → Reactive maintenance costs are nearly 5x higher than preventive costs, suggesting inefficient maintenance practices.  

2. **Higher Failures in High-Temperature Equipment**  
   → Equipment in high-temperature zones had the most predicted failures, emphasizing need for cooling systems.  

3. **Non-critical equipment still predicts failures**  
   → A notable percentage of predicted failures were in non-critical assets, highlighting hidden risks.



## 🌐 Published Dashboard  
[Click to View Live Report](https://app.powerbi.com/view?r=eyJrIjoiNzk4NzUwYzUtZjc1Yi00MjU0LWFmYjctZGQ5Y2RiY2I1MzQzIiwidCI6IjE2ZDgzZWU2LTI1NGEtNDY5ZC1hNmNjLTU0ZTJjYTIzMTNlNyIsImMiOjh9)
