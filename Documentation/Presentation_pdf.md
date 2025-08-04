# Power BI Capstone Project – [Automotive parts manufacturer with IoT sensors]
**Group [3]** | DSA 3050 – Semester Project
## Group Members
- Student 1 – Marilyn S
- Student 2 – Gracy K
- Student 3 – Amy N

# DASHBOARD EXPLANATIONS
## 📊 Dashboard: Equipments Overview

This dashboard provides a high-level summary of equipment performance, focusing on failure rates, costs, and operating conditions:

🔹 Key Insights:
Cost Saving Percent: The equipment has achieved a 0.64% cost saving through preventive maintenance or other optimizations.

Number of Equipment: The system tracks 20 unique equipment units.

Predicted Failures: A total of 525 failures are predicted, emphasizing the need for robust preventive strategies.

Reactive to Preventive Cost Ratio: The ratio stands at 4.59, meaning reactive maintenance is 4.59 times more costly than preventive maintenance, highlighting inefficiency in reactive strategies.

📈 Trends and Distributions:
Equipment Failure Rate (over time): Failure rates peaked around May–July 2024, suggesting operational or environmental stress during that period.

Temperature Category Distribution:

Most sensor readings are from Medium (687) temperature conditions.

High temperatures (200) correlate with increased failure risk.

Low temperatures (113) are least common.

Equipment Condition:

74.7% of the records indicate critical equipment status, underscoring high operational risk.

Cost by Manufacturer:

Bosch, Honeywell, and GE have significantly high cost avoided figures, but preventive costs remain low across all manufacturers.

This suggests high savings potential if preventive actions are scaled.

## 📊 Dashboard: Time Visualizations
This page provides a high-level overview of key performance indicators (KPIs) and their trends over time (monthly).

1. Key Performance Indicator (KPI) Cards
These cards at the top give a snapshot of the most important metrics for the entire period covered.

Average of HealthScore: 49.91

What it is: This is the average health rating of all monitored assets. Assuming a scale of 0−100, a score of ~50 suggests that, on average, the equipment is in a mediocre or borderline state of health.

ReactiveCost: 2M (2,000,000)

What it is: This is the total cost incurred from "reactive maintenance"—repairs performed after a piece of equipment has already failed. This is often called "fire-fighting."

PreventiveCost: 396K (396,000)

What it is: This is the total cost of "preventive maintenance"—planned activities to service equipment and prevent it from failing.

CostAvoided: 1M (1,000,000)

What it is: This is an estimate of the money saved by performing preventive maintenance on assets that were predicted to fail. It quantifies the value of the predictive program.

Key Insight: The company is spending 5 times more on reactive maintenance than on preventive maintenance (2M vs. 396K). While the predictive program has successfully avoided 1M in costs, the high reactive cost indicates that the company is still operating in a very reactive mode. There is a significant opportunity to reduce costs by investing more in preventive strategies.

2. Line Chart: Average of Health Score by Timestamp
What it shows: This chart tracks the fluctuation of the average equipment HealthScore month-by-month throughout the year.

Interpretation: The health score hovers around the 50 mark. There are noticeable dips in June (48.9) and August (48.7), indicating periods where equipment condition was at its worst. The health score peaked in May (51.2) and November (50.8). These dips and peaks could be correlated with production cycles, seasonal stress, or the timing of maintenance schedules.

3. Donut Chart: HealthScore by PredictedFailure
What it shows: This chart segments the data based on whether the system predicted a failure (True) or not (False).

Interpretation: The predictive model has flagged 46.46 of the instances as a potential failure (PredictedFailure = True). This is a substantial number and indicates that the underlying predictive model is actively identifying at-risk assets. This is the pool of events from which the "1M Cost Avoided" metric is calculated.

4. Bar Chart: Total Reactive Cost and Total Preventive Cost by Year and Month
What it shows: This chart provides a month-by-month comparison of spending on reactive versus preventive maintenance.

Interpretation: This is the most powerful visual on this page. In every single month, the Reactive Cost (dark bars) dramatically outweighs the Preventive Cost (light bars). The highest reactive cost occurred in June (0.20M), which directly correlates with the lowest point in the equipment Health Score chart. This strongly suggests that when equipment health declines, costly failures follow.

## 📊 Dashboard: Location Visualizations

This page drills down into the same metrics but breaks them down by physical location, helping to identify exactly where the problems are occurring.

1. KPI Cards
First LocationID / Name: LOC_01 / Assembly. This is likely just showing the first item in the location list.

Average Temperature: 74.62

This is a new metric on this page, suggesting that environmental factors like temperature might be tracked as a potential cause of failure.

Total Reactive Cost: 2M

This matches the total from the first page, confirming this is a different view of the same overall data.

2. Bar Chart: Total Reactive and Preventive Costs by Location Name
What it shows: A side-by-side cost comparison for each location.

Interpretation: This chart clearly pinpoints the problem areas. The Assembly and Testing locations have the highest reactive costs by a significant margin (approx. 0.28M and 0.27M respectively). In contrast, Storage has the lowest reactive costs. This tells managers exactly where to focus their attention.

3. Pie Chart: Count of Predicted Failure by the Location Name
What it shows: The distribution of the number of predicted failures across locations.

Interpretation: Interestingly, the locations with the most predicted failures (Warehouse at 18.9, Maintenance at 17.9) are not the ones with the highest reactive costs. The Assembly location, which has very high costs, only accounts for 17.6 of predictions.

Key Insight: This implies that failures in Assembly and Testing are far more costly than failures in other locations like the Warehouse. A single failure in Assembly likely costs much more to fix.

4. Bar Chart: Average of Health Score by Location Name
What it shows: The average equipment health score for each location.

Interpretation: The health scores are tightly clustered between 49 and 51. Testing has a low score (49) which aligns with its high reactive costs. However, Assembly has a mediocre score (50), yet the highest costs. This further supports the idea that the impact and cost of a failure in Assembly are disproportionately high.

5. Table: Detailed Breakdown by Location and Production Line
What it shows: A detailed table (matrix) providing raw numbers for costs and health scores, broken down by Location Name and even further by Production Line.

Actionable Insight: This is the most granular and actionable visual. It allows for precise problem identification. For example:

Within the Testing location, Line 1 is the main problem, with a reactive cost of 310,043.

Within the Assembly location, Line 2 is the primary driver of cost, with a reactive cost of 283,470.

Overall Summary & Recommendations
Problem: The company is in a reactive maintenance cycle, spending $5 for every $1 of preventive work. This is inefficient and costly.

Where to Focus: The primary sources of these high costs are the Assembly and Testing locations.

Actionable Steps: Using the detailed table, management can go a step further and target Testing Line 1 and Assembly Line 2 for immediate investigation and increased preventive maintenance.

Strategic Opportunity: There is a clear business case for increasing the preventive maintenance budget, especially for the identified high-cost assets, as the Cost Avoided metric shows this approach yields a positive return.


Q4):

* *Voltage and Pressure readings spike notably in Q3*, which may indicate seasonal workload stress, equipment overheating, or production peaks.
* *Temperature and Vibration readings remain more stable* throughout the quarters.
* The trends help identify *patterns that align with operational cycles*, allowing for more informed maintenance planning.

---

### 🧠 Summary

| Element         | What It Shows                                            |
| --------------- | -------------------------------------------------------- |
| KPI Cards       | Overall system health, sensor count, and failure alerts  |
| Donut Chart     | Equal sensor distribution across all factory locations   |
| Reference Table | Clear mapping between sensors, types, and units          |
| Bar Chart       | Pressure sensors dominate predicted failures             |
| Line Chart      | Voltage and pressure spike in Q3 — potential risk period |

---

This page provides both a macro and micro view of sensor-driven insights. It allows engineers, analysts, and decision-makers to *quickly assess health, **identify risky equipment, and **monitor trends across time and space*. Every visual contributes to a unified story about how sensor data can support predictive maintenance and reduce unplanned downtime.


---

### 📊 Sensor Visualizations – Interpretation

The *Sensor Visualizations* page presents an overview of the condition, distribution, and behavior of the sensors used to monitor equipment in the manufacturing environment. This section helps stakeholders understand how sensor data reflects equipment health, risk of failure, and operational trends over time.

---

#### 🔹 Top KPIs (Card Visuals)

Four key performance cards summarize the current sensor system status:

* *First Unit*: Displays "Celsius", indicating the unit of measurement for temperature readings. This acts as a reference point for interpreting the data shown across the dashboard.

* *Average HealthScore: 49.91*

  * Reflects the overall health of all equipment based on sensor readings.
  * Since the score is significantly below 60, it indicates *system-wide sensor readings deviating from ideal operating conditions*, suggesting wear, overload, or inefficiencies in machinery.

* *Count of PredictedFailure (True): 525*

  * Shows that *525 readings have crossed the defined failure threshold*, meaning the system flagged them as likely to precede a breakdown.
  * This highlights an increased *failure risk* across the equipment being monitored.

* *Count of SensorID: 10*

  * Indicates that *10 unique sensors* are currently tracked in the system.
  * These sensors monitor different aspects of the machines, such as pressure, voltage, temperature, and vibration.

---

#### 🥧 Sensor Distribution by Location (Donut Chart)

This visual shows how sensors are spread across the facility:

* Each of the six locations — *Assembly, Maintenance, Packaging, Storage, Testing, and Warehouse* — holds exactly *16.67%* of the sensors.
* This *even distribution* suggests that sensor placement is balanced and covers all major operational areas equally, which supports consistent monitoring.

---

#### 📋 Sensor Reference Table

* The table lists each *SensorID, its corresponding **SensorType, and the **Unit of Measurement*.
* This offers a quick-reference view for users to understand what each sensor measures, such as:

  * Pressure → Pa
  * Voltage → Volt
  * Temperature → Celsius

---

#### 📊 Failure Breakdown by Sensor Type (Bar Chart)

This bar chart groups the number of predicted failures by the type of sensor responsible:

* *Pressure sensors* are responsible for the highest number of predicted failures.
* *Temperature* and *Voltage sensors* contribute a moderate number.
* *Vibration sensors* trigger the fewest failure predictions.

> This distribution suggests that *pressure is the most volatile or sensitive parameter* being tracked, and might require closer attention or recalibration.

---

#### 📈 Sensor Readings Over Time (Line Chart)

This visual tracks how sensor readings have changed over time, divided by quarter (Q1–Q4):

* *Voltage and Pressure readings spike notably in Q3*, which may indicate seasonal workload stress, equipment overheating, or production peaks.
* *Temperature and Vibration readings remain more stable* throughout the quarters.
* The trends help identify *patterns that align with operational cycles*, allowing for more informed maintenance planning.

---

### 🧠 Summary

| Element         | What It Shows                                            |
| --------------- | -------------------------------------------------------- |
| KPI Cards       | Overall system health, sensor count, and failure alerts  |
| Donut Chart     | Equal sensor distribution across all factory locations   |
| Reference Table | Clear mapping between sensors, types, and units          |
| Bar Chart       | Pressure sensors dominate predicted failures             |
| Line Chart      | Voltage and pressure spike in Q3 — potential risk period |

---

This page provides both a macro and micro view of sensor-driven insights. It allows engineers, analysts, and decision-makers to *quickly assess health, **identify risky equipment, and **monitor trends across time and space*. Every visual contributes to a unified story about how sensor data can support predictive maintenance and reduce unplanned downtime.

---




## Published Dashboard
 [Click to View Live Report]([Click to View Live Report](https://app.powerbi.com/view?r=eyJrIjoiNzk4NzUwYzUtZjc1Yi00MjU0LWFmYjctZGQ5Y2RiY2I1MzQzIiwidCI6IjE2ZDgzZWU2LTI1NGEtNDY5ZC1hNmNjLTU0ZTJjYTIzMTNlNyIsImMiOjh9))

