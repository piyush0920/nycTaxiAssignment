# 🚕 NYC Yellow Taxi Operations – Exploratory Data Analysis (Capstone Project)

## 📌 Project Overview

This project is an **end-to-end Exploratory Data Analysis (EDA)** of NYC Yellow Taxi trip data, created as a **capstone project** to demonstrate practical data analysis, data cleaning, and insight generation skills using Python.

The objective is to understand **travel demand patterns, revenue trends, operational inefficiencies, and geographic hotspots**, and to provide **data-driven recommendations** for optimizing taxi operations in New York City.

This repository showcases:

* Real-world data preparation techniques
* Structured EDA methodology
* Time-based and geospatial analysis
* Business-focused insights and recommendations

---

## 🎯 Objectives

* Clean and prepare large-scale real-world taxi data
* Identify demand patterns across **hours, days, months, and zones**
* Analyze **fare, tips, passenger behavior, and vendor patterns**
* Detect congestion-prone routes and operational inefficiencies
* Provide **actionable recommendations** for routing, dispatching, and pricing

---

## 🗂️ Dataset

* **Source:** NYC Yellow Taxi Trip Records (I have only used data from year 2023)

* **Link:**
The dataset is available from the [NYC Taxi & Limousine Commission][tlc-link].

[tlc-link]: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
* **Format:** Monthly CSV files
* **Size:** Very large (sampled for performance)
* **Key Features:**

  * Pickup & dropoff timestamps
  * Trip distance & duration
  * Fare components & tips
  * Passenger count
  * Pickup & dropoff zones

> A fixed sampling fraction and random state were used to maintain reproducibility while keeping the dataset computationally manageable.

---

## 🧰 Tools & Technologies

* **Python**
* **Pandas** – data manipulation
* **NumPy** – numerical operations
* **Matplotlib / Seaborn** – visualizations
* **GeoPandas** – spatial analysis
* **Jupyter Notebook** – analysis workflow

---

## 🔧 Methodology

### 1. Data Preparation

* Loaded multiple monthly CSV files
* Parsed datetime columns for time-based analysis
* Sampled and combined datasets
* Standardized column names and data types
* Reset and cleaned indexes

### 2. Data Cleaning

* Combined duplicate columns (e.g., airport fees)
* Handled missing values using domain-driven assumptions
* Removed invalid records (negative fares, distances, tips)
* Corrected common data entry issues

### 3. Exploratory Data Analysis

* Time-based demand analysis (hourly, daily, monthly trends)
* Revenue and quarterly contribution analysis
* Fare vs distance and tip behavior analysis
* Passenger count and payment type patterns
* Vendor-wise fare comparisons

### 4. Geospatial Analysis

* Integrated NYC taxi zone shapefiles
* Identified high-traffic pickup & dropoff zones
* Mapped spatial demand hotspots
* Analyzed pickup-to-dropoff imbalance

### 5. Advanced Insights

* Identified slow and congested routes using average speeds
* Compared weekday vs weekend traffic
* Analyzed night-time demand and revenue contribution
* Studied fare-per-mile patterns by time and vendor

---

## 📊 Key Insights

* Taxi demand follows **strong daily and weekly patterns**
* Peak activity occurs during **morning and evening commute hours**
* Certain zones consistently act as **high-demand hotspots**
* Credit card payments dominate both trips and revenue
* Night-time trips contribute a significant share of revenue
* Some zones experience consistent **pickup-dropoff imbalance**, indicating fleet rebalancing needs

---

## 📈 Business Recommendations

* Increase fleet availability during peak hours and high-demand zones
* Rebalance vehicles between pickup-heavy and dropoff-heavy zones
* Adjust routing strategies for consistently slow routes
* Support night-time demand around airports and transit hubs
* Use tiered pricing strategies for short vs long trips

---

## 📁 Repository Structure

```
├── EDA_Assg_NYC_Taxi_Starter_piyush_sharma.ipynb
├── Report_NYC_Taxi_Operations.pdf / .docx
├── README.md
```

---

## 📄 Project Report

A detailed report explaining methodology, analysis, visualizations, insights, and recommendations is included in this repository.


---

## 🚀 Future Improvements & Extension Ideas

If you want to enhance this project further, consider:

1. **PySpark Version**

   * Rebuild the analysis using PySpark for big data scalability

2. **Predictive Modeling**

   * Predict demand by hour or zone using regression or time-series models

3. **Dashboard**

   * Create an interactive dashboard using Power BI / Tableau / Streamlit

4. **Clustering**

   * Cluster zones based on demand and revenue patterns

5. **Real-Time Simulation**

   * Simulate taxi allocation strategies based on historical demand

6. **Cost Optimization**

   * Analyze fuel/time cost vs revenue to improve profitability

---

## 👤 Author

**Piyush Sharma**
Aspiring Data Analyst | Python | EDA | Business Analytics

📫 *Open to data analyst and analytics roles*

---

If you want, I can:

* Rewrite this README in a **more technical** or **more business-focused** tone
* Add **badges**, **screenshots**, or **dashboard links**
* Help you write a **GitHub project description** or **LinkedIn post** for this capstone
