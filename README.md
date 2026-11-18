# GLOBAL ULTRA HIGH NET WORTH (UHNW) WEALTH DISTRIBUTION & ALPHA INVESTIGATION  🏦📊 

 **Author:** Elisha Alal, Data Analyst UEFI Global 
 **Role:** Data Analyst, UEFI Global  
**Tools:** SQL (SQLite / PostgreSQL), Relational Data Modeling, Quantitative Statistical Analysis  
**Dataset:** Forbes Top 200 Global Billionaires (`TOP_200_BILLIONAIRES.csv`)
![](introduction.jpg) 

## Initial Dataset Exploration
![](introduction_image.png)
## CONTENTS
* [Data Overview](Billionaires)
* [Project Overview](Project-Overview)
* [Business Problem](Business-Problem)
* [Project Objectives](Project-Objectives)
* [Analytical Questions](Analytical-Questions)
* [Dataset Description](Dataset-Description)
* [Tools and Technologies](Tools-and-Technologies)
* [Data Exploration and Methodology](Data-Exploration-and-Methodology)
* [SQL Analysis Images](SQL-Analysis-Files-Images)
* [Key Findings and Insights](Key-Findings-and-Insights)
* [Geographical Analysis](Geographical-Analysis)
* [Industry Analysis](Industry-Analysis)
* [Business Implications](Business-Implications)
* [SQL Skills Demonstrated](SQL-Skills-Demonstrated)
* [Repository Structure](Repository-Structure)
* [How to Explore the Project](How-to-Explore-the-Project)
* [Assumptions and Limitations](Assumptions-and-Limitations)
* [Conclusion](Conclusion)
* [Author](Author)
## DATA OVERVIEW
This project explores the world's 200 richest people using Microsoft SQL Server. The analysis examines billionaire wealth distribution, age demographics, geographical representation and industry classifications through structured SQL queries.

Using a dataset containing 200 billionaire records, the project investigates patterns in individual net worth, country representation, industry concentration and demographic characteristics.

The analysis applies SQL querying, filtering, sorting, aggregate functions, grouping, conditional logic and subqueries to extract meaningful information from the dataset.
MICRO MACRO AND GLOBAL - MARKET FAILURE 

---

##  Executive Summary & Business Mandate
![](introduction_image.png)
As a Data Analyst within a premier Global Wealth Management division, my mandate was to analyze the global Ultra-High-Net-Worth (UHNW) landscape across the world’s 200 wealthiest individuals (representing **$6,368.50 Billion** in aggregate capital). 

By moving beyond surface-level descriptive metrics into **quantitative concentration risk, generational wealth velocity, and sector dispersion**, this investigation provides actionable intelligence for private wealth advisory, family office coverage, and sector-focused capital allocation.

### Key Headline Metrics
![](introduction_image.png)
* **Total Addressable UHNW Capital (Top 200):** $6,368.50 Billion
* **Mean Net Worth:** $31.84 Billion *(vs. Median skew driven by mega-cap outliers)*
* **Mean Principal Age:** 69.38 Years
* **Centibillionaire Tier ($100B+):** 14 Individuals controlling **$1,973.00 Billion** (30.98% of total pool)

---

##  Data Architecture & Schema
![](introduction_image.png)
The analysis was conducted on a structured relational table (`TOP_200_BILLIONAIRES`) comprising 200 records across 7 attributes:

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `serial_number` | `INTEGER` | Sequential record identifier (1–200) |
| `rank` | `INTEGER` | Global Forbes wealth ranking |
| `name` | `TEXT` | Principal billionaire or family dynasty name |
| `age` | `INTEGER` | Current age of the primary wealth holder |
| `country` | `TEXT` | Primary country of citizenship / residence |
| `networth_billion_US_dollars` | `REAL` | Total net worth denominated in USD Billions |
| `industry` | `TEXT` | Primary sector of wealth generation |

---

## Part I: Core Wealth Management & Demographic Findings
![](introduction_image.png)
### 1. Geographic Capital Concentration
![](introduction_image.png)
Wealth among the top 200 is heavily concentrated in North America and major Asian/European hubs. Only **8 countries** host five or more top-200 billionaires:

| Rank | Country | Billionaire Count | Combined Wealth ($B) \vert{} Avg Wealth / Principal ($B) |
| :--- | :--- | :---: | :---: | :---: |
| 1 | **United States** | 79 | $3,130.90B | $39.63B |
| 2 | **China** | 17 | $387.40B | $22.79B |
| 3 | **India** | 13 | $434.50B | $33.42B |
| 4 | **Germany** | 11 | $248.20B | $22.56B |
| 5 | **Russia** | 11 | $224.50B | $20.41B |
| 6 | **France** | 7 | $478.80B | $68.40B |
| 7 | **Hong Kong** | 7 | $139.30B | $19.90B |
| 8 | **Australia** | 5 | $100.20B | $20.04B |

> **Advisory Takeaway:** While the **United States** accounts for **39.5%** of all principals and **49.16%** of total capital, **France** exhibits the highest capital efficiency among multi-billionaire nations at **$68.40B per principal**, anchored by luxury retail conglomerates.

---

### 2. Sector Dominance & Capital Engines
![](introduction_image.png)
**Technology**, **Finance & Investments**, and **Fashion & Retail** account for **51% (102 of 200)** of all UHNW principals:
![](introduction_image.png)
| Industry Sector | Principal Count | Combined Wealth ($B) | Dominant Geography |
| :--- | :---: | :---: | :--- |
| **Technology** | 40 | $1,738.80B | United States ($1,376.7B) |
| **Finance & Investments** | 32 | $976.30B | United States ($630.5B) |
| **Fashion & Retail** | 30 | $1,165.50B | France ($453.3B) |
| **Food & Beverage** | 15 | $402.10B | United States ($110.6B) |
| **Diversified** | 15 | $579.10B | India ($219.7B) |

---

### 3. Generational Segmentation & Succession Pipeline
![](introduction_image.png)
Segmenting principals by age reveals critical insights for **Estate Planning, Trust Structuring, and Next-Gen Wealth Transfer**:

| Generational Tier | Principal Count | Combined Wealth ($B) \vert{} Avg Net Worth ($B) |
| :--- | :---: | :---: | :---: |
| **60 – 79 (Senior Leaders)** | 100 | $3,291.60B | $32.92B |
| **80+ (Legacy / Succession Tier)** | 49 | $1,453.40B | $29.66B |
| **40 – 59 (Prime Career)** | 46 | $1,345.10B | $29.24B |
| **Under 40 (Next-Gen Disruptors)** | 5 | $278.40B | $55.68B |

* **Succession Opportunity:** **74.5% of the dataset (149 principals)** are aged **60 or older**, representing **$4,745.00B** in assets requiring active intergenerational wealth transfer and estate advisory over the next decade.

* **Family Dynasty Footprint:** **43 entries** explicitly operate as multi-generational family offices (`& family`), controlling **$1,507.80B** (averaging **$35.07B**—exceeding the overall dataset mean of $31.84B).
![](introduction_image.png)
---

## Part II: Quantitative & Risk Analytics (Quant Perspective)
![](introduction_image.png)
To evaluate structural risk and wealth generation efficiency, five quantitative models were engineered directly in SQL:

1. **Tail Risk & Power-Law Skewness:**
   * The **Top 5 principals** (2.5% of sample) control **$940.00B (14.76%)** of total wealth.
   * The **Top 10 principals** (5.0% of sample) control **$1,552.00B (24.37%)** of total wealth.
   * **53 principals** exceed the dataset mean of $31.84B, confirming a heavily right-skewed power-law distribution.
   ![](introduction_image.png)
2. **Alpha Generation Velocity ($\text{Net Worth} / \text{Age}$):**
   ![](introduction_image.png)
   * Measuring capital accumulation per year of life isolates high-velocity wealth creators from legacy compounding.
   * **Mark Zuckerberg** leads globally at **$4.54B/year** (Age 39, $177B), followed by **Elon Musk** at **$3.75B/year** (Age 52, $195B) and **Jeff Bezos** at **$3.23B/year** (Age 60, $194B).
4. **Sector Dispersion & Volatility:**
   ![](introduction_image.png)
   * **Automotive** ($\sigma = \$56.62\text{B}$) and **Technology** ($\sigma = \$50.00\text{B}$) display the widest internal net-worth dispersion, reflecting "winner-take-all" market dynamics compared to lower-variance sectors like Metals & Mining.
6. **Market Concentration (HHI Proxy):**
   ![](introduction_image.png)
   * Niche sectors such as **Telecom** ($102.0B avg) exhibit single-entity dominance, whereas **Technology** and **Finance** demonstrate deep, multi-principal liquidity pools.

---

## Strategic Wealth Management Recommendations
![](introduction_image.png)
1. **Prioritize Legacy Succession Advisory (Age 75+ Cohort):** Target the 49 principals in the 80+ cohort ($1.45T AUM pool) with bespoke multi-generational trust, philanthropic foundation, and tax-efficient inheritance structures.
![](introduction_image.png) 
2. **Dedicated Tech & Founder Liquidity Desks:** With 40 Tech principals ($1.74T) and high wealth velocity among under-50 founders ($508.3B total wealth under age 50), advisory teams should specialize in concentrated stock hedging, pre-IPO/post-IPO liquidity management, and venture co-investment vehicles.
![](introduction_image.png)
3. **Expand Cross-Border European & Asian Family Office Coverage:** While US coverage remains foundational, high average net worth per principal in **France ($68.40B)** and rapid conglomerate growth in **India ($434.50B total)** warrant dedicated regional private banking teams.
![](introduction_image.png)

---

## 🛠️ Repository Structure & Execution

```text
├── README.md                     # Executive report & analytical summary
├── TOP_200_BILLIONAIRES.csv      # Raw Forbes Top 200 dataset
└── wealth_analysis.sql           # Complete SQL script (Core, Business, & Quant queries)
