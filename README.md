# 🏦 Bank Loan Risk Analysis Dashboard

### 📄 Executive Summary
This project analyzes a dataset of **500,000+ consumer loans** to identify trends in default rates and credit quality. The goal was to build a diagnostic tool for the Credit Risk Department to detect cohorts or segments driving portfolio loss.

**Key Business Insight:**
While the overall portfolio default rate is stable at **11%**, the **Vintage Analysis** revealed a critical deterioration in the **Q4-2015 cohort**, driven specifically by **'Small Business' loans in Grade G**, which exhibit a default rate exceeding **20%**.

---

### 📊 Dashboard Preview

![Dashboard Overview](https://github.com/zestcoderg/Bank-Loan-Risk-Analysis/blob/main/dashboard_overview.png.png)
*(To see the full interactive report, download the .pbix file from this repository)*

---

### ❓ Business Problem
The bank observed a rising volume of "Charged Off" accounts but lacked visibility into:
1.  **Which specific loan grades** were failing?
2.  **Was the risk increasing** over time (Vintage deterioration)?
3.  **Where** geographically and structurally (Purpose/Term) was the bad debt concentrated?

### 🛠️ Tech Stack
* **Tool:** Microsoft Power BI
* **Data Processing:** Excel (Advanced Cleaning, Text-to-Columns, Imputation)
* **Data Modeling:** Star Schema (Fact Table + Date Dimension)
* **Languages:** DAX (Data Analysis Expressions)

### 📈 Key Analysis Steps

#### 1. Data Engineering & Cleaning
* handled missing financial data by imputing interest rates based on Grade averages.
* Created a custom **"Risk Flag"** logic using DAX to categorize multiple status types (e.g., "Charged Off", "Default", "Late") into a binary Risk Metric.
* Standardized date formats from legacy systems to enable Time Intelligence functions.

#### 2. Vintage Analysis (Cohort Performance)
* Implemented **Time-Intelligence calculations** to track loan quality by "Issue Quarter".
* Identified that while 2014 cohorts were stable, the **Q4-2015 cohort** saw a 40% spike in defaults relative to the baseline.

#### 3. Root Cause Analysis (RCA)
* Designed a **Heatmap Matrix** to pinpoint the intersection of Loan Grade and Loan Purpose.
* **Finding:** The "Red Zone" is isolated to **Small Business loans** in high-risk grades (F & G), allowing for a targeted tightening of credit policy rather than a blanket freeze.

---

### 📉 Visual Insights

**Risk Heatmap (Grade vs Purpose):**
![Heatmap](https://github.com/zestcoderg/Bank-Loan-Risk-Analysis/blob/main/risk_heatmap.png.png)
*Clearly shows the high concentration of risk in specific segments.*

**Vintage Trend:**
![Vintage Chart](https://github.com/zestcoderg/Bank-Loan-Risk-Analysis/blob/main/Vintage%20Analysis.png)
*Visualizing the spike in default rates for late-2015 cohorts.*

---

### 💡 Conclusion & Recommendation
The analysis suggests that the rise in defaults is **not systemic** but rather tied to a specific loosening of underwriting standards for Small Business loans in late 2015. 
**Recommendation:** Temporarily suspend approvals for Grade F-G Small Business loans to stabilize the NPA (Non-Performing Asset) ratio.
