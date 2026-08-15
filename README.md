# 🌍 Multi-Source Environmental & Public Health Data Analysis (India)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

## 📌 Project Overview
This project presents an end-to-end exploratory data analysis (EDA) examining the interrelationships between **Air Quality Index (AQI)**, **Vehicle Density (Vahan)**, **Public Health Outbreaks (IDSP)**, and **Demographic Projections** across various Indian states and metropolitan cities.

The objective is to derive data-driven insights on seasonal pollution trends, weekend-vs-weekday air quality shifts, disease correlates, and regional environmental severity mapping.

---

## 📊 Datasets Analyzed

| Dataset | File Name | Description | Key Features |
| :--- | :--- | :--- | :--- |
| **AQI Data** | `aqi.csv` | Daily monitoring station metrics across Indian areas | `date`, `state`, `area`, `aqi_value`, `prominent_pollutants`, `air_quality_status` |
| **Vahan Data** | `vahan.csv` | Vehicle registration records by state and RTO | `year`, `month`, `state`, `vehicle_class`, `fuel`, `value` |
| **IDSP Data** | `idsp.csv` | Integrated Disease Surveillance Programme outbreak records | `year`, `week`, `state`, `disease_illness_name`, `cases`, `deaths` |
| **Population Projection** | `population_projection.csv` | State-wise demographic growth estimates up to 2036 | `year`, `month`, `state`, `gender`, `value` |

---

## 🔑 Key Findings & Analysis Highlights

### 1. AQI Extremes (Dec 2024 – May 2025)
* **Top 5 Worst Affected Areas (Highest Mean AQI):** Byrnihat (284.19), Delhi (238.92), Hajipur (233.67), Bahadurgarh (226.44), Gurugram (204.14).
* **Bottom 5 Cleanest Areas (Lowest Mean AQI):** Tirunelveli (33.31), Palkalaiperur (42.79), Madikeri (42.95), Vijayapura (44.33), Chamarajanagar (44.81).

### 2. Southern India Prominent Pollutants
* Across Southern states (**Andhra Pradesh, Karnataka, Kerala, Tamil Nadu, Telangana**), **PM10** and **PM2.5** emerge as the most dominant pollutants, followed by Carbon Monoxide (CO).

### 3. Weekday vs. Weekend AQI (Metro Cities)
* Mixed patterns observed across major metros over a 1-year period:
  * **Improvement on Weekends:** Delhi (208.7 → 198.9), Chennai (71.2 → 68.4), Kolkata, Pune.
  * **Slight Increase on Weekends:** Ahmedabad, Bengaluru, Hyderabad, Mumbai.

### 4. Critical Pollution Months
* **November & December** consistently exhibit the highest average AQI values across top-monitored Northern and Central states (e.g., Delhi, UP, Haryana, Bihar, Rajasthan).

---

## 🛠️ Data Pipeline & Workflow

1. **Data Ingestion & Preprocessing:**
   * Encoding normalization (Latin-1/UTF-8 handling).
   * Date-time parsing and feature extraction (`Year`, `Month`, `DayOfWeek`).
2. **Aggregation & Temporal Filtering:**
   * 6-month moving windows, rolling averages, and state-level groupby operations.
3. **Cross-Domain Correlation:**
   * Merging AQI indices with IDSP health reports and Vahan vehicle registration metrics.

---

## 🚀 How to Run

### Prerequisites
Make sure you have Python installed along with the required libraries:
```bash
pip install pandas numpy matplotlib seaborn
