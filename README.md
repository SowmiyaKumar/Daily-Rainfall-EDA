# 🌧️ Daily Rainfall Data Cleaning & Exploratory Analysis (Australia)

**Course:** Practical Data Science with Python
**Type:** Individual Project
**Year:** 2024

---

## 📌 Project Overview

This project focuses on **cleaning, validating, and exploring 10 years of daily rainfall data (2013–2023)** for an Australian city.
The emphasis is on **robust data preparation**, handling real-world data quality issues, and performing **time-series exploratory data analysis (EDA)** to uncover seasonal and long-term rainfall patterns.

---

## 🎯 Objectives

* Detect and correct **data entry errors**, missing values, and physically impossible measurements
* Produce a **clean, analysis-ready rainfall dataset**
* Perform **time-series EDA** to analyse monthly, yearly, and long-term rainfall trends
* Visualise and interpret **seasonality, extremes, and trends**

---

## 🧑‍💻 My Role

* **Sole contributor**
* Owned the **entire data pipeline**:

  * Data cleaning
  * Validation
  * Imputation strategy
  * Exploratory analysis
  * Visualisation and interpretation

---

## 📂 Dataset

* **Source:** Australian Bureau of Meteorology (daily rainfall records); Provided as part of RMIT University coursework
* **Time span:** 2013 – 2023
* **Granularity:** Daily
* **Format:** CSV
* **Final size:**

  * **3866 rows × 4 columns**
  * Columns: `Year`, `Month`, `Day`, `Rainfall (mm)`

Two versions are included:

* **Raw dataset** (as received)
* **Cleaned dataset** (after full preprocessing)

---

## 🛠️ Tech Stack

* **Python**
* **Libraries:**

  * pandas
  * numpy
  * matplotlib
* **Environment:** Jupyter Notebook

---

## 🔎 Approach

### 1. Data Understanding

* Inspected structure and statistics using:

  * `.info()`, `.describe()`, `.value_counts()`
* Identified incorrect datatypes and suspicious values

### 2. Data Cleaning & Preparation

Handled multiple real-world issues:

* **Data entry errors**

  * Text values in numeric columns (e.g. `"Jan"`, `"April"`, `"nine"`)
* **Physically impossible values**

  * Invalid days (`48`, `200`)
  * Rainfall values like `-10 mm` and `100000 mm`
* **Missing values**

  * Missing dates in time-series (e.g. `2017/04/06`, `2013/06/01`)
  * Missing Month/Day entries handled via forward fill (`ffill`)
* **Outlier treatment**

  * Implausible rainfall values replaced with `NaN`
* **Imputation strategy**

  * Rainfall imputed using **month-level mean per year** to preserve seasonality

### 3. Data Exploration (EDA)

Conducted structured analysis using aggregation and visualisation:

* **Task 1:** Highest daily rainfall per month (2014)
* **Task 2:** Monthly and yearly rainfall trends (2015–2017)
* **Task 3:** Top 3 wettest and driest years
* **Task 4:** 10-year rainfall trend and seasonality

---

## 📊 Key Insights

* Strong **seasonal patterns**, with April and late-year months showing higher rainfall
* **2019** identified as one of the driest years
* **2020** recorded exceptionally high rainfall (~787 mm)
* Overall **upward trend** in annual rainfall over the last decade
* High variability across years, highlighting climate volatility

---

## 📈 Outputs

* Cleaned, analysis-ready rainfall dataset
* Multiple visualisations:

  * Monthly maxima
  * Yearly totals
  * Seasonal trend plots
* Fully documented Jupyter Notebook with reproducible steps

---

## 📁 Repository Structure

```text
Daily-Rainfall-EDA/
│
├── data/
│   ├── raw_rainfall_data.csv
│   └── cleaned_rainfall_data.csv
│
├── notebooks/
│   └── eda_notebook.ipynb
│
├── report/
│   └── Rainfall_EDA_Report.pdf
│
├── README.md

```

---
📜 License

This project is released under the MIT License.

  * All code in this repository is original work produced as part of RMIT University coursework.
  * The dataset is provided for educational and non-commercial use.
  * No proprietary RMIT teaching materials or assignment specifications are included.
