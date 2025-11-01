# ⚡ Electric Vehicle Expense Analytics Dashboard (Power BI)

## 📘 Overview
The **Electric Vehicle Expense Analytics Dashboard** is a data-driven Power BI project designed to analyze and visualize the **total cost and expense distribution** of electric vehicles (EVs) across multiple companies and models.  

This project helps identify **key cost drivers**, track **yearly expense trends**, and **predict future cost movements** using advanced Power BI visuals and forecasting tools.  
It aims to provide **insights for manufacturers, policymakers, and analysts** to optimize EV pricing strategies and improve affordability.

---

## 🎯 Problem Statement
> The growing electric vehicle market faces rising production and operational costs.  
> Analyzing these expenses can help stakeholders identify major cost factors, optimize battery and maintenance costs, and predict future expense trends for better decision-making.

---

## 📊 Dashboard Objectives
- Analyze **total and average EV expenses** by company, model, and vehicle type  
- Compare **battery, maintenance, and charging costs**  
- Evaluate **company-wise cost efficiency**  
- Forecast **future expense trends** using historical data  
- Visualize cost distribution across different EV segments

---

## 🧩 Dataset Description
**File:** `electric_vehicle_analytics.csv`  
**Key Columns Used:**
| Column Name | Description |
|--------------|-------------|
| `Vehicle_ID` | Unique identifier for each EV |
| `Company_Name` | EV manufacturer (e.g., BMW, Tesla, Tata) |
| `Vehicle_Type` | EV segment (2W, 3W, 4W, etc.) |
| `Battery_Cost` | Cost of battery component |
| `Maintenance_Cost` | Annual maintenance expense |
| `Charging_Cost` | Energy and charging-related expense |
| `Total_Expense` | Sum of all cost components |
| `Year` | Year of record |

---

## ⚙️ DAX Measures Used
| Measure Name | Formula | Purpose |
|---------------|----------|----------|
| **Total Expense** | `SUM('EV_Data'[Total_Expense])` | Calculates total EV cost |
| **Avg Expense per Vehicle** | `DIVIDE([Total Expense], DISTINCTCOUNT('EV_Data'[Vehicle_ID]))` | Average cost per EV |
| **Avg Battery Cost** | `AVERAGE('EV_Data'[Battery_Cost])` | Mean battery expense |
| **Battery Cost %** | `DIVIDE(SUM('EV_Data'[Battery_Cost]), [Total Expense])` | Battery cost contribution |
| **Charging Cost %** | `DIVIDE(SUM('EV_Data'[Charging_Cost]), [Total Expense])` | Charging cost share |
| **Forecasted Expense Trend** | *(via Analytics Pane Forecast Line)* | Predicts upcoming expense trends |

---

## 📈 Visuals Included
1. **Expense Trend Over Time (Line Chart + Forecast)**
2. **Expense Breakdown by Company (Bar Chart)**
3. **Expense Composition by Type (Stacked Column)**
4. **Battery vs Charging Cost (Scatter Plot)**
5. **Average Expense by Vehicle Type (Column Chart)**
6. **Expense Distribution (Donut Chart)**
7. **Key Metrics Cards (KPIs)**  
   - Total Expense  
   - Average Expense per Vehicle  
   - Battery Cost %  
   - Maintenance Cost %

---

## 🧠 Insights Derived
- Battery costs account for the largest share of total EV expenses  
- Certain companies have achieved lower overall cost per vehicle  
- EV expenses show a moderate upward trend over years  
- Predicted expense growth can guide pricing and subsidy policies  

---

## 🧰 Tools & Technologies
- **Power BI Desktop**
- **Microsoft Excel / CSV**
- **DAX (Data Analysis Expressions)**
- **Forecasting via Analytics Pane**
- **Data Modeling and Transformation (Power Query)**

---

## 🚀 How to Use
1. Clone this repository  
   ```bash
   git clone https://github.com/Deepak2gr/EV-Expense-Analytics.git
