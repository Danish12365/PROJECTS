# 🏦 Bank Customer Churn Prediction & Model Benchmarking

## Executive Summary
This project develops machine learning and deep learning models to predict customer churn for a retail bank with **10,000 customers**. Using engineered behavioral features, regularized CatBoost, Deep Learning (ANN), and Voting/Hybrid Ensembles, the best model achieves an **AUC of 0.8798** and an **Accuracy of 86.90%**.

---

## Business Problem
Customer acquisition costs in retail banking are 5x higher than retention. The bank needs to identify high-risk churn customers early to deploy targeted retention offers while minimizing intervention costs.

---

## Dataset Overview
- **Source:** Kaggle Bank Customer Churn Prediction Dataset (`Bank Customer Churn Prediction.csv`)
- **License Note:** Open Dataset / Public Domain
- **Scale:** 10,000 rows, 12 original features (expanded to 17 engineered features)
- **Class Distribution:** 7,963 Retained (79.6%), 2,037 Churned (20.4%) — Imbalanced

---

## Methodology
1. **Feature Engineering:** Created domain features including `churn_triangle`, `germany_inactive_risk`, `balance_salary_ratio`, and `product_overload`.
2. **Preprocessing:** Standard scaling and one-hot encoding fitted strictly on training split ($80/20$).
3. **Model Experiments:** Evaluated standalone Deep Learning ANN, regularized CatBoost, and Hybrid Ensembles.
4. **Explainability:** Applied SHAP (SHapley Additive exPlanations) to identify top churn drivers (`Age`, `NumOfProducts`, `IsActiveMember`, `Geography_Germany`).

---

## Verified Model Performance Metrics
*All metrics copied directly from saved notebook cell execution outputs.*

| Notebook / Model | Valuation Split | Accuracy | ROC-AUC | Precision | Recall | F1-Score | Source Cell |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `Bank-customer-churn-prediction.ipynb` (CatBoost) | 5-Fold CV | 86.31% ±0.64% | 0.8700 ±0.0102 | Not reported | Not reported | Not reported | Cell 18 |
| `Bank-customer-churn-prediction.ipynb` (CatBoost) | Test Set (2,000) | **86.90%** | **0.8798** | **80.33%** | **47.17%** | **59.44%** | Cell 21 |
| `Deep-learning-bank-customer-churn-prediction.ipynb` (ANN) | Test Set (2,000) | Not reported | 0.8604 | Not reported | Not reported | Not reported | Cell 38 |
| `DL-VS-ML-VS-Hybrid-Ensemble...` (Hybrid 80/20) | Test Set (2,000) | Not reported | 0.8666 | Not reported | Not reported | Not reported | Cell 30 |

---

## Financial Impact Simulation
*Extracted from `Bank-customer-churn-prediction.ipynb` Cell 30 output:*
- **Test Set Churners:** 407
- **Correctly Identified Churners (True Positives):** 192 (47.2% Recall)
- **False Alarms (False Positives):** 47
- **Illustrative Financial Calculation:** Net Benefit = **$168,100** (Simulated ROI = **875.5%** based on $1,000 customer value and $100 retention incentive assumptions).

> ⚠️ **Note:** Financial ROI calculations rely on hypothetical unit economics ($1,000 LTV, $100 intervention cost).

---

## Known Limitations & Data Leakage Risk
1. **Hardcoded Data Paths:** Notebooks reference Kaggle input paths (`/kaggle/input/bank-customer-churn-dataset/...`).
2. **Imbalanced Class Trade-off:** High precision (80.33%) comes at the cost of moderate recall (47.17%).
3. **Secret Scan Flag:** Notebook `Bank-customer-churn-prediction.ipynb` Cell 27 PNG output metadata contains an AWS-like pattern string (`AKIaqIW9vaQafKvnzKkU`). This is an auto-generated Matplotlib image hash string and not an active AWS credential.

---

## How to Reproduce
1. Download `Bank Customer Churn Prediction.csv` from Kaggle.
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn catboost tensorflow shap matplotlib seaborn
   ```
3. Run `Bank-customer-churn-prediction.ipynb`.

---

## Notebook Fallback Links
- **CatBoost ML Notebook:** [Bank-customer-churn-prediction.ipynb](../../PYTHON_MACHINE%20LEARNING%20PROJECTS/Bank-customer-churn-prediction.ipynb)
- **Deep Learning ANN Notebook:** [Deep-learning-bank-customer-churn-prediction.ipynb](../../PYTHON_MACHINE%20LEARNING%20PROJECTS/Deep-learning-bank-customer-churn-prediction.ipynb)
- **Hybrid Benchmark Notebook:** [DL-VS-ML-VS-Hybrid-Ensemble-Bank-Customer-Analysis.ipynb](../../PYTHON_MACHINE%20LEARNING%20PROJECTS/DL-VS-ML-VS-Hybrid-Ensemble-Bank-Customer-Analysis.ipynb)
- **Open in Google Colab:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Danish12365/PROJECTS/blob/main/PYTHON_MACHINE%20LEARNING%20PROJECTS/Bank-customer-churn-prediction.ipynb)
- **View on nbviewer:** [View on nbviewer](https://nbviewer.org/github/Danish12365/PROJECTS/blob/main/PYTHON_MACHINE%20LEARNING%20PROJECTS/Bank-customer-churn-prediction.ipynb)
