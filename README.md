# Emission-Forecasting-for-Fossil-Fuel

# 🌍 Emission Forecasting for Fossil Fuel Electricity Sector (2000–2030)

## Akshit Bhandari (Machine Learning Analyst)

---

## 📌 Project Objective

This project forecasts pollutant emissions from *Canada’s fossil fuel electricity generation sector, especially under the scenario of **phasing out coal power plants by 2030. Using Environment Canada’s **National Pollutant Release Inventory (NPRI)* data (2000–2022), we analyzed historical emission patterns and predicted future releases with the goal of supporting data-driven climate policy decisions.

---

## 🧱 Key Steps & Deliverables

### 1️⃣ Data Cleaning & Integration
- Combined two datasets: release_dataset.csv and disposals_dataset.csv.
- Standardized formats, removed irrelevant fields, and joined on Facility Name, NPRI_ID, and Reporting Year.
- Handled missing values using:
  - *Mode* (for categorical)
  - *Median* (for numerical)
  - ffill and bfill (for time series continuity)

### 2️⃣ Feature Engineering
- Created binary flags like:
  - is_coal: Identifies coal-related pollutants
  - is_fossil_fuel: Flags fossil fuel entries by NAICS Title
- Constructed total_release by summing across air, land, and water categories
- Engineered year-based group averages (avg_sector_release)

### 3️⃣ Outlier Treatment
- Used *Interquartile Range (IQR)* to detect outliers
- Replaced outlier values with column medians for smoother model training

### 4️⃣ Data Encoding & Scaling
- Encoded categorical variables using LabelEncoder
  - Province, Substance Name (English), NAICS Title
- Applied StandardScaler to numeric features to normalize the dataset for regression

---

## 📊 Modeling Strategy

### Classification (Phase 1)
- Binned continuous release values into emission levels (e.g., low, medium, high)
- Helped identify feature importance before full regression modeling

### Regression (Phase 2)
- Trained three regression models:
  - ✅ *Linear Regression* (Best)
  - 🌲 Decision Tree Regressor
  - 🌲 Random Forest Regressor
- *Linear Regression* performed best:
  - *MAE*: 2291.28  
  - *RMSE*: 2748.41  
  - *R²*: 0.476  
  - *Accuracy*: 95.76%

---

## 📈 Key Visual Insights

- 📉 *Air emissions peaked around 2004–2005*, then declined sharply.
- 📊 Land and water emissions remained mostly stable.
- 🔄 After 2010, a noticeable drop occurred across all pollution types.
- 📅 Forecast for 2023–2030 shows a *steady downward trend*, validating the effectiveness of coal phase-out initiatives.

---

## 🔍 Sample Visualizations

- *Line Graph*: Total emissions over time (2000–2030)
- *Bar Plot*: Emissions by province
- *Scatter Plot*: Feature correlation with pollutant levels

---

## 🧠 Key Takeaways

- 🧼 Solid preprocessing and feature engineering enabled robust predictions
- 📉 Emissions expected to *continue declining if coal is phased out*
- 🧪 Linear models provided interpretable results that support sustainable energy policies
- 📊 Visuals supported policy-focused storytelling

---

## 📞 Contact

*Akshit Bhandari*  
📧 abhandari78@norquest.ca 
📞 +1 (437) 970-9974

---
