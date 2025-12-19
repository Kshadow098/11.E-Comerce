# 🛒 E-Commerce: Hypothesis Prioritization & A/B Testing

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458.svg)
![SciPy](https://img.shields.io/badge/Stats-SciPy-red.svg)
![Matplotlib](https://img.shields.io/badge/Viz-Matplotlib-11557c.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

## 📖 Project Overview
I work as a Data Analyst for a major online store. The marketing department has compiled a list of hypotheses to boost revenue, but we cannot test them all at once due to budget constraints.

This project is divided into two key phases:
1.  **Prioritization:** Using the **ICE** and **RICE** frameworks to select the most promising hypothesis.
2.  **A/B Testing:** Analyzing the results of an A/B test executed on the selected hypothesis to determine if the changes significantly increased revenue or conversion rates.

## 📂 Data Description
The analysis uses three datasets:
* **`hypotheses_us.csv`**: Contains 9 marketing hypotheses with scores (1-10) for *Reach*, *Impact*, *Confidence*, and *Effort*.
* **`orders_us.csv`**: Transaction data including `revenue`, `date`, `group` (A/B), and `visitorId`.
* **`visits_us.csv`**: Daily traffic data per group.

## 🛠️ Methodology
**Tools:** Python, Pandas, Matplotlib, SciPy (Mann-Whitney U Test).

### Part 1: Prioritization of Hypotheses
* Calculated **ICE Score**: $(Impact \times Confidence) / Effort$.
* Calculated **RICE Score**: $(Reach \times Impact \times Confidence) / Effort$.
* **Comparison:** Analyzed how the prioritization ranking changes when the **Reach** factor is included (RICE vs. ICE).

### Part 2: A/B Test Analysis
* **Data Preprocessing:** Checked for users present in both groups (A and B) to ensure data integrity.
* **Cumulative Metrics:** Plotted cumulative revenue, average order size, and conversion rates to check for stability.
* **Anomaly Detection:** Used the **95th and 99th percentiles** to identify outliers in the number of orders per user and order prices.
* **Statistical Significance:**
    * Applied the **Mann-Whitney U test** (non-parametric) to determine if differences between groups were statistically significant.
    * Tested on both **raw data** and **filtered data** (without anomalies).

## 💡 Key Findings
> *Insights derived from the analysis:*

* **Prioritization:** Hypothesis **#`[Insertar ID, ej: 8]`** won under the ICE framework, but Hypothesis **#`[Insertar ID, ej: 7]`** took the lead when using RICE because it reached a larger audience.
* **Conversion Rate:** Group B showed a relative gain of **`[Insertar %, ej: 13.8%]`** in conversion compared to Group A.
* **Average Order Size:** There was `[Insertar: "no significant difference" / "a significant increase"]` in the average order size between groups.
* **Statistical Result:** The p-value for conversion was **`[Insertar p-value, ej: < 0.05]`**, indicating the difference is statistically significant.

## 🚀 Conclusion & Decision
Based on the A/B test results:
* **Decision:** **`[Insertar decisión: Stop the test, Group B wins]`**.
* **Reasoning:** Although the average order size did not change significantly, the **conversion rate increased** clearly and stabilized in Group B, leading to higher overall revenue.

## 💻 How to Run
1.  Clone the repository:
    ```bash
    git clone [URL_DEL_TU_REPO]
    
