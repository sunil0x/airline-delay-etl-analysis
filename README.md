# ✈️ Airline Delay Data Analysis - Task

## 📌 Project Overview
This project analyzes an Airline Delay Dataset using a structured ETL pipeline and visual analytics to uncover patterns, causes, and trends in flight delays.

---

## 🛠 Task 1: Data Pipeline (ETL)

A simple data pipeline was created with the following steps:

### 1️⃣ Extract
- Loaded raw data from the Airline Delay Dataset.

### 2️⃣ Transform
- Removed duplicate rows:
  df.drop_duplicates()

- Handled missing values in numerical columns:
  df.fillna(0)

- Created a binary indicator column:
  is_delayed = 1  if arrival_delay > 15 minutes  
  is_delayed = 0  otherwise

### 3️⃣ Load
- Saved the cleaned dataset as:
  cleaned_airline_data.csv

---

## 📊 Visualizations

The following visualizations were generated using Seaborn:

### 🔥 Correlation Heatmap
- Analyzed relationships between:
  - Weather Delay
  - Carrier Delay
  - NAS Delay
  - Late Aircraft Delay
  - Total Arrival Delay

### 📉 Histogram
- Displayed the distribution of arrival delays.
- Result: Heavy right-skew (most flights have small delays).

### 📊 Bar Plot
- Compared average arrival delays across different airline carriers.

### 📦 Box Plot
- Showed spread and outliers in different delay causes.

### 📈 Line Plot
- Tracked average delay trends across months.

---

## 🔎 Data Insights (Q&A)

### ❓ Which airline is the "King of Delays"?
Based on the bar plot, WN has the highest average arrival delay, making it the least punctual carrier in this dataset.

### ❓ Is weather the biggest cause of delays?
No.

The heatmap and box plot show that:
- Late Aircraft Delay (domino effect)
- Carrier Delay

have stronger correlations and larger impacts on total delay than weather-related delays.

### ❓ Do delays get worse during specific months?
Yes.

The line plot shows peaks in:
- December (winter holidays)
- June/July (summer peak travel season)

This indicates seasonal demand increases delays.

### ❓ What is the most common passenger experience?
The histogram peaks around 0–15 minutes delay, meaning:

Most flights arrive nearly on time, despite the presence of extreme outliers.

---

## 📌 Conclusion

Although extreme delays exist, the majority of flights operate close to schedule. Operational inefficiencies (carrier and late aircraft delays) contribute more significantly to delays than weather conditions, and seasonal travel demand increases overall delay patterns.
