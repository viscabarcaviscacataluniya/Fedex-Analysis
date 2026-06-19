# FedEx Logistics Performance Analysis

## Overview

This project analyzes FedEx logistics and supply chain operations using a large-scale shipment dataset containing over **10,000 delivery records** and **33 operational features**. The analysis focuses on identifying inefficiencies in delivery performance, shipment delays, freight costs, and vendor operations through data cleaning, feature engineering, exploratory analysis, and geographical visualization.

The goal of the project is to transform raw logistics data into actionable operational insights that improve delivery reliability, optimize transportation costs, and support strategic supply chain decision-making.

---

# Business Problem

Modern logistics networks operate across multiple countries, vendors, shipment modes, and manufacturing sites, making operational efficiency difficult to monitor at scale.

FedEx faces challenges such as:

* Inconsistent delivery timelines
* Shipment delays across regions
* Variability in freight costs
* Vendor performance inefficiencies
* Data quality inconsistencies in operational systems

This project aims to address these challenges through data-driven analysis and operational intelligence.

---

# Objectives

The primary objectives of this project are:

* Analyze shipment performance and delivery reliability
* Identify operational bottlenecks causing delays
* Evaluate cost efficiency across shipment modes and vendors
* Measure country-wise logistics performance
* Standardize cost analysis using derived business metrics
* Build a foundation for predictive supply chain optimization

---

# Dataset Information

### Dataset

`SCMS_Delivery_History_Dataset.csv`

### Dataset Scale

* **Rows:** 10,324
* **Columns:** 33

### Key Features

#### Shipment Information

* Project Code
* PO / SO Number
* ASN / DN Number
* Shipment ID

#### Logistics Attributes

* Shipment Mode
* Vendor INCO Terms
* Fulfillment Method
* Managed By

#### Geographical Features

* Country
* Manufacturing Site

#### Financial Metrics

* Freight Cost (USD)
* Line Item Value
* Unit Price
* Insurance Cost

#### Time Features

* Scheduled Delivery Date
* Delivered to Client Date
* PO Sent Date
* Delivery Recorded Date

#### Product Information

* Product Group
* Brand
* Dosage
* Molecule/Test Type

---

# Technical Stack

| Category              | Technologies                    |
| --------------------- | ------------------------------- |
| Programming           | Python                          |
| Data Processing       | Pandas, NumPy                   |
| Visualization         | Matplotlib, Seaborn             |
| Interactive Analytics | Plotly Express                  |
| Notebook Environment  | Jupyter Notebook / Google Colab |

---

# Data Engineering & Preprocessing

## Data Cleaning

Performed comprehensive preprocessing to improve dataset quality:

* Handled missing values in critical logistics fields
* Corrected invalid or inconsistent date relationships
* Standardized numerical columns
* Removed illogical processing records
* Fixed datatype inconsistencies

## Feature Engineering

Generated additional operational features including:

* Processing Days
* Delivery Delay
* Cost per Unit
* Weekday / Weekend indicators
* Month, Quarter, and Year features
* Week-of-Year analytics

These derived metrics enabled deeper operational and temporal analysis.

---

# Exploratory Data Analysis

## 1. Delivery Performance Analysis

Evaluated on-time delivery rates across:

* Shipment Modes
* Countries
* Vendors
* Operational Teams

### Key Insight

Certain shipment modes consistently underperformed in specific regions, indicating route-level inefficiencies.

---

## 2. Delay Analysis

Measured average delivery delays by country and logistics configuration.

### Key Insight

Several regions exhibited significantly higher processing times, suggesting infrastructure or customs-related bottlenecks.

---

## 3. Freight Cost Optimization

Analyzed freight costs relative to:

* Shipment weight
* Product categories
* Shipment modes
* Vendor operations

### Key Insight

Air shipments delivered faster turnaround times but introduced disproportionately higher freight costs for low-priority products.

---

## 4. Correlation Analysis

Performed correlation analysis across numerical operational metrics.

### Observations

* Freight cost strongly correlated with shipment weight
* Longer processing times increased total logistics cost
* Certain vendors demonstrated higher operational consistency

---

## 5. Geospatial Analysis

Built choropleth visualizations to analyze:

* Country-wise processing delays
* On-time delivery performance
* Regional logistics efficiency

### Key Insight

Geographical patterns revealed clear disparities in supply chain efficiency across regions.

---

# Business Recommendations

## 1. Vendor Performance Monitoring

Introduce KPI-based vendor evaluation frameworks using:

* On-time delivery %
* Average processing time
* Freight cost efficiency
* Delay frequency

---

## 2. Intelligent Shipment Mode Selection

Develop rule-based or ML-driven shipment optimization systems that dynamically choose:

* Cost-efficient routes
* Optimal shipment modes
* Delivery-time-aware transportation methods

---

## 3. Data Quality Governance

Implement validation pipelines for:

* Date consistency
* Freight cost anomalies
* Missing operational records
* Weight standardization

---

## 4. Predictive Supply Chain Analytics

Future improvements may include:

* Delivery delay prediction models
* Demand forecasting
* Logistics cost forecasting
* Route optimization algorithms

---

# Key Outcomes

* Improved visibility into logistics inefficiencies
* Identified high-delay regions and shipment bottlenecks
* Standardized operational cost analysis
* Built scalable analytical workflows for logistics intelligence
* Established a strong foundation for predictive supply chain optimization

---

# Future Enhancements

Potential future work includes:

* Machine Learning-based ETA prediction
* Real-time logistics dashboards
* Supply chain anomaly detection
* Route optimization using graph algorithms
* Automated KPI monitoring pipelines

---

# Repository Structure

```bash
FedEx-Logistics-Analysis/
│
├── data/
│   └── SCMS_Delivery_History_Dataset.csv
│
├── notebooks/
│   └── fedex_logistics_analysis.ipynb
│
├── visualizations/
│   └── charts_and_maps/
│
├── README.md
└── requirements.txt
```

---

# How to Run

## 1. Clone Repository

```bash
git clone <repository-url>
```

## 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn plotly
```

## 3. Launch Notebook

```bash
jupyter notebook
```

Open the notebook and execute cells sequentially.

---

# Conclusion

This project demonstrates how data analytics can be applied to large-scale logistics operations to uncover operational inefficiencies, optimize transportation strategies, and improve supply chain reliability.

By combining data preprocessing, feature engineering, visualization, and operational analytics, the project provides actionable business insights that can support intelligent logistics decision-making at enterprise scale.
