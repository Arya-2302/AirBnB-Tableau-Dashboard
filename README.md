# 🏠 Airbnb Listings Analysis Dashboard

## Executive Summary

The **Airbnb Listings Analysis Dashboard** is an interactive business intelligence project designed to analyze Airbnb rental market trends using listing, review, and calendar datasets. The dashboard provides insights into property pricing, revenue generation, listing distribution, and geographic performance across different locations.

By transforming raw Airbnb data into actionable insights, this project demonstrates the application of data cleaning, data modeling, exploratory analysis, and dashboard development to support data-driven decision-making for hosts, investors, and property managers.

---

## 🎯 Business Objective

The primary objective of this project is to analyze Airbnb rental data and answer key business questions such as:

* How does property pricing vary based on the number of bedrooms?
* Which locations generate the highest rental prices?
* What are the revenue trends over time?
* How are listings distributed across different property sizes?
* Which geographic areas present the greatest investment opportunities?

The dashboard enables stakeholders to identify pricing patterns, evaluate market performance, and make informed business decisions.

---

## 📂 Dataset Overview

The project utilizes three interconnected datasets from the Airbnb Seattle market.

### Listings Dataset

Contains detailed information about Airbnb properties, including:

* Listing ID
* Property Name
* Listing URL
* Number of Bedrooms
* Zip Code
* Property Description
* Host Information

### Reviews Dataset

Contains customer review information, including:

* Listing ID
* Reviewer ID
* Reviewer Name
* Review Date
* Customer Comments

### Calendar Dataset

Contains property availability and pricing data, including:

* Listing ID
* Date
* Availability Status
* Daily Price

---

## 🔗 Data Model

The datasets were connected using **Listing ID** as the primary key.

```text
Listings
   │
   ├── Listing ID ── Reviews
   │
   └── Listing ID ── Calendar
```

This data model enabled integrated analysis of property details, customer feedback, and pricing behavior.

---

## 🧹 Data Preparation and Transformation

Data preprocessing was performed prior to analysis to ensure data quality, consistency, and reliability.

### Key Data Cleaning Activities

#### Removal of Invalid and Duplicate Records

* Removed duplicate entries across datasets.
* Eliminated records with incomplete or invalid information.

#### Handling Missing Values

* Identified and managed missing zip codes.
* Reviewed incomplete listing information.
* Validated availability and pricing records.

#### Price Data Transformation

The original price column contained currency symbols and text formatting.

Example:

```text
$125.00
$250.00
$89.00
```

Converted into numeric values for aggregation and analysis.

#### Date Standardization

* Standardized date formats across all datasets.
* Enabled accurate time-series and trend analysis.

#### Data Validation

Verified:

* Listing IDs
* Property attributes
* Pricing consistency
* Relationship integrity between tables

---

## 📈 Dashboard Components

### 1. Average Price per Bedroom

**Visualization:** Bar Chart

Displays the average property price for each bedroom category.

| Bedrooms | Average Price ($) |
| -------- | ----------------- |
| 1        | 96                |
| 2        | 175               |
| 3        | 250               |
| 4        | 315               |
| 5        | 450               |
| 6        | 585               |

**Insight:**
Property prices increase significantly as the number of bedrooms grows, indicating a strong relationship between property size and rental value.

---

### 2. Distribution of Listings by Bedroom Count

**Visualization:** Horizontal Bar Chart

Shows the number of Airbnb listings available for each bedroom category.

**Insight:**
One-bedroom properties dominate the market, representing the largest share of available listings.

**Business Value:**
Provides visibility into supply distribution and market demand patterns.

---

### 3. Average Price by Zip Code

**Visualization:** Bar Chart

Compares average rental prices across different zip codes.

**Insight:**
Certain neighborhoods command substantially higher rental rates than others due to factors such as location attractiveness, accessibility, and local demand.

---

### 4. Geographic Price Distribution

**Visualization:** Map

Provides a location-based view of pricing patterns across Seattle.

**Insight:**
Premium rental zones can be easily identified, helping investors and hosts evaluate market opportunities.

**Business Value:**
Supports location-based investment and pricing decisions.

---

### 5. Revenue Trend Analysis

**Visualization:** Time-Series Line Chart

Displays revenue performance throughout the year.

**Insight:**
Revenue demonstrates consistent growth and reaches approximately $2 million during the analyzed period.

**Business Value:**
Highlights overall market stability and demand trends within the Airbnb ecosystem.

---

## 📊 Key Metrics Analyzed

The dashboard focuses on several core performance indicators:

* Average Property Price
* Average Price per Bedroom
* Average Price per Zip Code
* Total Listings
* Revenue Trends
* Property Availability
* Geographic Performance

---

## 🛠️ Technology Stack

* **Tableau / Power BI** – Dashboard Development & Data Visualization
* **Microsoft Excel / CSV** – Data Storage and Processing
* **Data Cleaning & Transformation**
* **Data Modeling**
* **Trend Analysis**
* **KPI Development**
* **Business Intelligence & Reporting**

---

## 📷 Dashboard Preview

<img width="1821" height="731" alt="Dashboard 1" src="https://github.com/user-attachments/assets/beb04048-3248-4369-9e54-ed3df3c9432a" />

## 📁 Repository Structure

```text
Airbnb-Listings-Analysis/
│
├── Dataset/
│   ├── Listings.csv
│   ├── Reviews.csv
│   └── Calendar.csv
│
├── Dashboard/
│   └── Dashboard.png
│
├── Report/
│   └── AirBnB_Report.pdf
│
└── README.md
```
