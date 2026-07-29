# 🏥 Bridging Clinical Efficiency and Revenue Integrity
**Excel Analytics Project | Power Query · DAX · Data Modeling · Dashboard Design**

---

## 📌 Project Overview

Hospitals sit on two data streams that rarely talk to each other: clinical operations (how care is delivered) and financial performance (what that care costs). Leadership teams often see volume climbing and costs climbing right alongside it but without a merged view, it's hard to tell whether that's a capacity problem, a pricing problem, or just growth.

This project analyzes **six years of hospital data (2019–2024) totaling $1.4B in billing**, integrating **Length of Stay (LOS)** with **billing trends** to find where clinical operations and financial performance intersect.

> **The goal:** give leadership a single, drillable view that connects *how patients move through the hospital* to *what that movement costs* — and turn that into concrete resource and staffing decisions.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Excel & Power Query | ETL — standardizing dates, building calculated columns (Age Bins, Length of Stay) |
| DAX | Measures for YOY Growth, Standard Deviation of billing, and Time Intelligence |
| PowerPoint | Dashboard wireframing prior to build, for a clean executive-focused layout |
| Excel Dashboarding | Final interactive report (slicers, dynamic KPIs) |

---

## 📂 Repository Structure

```
clinical-revenue-integrity/
│
├── assets/
│   ├── financial-view.png
│   └── clinical-operations.png
│
├── data/
│   └── hospital_records_2019_2024.csv
│
├── workbook/
│   └── clinical_revenue_integrity.xlsx
│
└── README.md
```

---

## ⚙️ Project Pipeline

```
Phase 1 → Data Loading & Understanding (55,000 records, 2019–2024, Kaggle)
Phase 2 → Data Cleaning (Power Query)
Phase 3 → Structuring & Calculated Fields (Age Bins, LOS)
Phase 4 → DAX Modeling (YOY Growth, Std. Dev., Time Intelligence)
Phase 5 → Dashboard Wireframing (PowerPoint) & Build (Excel)
Phase 6 → Insights & Recommendations
```

---

## 1. Business Problem (The Why)

Leadership noticed patient volume and treatment costs rising in tandem and needed a data-driven answer to two questions:

- **Financials:** Which conditions drive the highest billing, and how do insurance providers compare?
- **Operations:** Are specific doctors or admission types (Emergency vs. Elective) creating bottlenecks in patient throughput?

**Cost-focused questions:**
1. Which medical conditions generate the highest average billing?
2. Does admission type affect billing amount?
3. Which insurance providers are linked to the highest/lowest billing?

**Efficiency-focused questions:**
1. Which conditions have the highest patient volume?
2. Do older patients stay longer?
3. Which doctors handle the longest-stay patients?

---

## 💰 Financial View

![Financial View Dashboard](assets/financial-view.png)

| Metric | Value |
|---|---|
| Total Billing | $1,417.43M |
| Average LOS | 15.5 days |
| Average Billing | $25.54K |
| Billing YOY | ▲ 22.98% |
| LOS YOY | ▲ 0.09% |

**Findings:**
- **Diabetes** is the highest-billing condition, ahead of Arthritis, Asthma, Cancer, Hypertension, and Obesity.
- **Admission type barely moves billing.** Elective (33.70%), Emergency (33.44%), and Urgent (32.86%) are split almost evenly — cost isn't concentrated in any one entry point.
- **Payer mix is tight.** Cigna carries the highest total billing, Aetna the lowest, with UnitedHealthcare, Medicare, and Blue Cross clustered in between — no single payer is disproportionately driving cost.
- Billing trend by month shows a cyclical, not runaway, pattern — spend rises and falls in waves rather than trending sharply upward within a year.

---

## 🏥 Clinical Operations

![Clinical Operations Dashboard](assets/clinical-operations.png)

| Metric | Value |
|---|---|
| Average LOS | 15.5 days |
| Patient Count | 55,500 |
| Patient Count YOY | ▲ 22.85% |

**Findings:**
- **Volume is scaling, LOS isn't.** Patient count grew 22.85% YOY while average LOS moved only 0.09% — throughput is keeping pace with demand rather than degrading under it.
- **Age drives length of stay.** Patients over 60 have a visibly longer average LOS than the 0–18, 19–35, and 36–60 groups, which sit close together.
- **Arthritis and Diabetes** account for the highest patient volume, consistent with them also being the top cost/billing drivers.
- **LOS varies meaningfully by doctor.** Some providers (e.g., Aaron Baker) show notably longer average stays than others handling similar case mix — a signal for care-pathway variance rather than case severity alone.
- Admission type distribution is again near-even (Elective ≈18.6K, Urgent ≈18.6K, Emergency ≈18.3K), confirming the split holds at the patient-count level, not just billing.

---

## 3. Key Insights

- **Volume vs. Revenue Growth:** A 22.85% YOY increase in patient count has directly driven a 22.98% increase in total billing (currently $1.4B) — revenue is growing in lockstep with volume, not outpacing it.
- **Stability in Care Delivery:** Despite the surge in volume, average LOS has held at 15.5 days (a negligible 0.09% increase), indicating clinical throughput is scaling effectively with demand.
- **Billing Drivers:** Diabetes remains the highest-billing condition, while Arthritis and Diabetes together account for the highest patient volume.
- **Payer Mix:** Billing is distributed almost evenly across major providers, with Cigna representing the highest billing total and Aetna the lowest.

---

## 4. Strategic Recommendations

1. **Optimize High-LOS Providers.** Address the variance in LOS by doctor — some providers show significantly longer stays than others. Standardizing care pathways for these outliers could free up bed capacity.
2. **Resource Allocation for Chronic Care.** Since Arthritis and Diabetes dominate both patient volume and billing, expand specialized outpatient programs to manage these conditions more efficiently and reduce reliance on long inpatient stays.
3. **Emergency vs. Elective Balance.** Admission types are nearly perfectly split (~33% each across Elective, Emergency, and Urgent). Investigate whether Emergency admissions drive higher per-case cost than Elective, to make sure staffing models account for that unpredictable influx.

---

## 🎯 What I Focused On

| Focus Area | Approach |
|---|---|
| Data structuring | Power Query ETL to standardize six years of raw records into a clean, modeled table |
| KPI design | DAX measures (YOY growth, std. deviation, time intelligence) built to answer specific leadership questions, not just report totals |
| Cross-functional narrative | One dataset, two lenses — Financial View and Clinical Operations — reconciled into a single set of recommendations |
| Storytelling | Every finding paired with a concrete, actionable recommendation |

---

## 📄 Deliverables

| Deliverable | Description |
|---|---|
| `workbook/clinical_revenue_integrity.xlsx` | Full Excel workbook — Power Query ETL, DAX measures, dashboards |
| `assets/financial-view.png` | Financial View dashboard |
| `assets/clinical-operations.png` | Clinical Operations dashboard |
| `README.md` | Full project documentation |

---

## 👤 Author

**Lawal Yusuf Gbolahan**
Data Analyst · Analytical Engineering

*Six years of hospital data, one merged view — connecting how patients move through the system to what that movement costs.*
