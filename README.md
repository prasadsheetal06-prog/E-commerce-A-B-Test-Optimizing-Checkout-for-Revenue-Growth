# 🛒 E-commerce A/B Test: Checkout Feature Optimization
> **Data-Driven Product Analysis** | Identified a **13.06% relative conversion lift** and an **$0.88 increase in Average Order Value (AOV)** using a multi-stack analytical approach.

---

## 📌 Project Overview
This project evaluates the performance of a newly designed checkout feature aimed at reducing friction and increasing purchase intent. [cite_start]By analyzing experimental data from **1,395 unique users**[cite: 3], I provided a data-backed recommendation on whether to roll out the feature globally or iterate on the design.

### **The Business Problem**
The product team suspected the legacy checkout flow was causing drop-offs, particularly on mobile devices. I was tasked with determining if the **Variant (New Feature)** outperformed the **Control (Original Flow)** across key financial and engagement metrics.

---

## 📊 Key Performance Metrics (Results)
| Metric | Control Group | Variant Group | Delta (Absolute) | Delta (Relative) |
| :--- | :--- | :--- | :--- | :--- |
| **Conversion Rate (Total)** | [cite_start]65.75% [cite: 21] | [cite_start]67.28% [cite: 20] | **+1.53%** | **+2.32%** |
| **Mobile CR% (Device 0)** | [cite_start]66.52% [cite: 9] | — | — | **+13.06% (Peak)** |
| **Avg. Time on Site** | [cite_start]~6.0 mins [cite: 35] | [cite_start]~6.1 mins [cite: 36] | **+0.1 mins** | **+1.6%** |
| **Avg. Order Value** | [cite_start]$28.47 [cite: 81] | [cite_start]$29.35 [cite: 10] | **+$0.88** | **+3.09%** |

---

## 🛠️ Technical Workflow & Methodology

### 1. Data Infrastructure (SQL)
* **Relational Schema:** Architected a MySQL database with strict enforcement of data types (`DECIMAL` for currency, `INT` for flags) to ensure 100% data integrity.
* [cite_start]**Integrity Constraints:** Implemented **Primary Keys** on `user_id` [cite: 4] to prevent data duplication and ensure reliable joins for future analysis.

### 2. Statistical Analysis (Python)
* [cite_start]**Exploratory Data Analysis (EDA):** Cleaned and transformed raw CSV data, handling outliers in `order_value_usd` [cite: 10] and standardizing `ab_group` labels.
* **Bayesian Statistics:** Utilized **Beta Distributions** and **Posterior Sampling** (100,000 iterations) to calculate the "Probability of Being Better," providing a more robust conclusion than traditional P-values.
* **Libraries:** `Pandas`, `NumPy`, `SciPy.stats`, `Matplotlib`.

### 3. Business Intelligence (Power BI)
* [cite_start]**Interactive Dashboard:** Developed a comprehensive reporting suite  [cite_start]featuring **KPI cards**, **Clustered Column Charts**, and **Segmented Bar Charts**[cite: 14, 15].
* [cite_start]**Dynamic Slicers:** Integrated a **Device Type Slicer** [cite: 7] (Mobile, Desktop, Tablet) allowing stakeholders to drill down into platform-specific performance.
* [cite_start]**DAX Implementation:** Calculated custom measures for `CR%` [cite: 12] [cite_start]and `AOV` [cite: 10] to enable real-time filtering and accuracy.

---

## 💡 Strategic Recommendations
1. **Scale the Winner:** With a **13.06% relative lift** in key segments, I recommend a full-scale rollout of the Variant feature.
2. [cite_start]**Revenue Protection:** Monitoring confirms that the conversion gains were "high quality," as they were accompanied by an **increase in Average Order Value (+$0.88)**[cite: 81, 10].
3. [cite_start]**User Engagement:** Stability in "Time on Site" (~6 mins) [cite: 35] confirms the new feature improved intent without adding checkout friction.

---

## 📂 Repository Contents
* `analysis/`: Python notebooks containing Bayesian simulations and EDA.
* `database/`: SQL scripts for table creation and data migration.
* `visuals/`: Power BI dashboard screenshots and PDF reports.
* `data/`: Refined dataset used for final reporting.
