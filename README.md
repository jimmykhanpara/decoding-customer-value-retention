<div align="center">

# 🛍️ Decoding Customer Value
### A SQL-Driven Retention Strategy for D2C Fashion

*Identifying who's genuinely loyal, who's just chasing discounts, and how to build sustainable revenue growth.*

![Python](https://img.shields.io/badge/Python-Pandas-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-Analysis-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

</div>

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Business Objective](#-business-objective)
- [Key Findings](#-key-findings)
- [Methodology](#-methodology)
- [Repository Structure](#-repository-structure)
- [Strategic Recommendations](#-strategic-recommendations)
- [Tech Stack](#️-tech-stack)
- [Team & Contributions](#-team--contributions)
- [License](#-license)

---

## 🔎 Overview

A **Direct-to-Consumer (D2C) fashion brand** has grown steadily to ~3,900 customers but has never built a structured way to understand them beyond surface-level sales numbers. This project builds that intelligence layer from scratch — using **Python** for feature engineering, **SQL** for segmentation analysis, and **Power BI** for an executive-facing dashboard — to answer one strategic question:

> **Is the business building genuine customer loyalty, or is growth being propped up by discounts?**

The raw dataset had **no loyalty score, no churn label, and no timestamps** — every concept used here (loyalty, value tier, promo dependency) was engineered from behavioral variables and validated, not assumed.

<table>
<tr>
<td width="50%" valign="top">

**📌 Project Snapshot**
| | |
|---|---|
| Domain | D2C Fashion / Retail |
| Dataset | ~3,900 customers |
| Stack | Python · SQL · Power BI |

</td>
<td width="50%" valign="top">

**📦 Deliverables**
- Feature-engineered dataset
- SQL segmentation analysis
- Interactive Power BI dashboard
- Retention playbook & executive summary

</td>
</tr>
</table>

---

## 🎯 Business Objective

Assess customer behavior patterns to determine which customers generate the greatest business value, identify segments at risk of churn, evaluate discount dependency, and recommend strategies for sustainable revenue growth.

---

## 🔑 Key Findings

<table>
<tr>
<td align="center" width="25%"><h3>716</h3>Potential Loyalists<br><sub>largest growth opportunity</sub></td>
<td align="center" width="25%"><h3>687</h3>Champion Customers<br><sub>highest-value segment</sub></td>
<td align="center" width="25%"><h3>657</h3>At-Risk Customers<br><sub>need proactive retention</sub></td>
<td align="center" width="25%"><h3>👟</h3>Footwear<br><sub>#1 loyalty category</sub></td>
</tr>
</table>

- 🏆 **Potential Loyalists** are the single largest segment (716 customers) — the strongest conversion opportunity in the base.
- 👟 **Footwear** posts the highest average loyalty and customer-value scores of any category.
- ⚠️ **539 Champion customers** are simultaneously *highly promo-dependent* — their retention may be propped up by discounts, not brand loyalty.
- 🔁 **519 customers** are labeled both "Loyal" *and* "At Risk" — proof that past loyalty doesn't guarantee future retention.
- 📈 **Loyalty score outweighs purchase frequency** as a driver of value — frequency stays flat (~5.8–6.0) across tiers while loyalty score nearly doubles from Very Low to High Value.
- 🗺️ **Organic-demand states** (Kansas, Maine, Connecticut) show low discount dependency — an untapped, high-margin acquisition opportunity vs. discount-driven states like Iowa and Indiana.

---

## 🧠 Methodology

### 1️⃣ Loyalty Framework

Two competing loyalty models were built and tested — only one was adopted, based on its direct relevance to the core business question.

| Model | Criteria | Verdict |
|---|---|---|
| **A — Behavioral Loyalty** | Above-median purchases · active subscription · weekly/fortnightly frequency · rating ≥ 4 | Measures engagement, not economic independence |
| **B — Economic Loyalty** ✅ | Above-average spend & purchase history · **no** discount applied · **no** promo code used | **Selected** — directly tests whether revenue depends on discounts |

### 2️⃣ Customer Segmentation

| Segment | Profile | Strategic Priority |
|---|---|---|
| 🥇 **Premium Loyalists** | High spend, high history, low promo usage | Protect & reward |
| 📈 **Growth Customers** | Moderate spend, occasional promo usage | Convert to Premium |
| 🏷️ **Promo Dependents** | Frequent discount usage, low history | Gradual promo sunset |
| ⚠️ **At-Risk Customers** | Low frequency, low ratings, no subscription | Win-back campaigns |

### 3️⃣ Analysis Pipeline

```
Raw Data → Python Feature Engineering → SQL Segmentation → Power BI Dashboard → Retention Playbook
```

| Stage | What Happened |
|---|---|
| **Python** | Cleaned raw data; engineered `dependency_score`, `value_tier`, `loyalty_score`, `customer_value_score` — each tied to a specific business question |
| **SQL** | 8 structured analyses: loyalty distribution, customer pyramid, loyalty vs. discount dependency, value drivers, category performance, geography, demographics, ideal customer profile |
| **Power BI** | Four-panel founder dashboard: customer pyramid, promo dependency vs. retention, geographic opportunity map, category funnel |
| **Playbook** | Phased promotional sunset roadmap + data-backed ideal customer profile |

---

## 📂 Repository Structure

```
decoding-customer-value/
│
├── 📄 README.md
│
├── 📁 data/
│   ├── Dataset.csv                          # Raw dataset
│   └── customer_intelligence_dataset.csv    # Feature-engineered dataset
│
├── 📁 notebooks/
│   └── Feature_Engineering.ipynb            # Python cleaning & feature engineering
│
├── 📁 sql/
│   └── SQL_Analysis.pdf                     # Segmentation queries + insights
│
├── 📁 dashboard/
│   └── Decoding_Customer_Value_Dashboard.pbix
│
├── 📁 docs/
│   ├── Executive_Summary.pdf
│   ├── Playbook.pdf
│   └── Problem_Statements.pdf
│
└── 📁 reports/
    └── dashboard_screenshots/               # PNG exports for quick viewing
```

---

## 🚀 Strategic Recommendations

1. **Convert Potential Loyalists → Champions** through targeted loyalty programs, not broad discounting.
2. **Sunset discounts in phases, not abruptly:**

   | Phase | Timeline | Target | Action |
   |---|---|---|---|
   | 1 — Discount Optimization | Month 1 | Promo Dependents | 20% → 15% |
   | 2 — Value Substitution | Month 2 | Growth Customers | 15% → 10% |
   | 3 — Loyalty Monetization | Month 3–4 | Premium Loyalists | 10% → 0–5% |

3. **Double down on Footwear & Accessories** — the strongest categories for loyalty and value.
4. **Launch win-back campaigns** for At-Risk customers before full disengagement.
5. **Redirect marketing spend to organic-demand states** rather than blanket promotions.

**Expected Impact:** 8–15% gross margin increase · 20% discount cost reduction · 25% lower promo dependency

---

## 🛠️ Tech Stack

<div align="left">

![Python](https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/-SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/-Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

## 👥 Team & Contributions

| Component | Contributor(s) |
|---|---|
| 🐍 Python & Feature Engineering | Vineet Chauhan, Jimmy Khanpara |
| 🗃️ SQL Analysis | Piyush Chothani |
| 📊 Power BI Dashboard | Jimmy Khanpara |
| 📘 Retention Playbook | Jimmy Khanpara, Piyush Chothani |
| 📝 Executive Summary | All |

<sub>Built as part of the **Consulting & Analytics Club, IIT Guwahati** — Summer Projects '26.</sub>

---

## 📄 License

Released under the [MIT License](LICENSE).

<div align="center">

**⭐ If you found this project useful, consider giving it a star!**

</div>
