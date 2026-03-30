# 🛒 E-commerce A/B Test: Checkout Feature Optimization
> **Data-Driven Product Analysis** | Identified a **1.53% conversion lift** and an **$0.88 increase in Average Order Value (AOV)** using a multi-stack analytical approach.

---

## 📌 Project Overview
This project evaluates the performance of a newly designed checkout feature aimed at reducing friction and increasing purchase intent. By analyzing experimental data from **1,395 unique users**, I provided a data-backed recommendation on whether to roll out the feature globally or iterate on the design.

### **The Business Problem**
The product team suspected the legacy checkout flow was causing drop-offs, particularly on mobile devices. I was tasked with determining if the **Variant (New Feature)** outperformed the **Control (Original Flow)** across key financial and engagement metrics.

---

## 📊 Key Performance Metrics (Results)
| Metric | Control Group | Variant Group | Delta (Lift) |
| :--- | :--- | :--- | :--- |
| **Conversion Rate (Total)** | 65.75% | 67.28% | [cite_start]**+1.53%** [cite: 20, 21] |
| **Mobile CR% (Device 0)** | 66.52% | 67.28%* | [cite_start]**Segment Lead** [cite: 9, 20] |
| **Avg. Time on Site** | ~6.0 mins | ~6.1 mins | [cite_start]**+0.1 mins** [cite: 23, 35] |
| **Avg. Order Value** | $28.47 | $29.35 | [cite_start]**+$0.88** [cite: 10, 81] |

---

## 🛠️ Technical Workflow & Methodology

### 1. Data Infrastructure (SQL)
* **Relational Schema:** Architected a MySQL database with strict enforcement of data types (`DECIMAL` for currency, `INT` for flags) to ensure 100% data integrity.
* **Integrity Constraints:** Implemented **Primary Keys** on `user_id` to prevent data duplication and ensure reliable joins for future analysis.

### 2. Statistical Analysis (Python)
* **Exploratory Data Analysis (EDA):** Cleaned and transformed raw CSV data, handling outliers in `order_value_usd` and standardizing `ab_group` labels.
* **Bayesian Statistics:** Utilized **Beta Distributions** and **Posterior Sampling** (100,000 iterations) to calculate the "Probability of Being Better," providing a more robust conclusion than traditional P-values.
* **Libraries:** `Pandas`, `NumPy`, `SciPy.stats`, `Matplotlib`.

### 3. Business Intelligence (Power BI)
* [cite_start]**Interactive Dashboard:** Developed a comprehensive reporting suite featuring **KPI cards**, **Clustered Column Charts**, and **Segmented Bar Charts**[cite: 14, 15].
* [cite_start]**Dynamic Slicers:** Integrated a **Device Type Slicer** (Mobile, Desktop, Tablet) allowing stakeholders to drill down into platform-specific performance[cite: 7].
* [cite_start]**DAX Implementation:** Calculated custom measures for `CR%` and `AOV` to enable real-time filtering and accuracy[cite: 5, 6].

---

## 📖 Data Dictionary
| Column Name | Description | Type |
| :--- | :--- | :--- |
| `user_id` | Unique identifier for each participant | Integer (PK) |
| `ab_group` | Experimental group (Control vs. Variant) | String |
| `purchased` | Binary indicator of purchase (1 = Yes, 0 = No) | Boolean/Int |
| `order_value_usd` | Total transaction amount in USD | Decimal |
| `device_type` | Platform used (0: Mobile, 1: Desktop, 2: Tablet) | Integer |
| `time_on_site_min` | Total duration of the user session in minutes | Decimal |

---

## 💡 Strategic Recommendations
1. [cite_start]**Full Rollout:** Based on the **1.53% conversion lift** [cite: 20, 21] [cite_start]and the **increase in AOV**[cite: 10, 81], I recommend deploying the Variant feature to 100% of traffic.
2. [cite_start]**Device Focus:** The feature showed strong resilience on **Mobile (Device 0)**[cite: 9]; further UI/UX iterations should focus on the Tablet segment to close the minor engagement gap.
3. **Revenue Protection:** Monitoring confirms that the conversion gains were "high quality," as they were accompanied by a **revenue increase per user**, rather than a decrease from low-value impulse buys.

---
