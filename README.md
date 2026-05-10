```markdown
# FedEx Logistics Performance Analysis

![Project Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Built With](https://img.shields.io/badge/Built%20With-Python-blue)

## Table of Contents
- [Overview](#overview)
- [Project Goal](#project-goal)
- [Dataset](#dataset)
- [Key Analyses & Insights](#key-analyses--insights)
- [Solutions & Approaches for Improvement](#solutions--approaches-for-improvement)
- [Technical Stack](#technical-stack)
- [How to Use](#how-to-use)

## Overview
This project delves into the operational efficiency of FedEx's logistics through a comprehensive analysis of a rich dataset. Spanning 10,324 rows and 33 columns, the dataset captures intricate details of shipment records, including Project Codes, Purchase Order numbers, countries of delivery, shipment modes, vendor terms, line item quantities, freight costs, unit prices, and manufacturing sites. Our objective is to unearth patterns in shipping performance, identify variations in cost, and assess delivery reliability to provide actionable insights. This analysis aims to strategically enhance supply chain planning, optimize cost controls, and elevate FedEx's overall logistics performance.

## Project Goal
The primary goal of the FedEx Logistics Performance Analysis is to evaluate and improve the efficiency, reliability, and cost-effectiveness of FedEx's delivery services by analyzing their operational logistics data.

## Dataset
The dataset used for this analysis is `SCMS_Delivery_History_Dataset.csv`.

### Data Points Include:
-   **Shipment Identifiers**: ID, Project Code, PQ #, PO / SO #, ASN/DN #
-   **Geographical Information**: Country, Manufacturing Site
-   **Logistics Details**: Managed By, Fulfill Via, Vendor INCO Term, Shipment Mode
-   **Date & Time**: PQ First Sent to Client Date, PO Sent to Vendor Date, Scheduled Delivery Date, Delivered to Client Date, Delivery Recorded Date
-   **Product Information**: Product Group, Sub Classification, Vendor, Item Description, Molecule/Test Type, Brand, Dosage, Dosage Form, Unit of Measure (Per Pack)
-   **Financials & Quantities**: Line Item Quantity, Line Item Value, Pack Price, Unit Price, Freight Cost (USD), Line Item Insurance (USD)
-   **Physical Attributes**: Weight (Kilograms)
-   **Status Flags**: First Line Designation

## Key Analyses & Insights
Through a methodical approach to data exploration, cleaning, and feature engineering, we've uncovered several critical insights:

1.  **Data Quality Assessment**: Identified and addressed missing values in key columns like 'Shipment Mode', 'Dosage', and 'Line Item Insurance (USD)'. We also corrected illogical `Processing_Days` values (where `PQ First Sent to Client Date` was before `PO Sent to Vendor Date`).
2.  **Time-Based Feature Engineering**: Extracted year, month, day, day of week, week of year, and weekend indicators from all date columns to enable deeper temporal analysis.
3.  **Correlation Analysis**: Examined relationships between numeric variables to understand dependencies and potential drivers of costs and delays.
4.  **On-time Delivery Performance**: Analyzed on-time delivery rates across different `Managed By` teams, `Shipment Modes`, and `Countries`, revealing varying levels of efficiency.
5.  **Delay Analysis**: Quantified average delay times by country, highlighting regions with persistent delivery challenges.
6.  **Cost per Unit Analysis**: Calculated and analyzed 'Cost per Unit' to standardize cost comparisons across various product groups and vendors.
7.  **Geographical Visualization**: Utilized choropleth maps to visually represent average processing days and on-time delivery rates by country, identifying geographical patterns and disparities.

## Solutions & Approaches for Improvement
Based on our analysis, we propose the following strategies:

1.  **Data Quality & Process Improvement**: Implement robust data validation for date fields and standardize input formats for 'Weight (Kilograms)' and 'Freight Cost (USD)' to prevent inconsistencies.
2.  **Vendor Performance Optimization**: Establish KPIs for processing days, on-time delivery, and cost efficiency. Collaborate with underperforming vendors to identify root causes and implement improvement plans.
3.  **Shipment Mode & Route Optimization**: Develop dynamic strategies for selecting shipment modes and routes based on destination country performance, urgency, and cost, leveraging historical data to inform decisions.
4.  **Product Group Specific Logistics Strategies**: Tailor logistics approaches to the unique needs of different product groups (e.g., prioritize faster modes for high-value/time-sensitive items, optimize for cost for less critical goods).
5.  **Advanced Analytics & Predictive Modeling**: Build machine learning models to forecast demand, predict potential delays, and optimize resource allocation proactively, enhancing supply chain resilience.

## Technical Stack
-   **Python**: Programming language
-   **Pandas**: Data manipulation and analysis
-   **NumPy**: Numerical operations
-   **Matplotlib**: Data visualization
-   **Seaborn**: Enhanced data visualization
-   **Plotly Express**: Interactive geographical visualizations

## How to Use
To explore this analysis:
1.  Clone this repository to your local machine.
2.  Open the `.ipynb` notebook in Google Colab or any Jupyter-compatible environment.
3.  Ensure all required Python libraries are installed (`pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`).
4.  Run the cells sequentially to reproduce the analysis and visualizations.

Feel free to reach out for any questions or collaborations!
```
