# E-Commerce-Product-Intelligence-BI-Reporting-Dashboard
## Project Overview
This repository contains a multi-layered Business Intelligence (BI) and reporting application built in Power BI. Analyzing over 100,000 e-commerce transactions from the Brazilian marketplace Olist, this project transitions raw data into an interactive product analytics tool. The primary objective is to diagnose the root causes of customer churn, track market shifts across product categories, and provide executives with a transparent view of true user retention.

## Business Value & Objectives
* Product Analytics: Identified product categories driving long-term customer loyalty versus categories causing high single-purchase churn.

* Logistics Diagnostics: Analyzed the correlation between high freight costs and customer retention drop-offs.

* Enterprise Reporting: Built a scalable, intuitive interface for stakeholders ranging from C-suite executives to regional marketing leads.

## Strategic Business Decisions Enabled
This reporting suite empowers stakeholders to move beyond passive observation and make active, data-driven decisions:

* Targeted Marketing Spend: By identifying which product categories are gaining rank over time, marketing teams can confidently allocate ad budgets to high-momentum products.

* Logistics & Freight Renegotiation: The Friction Analysis scatter plot allows supply chain managers to pinpoint exactly which product categories require immediate freight cost renegotiations to prevent customer drop-off.

* Localized Inventory Planning: Using the Regional Heatmap and Drill-Through diagnostics, regional managers can identify top-selling categories in specific states to optimize local warehouse inventory and reduce shipping times.

* Catalog Optimization: The AI Decomposition Tree helps product stakeholders distinguish between "loyalty-driving" products and "one-and-done" purchases, guiding decisions on vendor contracts and catalog expansion.

## Dashboard Architecture & UI/UX
The application is structured into three distinct analytical layers, utilizing a cohesive, modern UI/UX design (the "Everest Group" aesthetic) featuring custom navigation, strategic color isolation, and soft-bloom backgrounds.

### Page 1: Executive Summary
Provides a high-level, 10-second overview of business health for leadership.

* KPI Cards: Dynamic tracking of Total Revenue, Total Customers, and True Retention Rate.

* Segmentation: Donut charts isolating one-time buyers from repeat customers.

* Regional Heatmap: A conditional-formatted matrix highlighting customer loyalty by state.

  ![Executive Summary Dashboard](Dashboard%20Images/Olist%20Product%20Retention%20Dashboard.png)

### 2. Page 2: Product & Churn Diagnostics (Deep-Dive)
A highly technical page built to investigate drivers of churn.

* AI Decomposition Tree: Allows dynamic breakdown of retention rates across product categories, states, and individual cities.

* Friction Analysis (Scatter Plot): Correlates average freight costs against retention rates by product category to identify logistics bottlenecks.

* Market Shift (Ribbon Chart): Tracks the ranking and revenue shifts of top product categories over mature operational months.

  ![Retention Drivers](Dashboard%20Images/Retention%20drivers%20and%20retention.png)

### 3. Page 3: Regional Profile (Hidden Drill-Through)
An isolated reporting layer designed for targeted local analysis.

* Stakeholders can right-click any state on the main dashboard to "drill through" to this hidden page.

* Dynamically filters all KPIs, local catalog top-sellers, and revenue trends strictly to the selected region using advanced SELECTEDVALUE DAX measures.

  ![Regional Deep Dive Drill Through](Dashboard%20Images/Regional%20deep%20dive%20drill%20through.png)

## Technical Stack & Skills Demonstrated
Business Intelligence & Reporting

* Tool: Power BI Desktop

*Data Transformation: Power Query (ETL pipeline for cleaning and standardizing raw transaction data)

* Data Modeling: Optimized Star Schema architecture (Fact tables and Dimension tables)

   * Advanced DAX (Data Analysis Expressions)

   * Engineered robust measures to handle evaluation contexts and prevent data aggregation errors.

* Key DAX Highlight: Redefined the standard retention calculation. Moved away from basic "Basket Size" (row counting) to true user retention by utilizing DISTINCTCOUNT on order_purchase_timestamp to accurately track separate customer visits.

## UI/UX & Interactive Design

Engineered Cross-Filtering and Drill-Through functionalities.

Implemented custom tooltip formatting and dynamic header generation.

Designed a custom enterprise theme utilizing strategic to guide stakeholder focus.

## Dataset Information
The dataset used for this BI application is the Olist E-Commerce Public Dataset.

Scope: ~100k orders spanning from 2016 to 2018.

Dimensions: Customers, Products, Locations, and Time.

* Note: Startup-phase data (2016) was systematically excluded from trend analyses via page-level filtering to ensure diagnostic accuracy and prevent timeline skewing.
