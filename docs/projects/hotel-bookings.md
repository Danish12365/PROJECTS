# 🏨 Hotel Bookings Optimization & Demand Analysis

## Executive Summary
This project analyzes **119,390 hotel booking records** across Resort and City hotels to identify drivers of booking cancellations, customer lead-time behaviors, and revenue losses. Using statistical hypothesis testing (**Chi-Square Test of Independence** and **Mann-Whitney U Test**), the analysis reveals critical operational friction points and quantifies an **illustrative €12.7M revenue optimization opportunity**.

---

## Business Problem
High cancellation rates (overall **37.0%**) lead to operational inefficiencies, misallocated inventory, and revenue leakage. Hotel management requires data-driven answers to:
1. What factors predict cancellation risk?
2. How do lead times and deposit types influence guest behavior?
3. What is the financial impact of cancellations across different market segments?

---

## Dataset Overview
- **Source:** Kaggle Hotel Booking Demand Dataset (`hotel_bookings.csv`)
- **License Note:** Public Domain / Open Dataset (CC0: Public Domain)
- **Scale:** 119,390 rows, 32 features
- **Target Variable:** `is_canceled` (Binary: 0 = Retained, 1 = Canceled)

---

## Analytical Methodology
1. **Exploratory Data Analysis (EDA):** Univariate, bivariate, and multivariate distribution analysis across hotel types, lead times, deposit policies, and market segments.
2. **Statistical Hypothesis Testing:**
   - **Mann-Whitney U Test:** Compared lead times between canceled vs. non-canceled bookings ($p < 0.001$).
   - **Chi-Square Test of Independence:** Evaluated deposit type vs. cancellation outcome ($p < 0.001$).
3. **Financial Risk Modeling:** Calculated Average Daily Rate (ADR) lost per canceled room night across segments.

---

## Key Findings & Results

| Metric / Dimension | Observation | Statistical / Financial Finding |
| :--- | :--- | :--- |
| **Overall Cancellation Rate** | 37.0% across all bookings | 44,224 canceled bookings out of 119,390 |
| **City vs Resort Hotel** | City Hotel cancellation rate: 41.7% | Resort Hotel cancellation rate: 27.8% |
| **Lead Time Impact** | Canceled bookings had significantly higher lead time | Mann-Whitney U test statistic = $1.28 \times 10^9, p < 0.001$ |
| **Deposit Type Paradox** | "Non Refund" bookings showed ~99% cancellation rate | Chi-Square $\chi^2 = 27,677, p < 0.001$ (driven by tour operator group booking structures) |
| **Financial Impact** | Average Daily Rate (ADR) lost per canceled booking | **€12.7M illustrative total opportunity** (based on hypothetical recovery model assumptions) |

> ⚠️ **Note on Financial Impact:** The €12.7M optimization figure is based on illustrative scenario assumptions regarding cancellation recovery and overbooking adjustments.

---

## Visual Previews
- **Static Preview PDF:** [View Hotel Bookings Dashboard PDF](../../POWER%20BI%20PROJECTS/Hotel_bookings_DASHBOARD.pdf)
- **PNG Chart Artifacts:** Saved inside notebook outputs.

---

## Limitations & Known Issues
1. **Hardcoded Data Path:** The notebook contains local machine file paths (`D:\AI and Data Science 6\Projectes\hotel_bookings.csv` and `/kaggle/input/...`). To execute locally, download `hotel_bookings.csv` from Kaggle and place it in your local working folder.
2. **Hypothetical Financial Assumptions:** Revenue recovery projections assume fixed ADR recovery percentages.

---

## How to Reproduce
1. Download the dataset from [Kaggle Hotel Booking Demand](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand).
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy ipywidgets
   ```
3. Open and run the notebook using Jupyter Notebook or JupyterLab.

---

## Notebook Fallback Links
- **Primary Source Notebook:** [Comprehensive Interactive Hotel Bookings Analysis.ipynb](../../PYTHON_EDA_PROJECTS/Comprehensive%20Interactive%20Hotel%20Bookings%20Analysis.ipynb)
- **Advanced Statistical Notebook:** [Advanced Data Analysis of Hotel Bookings Demand.ipynb](../../PYTHON_EDA_PROJECTS/Advanced%20Data%20Analysis%20of%20Hotel%20Bookings%20Demand.ipynb)
- **Interactive Version via nbviewer:** [View on nbviewer](https://nbviewer.org/github/Danish12365/PROJECTS/blob/main/PYTHON_EDA_PROJECTS/Comprehensive%20Interactive%20Hotel%20Bookings%20Analysis.ipynb)
- **Open in Google Colab:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Danish12365/PROJECTS/blob/main/PYTHON_EDA_PROJECTS/Comprehensive%20Interactive%20Hotel%20Bookings%20Analysis.ipynb)
- **PDF Dashboard Export:** [Hotel_bookings_DASHBOARD.pdf](../../POWER%20BI%20PROJECTS/Hotel_bookings_DASHBOARD.pdf)
