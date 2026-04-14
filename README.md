# 🧪 E-Commerce A/B Test: Optimizing Checkout for Revenue Growth
### *Statistical Validation & Financial Impact Analysis of UI/UX Interventions*

## 📌 Project Overview
This project evaluates the performance of a new checkout feature through a rigorous A/B testing framework. Moving beyond surface-level conversion metrics, I employed **Sequential Testing**, **Bootstrap Resampling**, and the **Delta Method** to validate financial lift and ensure the statistical stability of results before recommending a full-scale product rollout.

---

## 📈 Phase 1: Real-Time Monitoring & Convergence
To avoid the common pitfall of "peaking" at false positives, I utilized **Sequential Testing** to monitor the conversion rate as data accumulated. This ensured that the experiment reached a stable state before final conclusions were drawn.

![Sequential Test Convergence](visuals/Sequential%20Test:%20Conversion%20Rate%20Convergence%20Over%20Time.png)
*Figure 1: Real-time convergence of Conversion Rates across cumulative sessions.*

* [cite_start]**Stability Achieved:** Both Variant and Control groups showed clear convergence after 1,000 sessions, confirming that the observed lift was not a result of early-stage volatility[cite: 161, 177].

---

## 📊 Phase 2: Statistical Rigor & Lift Validation
I conducted a multi-stage validation using a **Z-Test** to measure immediate impact and **Bootstrap Distribution** to ensure the stability of the lift across 10,000 simulated runs.

![Z-Test Distribution](visuals/Z-Test:%20Control%20vs.%20Variant%20Distribution%20(Conversion%20Rates).png)
[cite_start]*Figure 2: Probability density showing a significant **+13.73% conversion lift** for the Variant group[cite: 223, 228].*

![Bootstrap Stability](visuals/Bootstrap%20Distribution:%20Stability%20of%20the%20Conversion%20Lift.png)
[cite_start]*Figure 3: Bootstrap results confirming a **99.58% probability** that the Variant outperforms the Control[cite: 185, 199].*

* [cite_start]**Statistical Confidence:** The Z-test reveals a distinct separation in means (37.79% vs 42.98%), while the Bootstrap mean lift of **5.22%** confirms high model stability[cite: 186, 224, 225].

---

## 💰 Phase 3: Financial Growth Analysis (The Delta Method)
Product success is ultimately measured by financial impact. I applied the **Delta Method** to calculate the lift in Average Order Value (AOV) and Revenue Per User (ARPU) while accounting for the variance inherent in ratio metrics.

![Delta Method Financial Growth](visuals/Delta%20Method:%20Financial%20Growth%20(AOV%20&%20ARPU).png)
*Figure 4: Financial impact analysis illustrating substantial growth in core revenue metrics.*

* [cite_start]**AOV Optimization:** The intervention drove a **+$9.75 AOV Lift**, increasing value from \$79.10 to \$88.85[cite: 145, 152, 153].
* [cite_start]**ARPU Lift:** Revenue per user increased by **+$4.75**, directly contributing to the platform's bottom-line growth[cite: 154, 156].

---

## 🔍 Final Validation: Chi-Square Observed vs. Expected
To conclude the analysis, a **Chi-Square test** was performed to compare observed buyer behavior against statistical expectations.

![Chi-Square Validation](visuals/Chi-Square%20Validation:%20Observed%20vs.%20Expected%20Buyers.png)
[cite_start]*Figure 5: Comparison confirming the Variant produced **32.4 extra buyers** beyond expectation[cite: 201, 211].*

---

## 💡 Strategic Conclusion
[cite_start]Based on the **99.58% probability of success** and the documented **+$9.75 lift in AOV**, the feature is cleared for a 100% traffic rollout[cite: 152, 199]. This analysis proves that the new checkout flow successfully reduces friction and incentivizes higher-value transactions.

---

## 🛠️ Technical Stack
* **Statistical Frameworks:** Z-Test, Chi-Square Validation, Bootstrap Resampling (10k iterations).
* **Advanced Analytics:** Delta Method for AOV/ARPU variance estimation, Sequential Testing.
* **Languages & Tools:** Python (Scipy, Statsmodels), Matplotlib, SQL (Metric Extraction).
