# E-commerce A/B Test: Checkout Feature Optimization

## 📌 Project Overview
This project evaluates the performance of a new checkout feature through a controlled A/B test. The goal was to determine if the new "Variant" experience significantly improves **Conversion Rates (CR%)** without negatively impacting **Average Order Value (AOV)** or user engagement time.

## 🛠 Tech Stack
* **Python:** Data cleaning, Feature Engineering, and Bayesian Statistical Modeling.
* **Power BI:** Interactive Data Visualization and Executive Reporting.
* **Statistics:** Beta Distribution analysis and Probability of Improvement calculations.

## 📊 Key Results
Based on the analysis of the experiment data:
* [cite_start]**Overall Conversion:** The Variant group achieved a **67.28%** conversion rate[cite: 20, 21].
* [cite_start]**Control Baseline:** The Control group maintained a conversion rate of **65.75%**[cite: 21].
* [cite_start]**Revenue Integrity:** Average Order Value remained stable at approximately **$29.35**, ensuring the lift in conversions translated to actual revenue growth[cite: 10].
* [cite_start]**Engagement:** User session length remained consistent across both groups at roughly **6 minutes**, suggesting no new friction was introduced by the feature[cite: 35, 71].

## 📈 Dashboard Highlights
[cite_start]The included Power BI report provides a multi-layered view of the test[cite: 1]:
* [cite_start]**Interactive Slicers:** Users can filter results by **Device Type** (Mobile, Desktop, Tablet) to see segment-specific performance[cite: 7].
* [cite_start]**KPI Overview:** High-level cards tracking Total Reach, CR%, and AOV[cite: 2, 5, 6].
* [cite_start]**Behavioral Trends:** Comparison of "Time on Site" to ensure the new feature didn't confuse users or increase checkout friction[cite: 15, 23].

## 📂 Repository Structure
* `/data`: Contains the `refined_ecommerce_data.csv` used for the analysis.
* `/notebooks`: Python scripts for data cleaning and Bayesian statistical testing.
* [cite_start]`/visuals`: Exported PDF and PNG versions of the Power BI dashboard[cite: 1, 38].

## 💡 Final Recommendation
The Variant group showed a clear, statistically significant improvement in conversion rates while maintaining stable order values. **Recommendation: Proceed with a 100% rollout of the new checkout feature.**
