# ❤️ Heart Disease Multi-Class Severity Classification

## Executive Summary
This project applies machine learning algorithms to diagnose heart disease and predict disease severity levels using clinical patient data from the **UCI Heart Disease Dataset** (920 patient records). By combining advanced preprocessing pipelines, hyperparameter tuning, and probability calibration, models are evaluated on both binary and multi-class classification tasks.

---

## Business & Clinical Context
Cardiovascular disease is a leading cause of global mortality. Early, non-invasive risk stratification allows cardiologists to prioritize diagnostic imaging and intervention for high-risk patients.

---

## Dataset Overview
- **Source:** UCI Machine Learning Repository / Kaggle (`heart_disease_uci.csv`)
- **License Note:** Open Dataset / Public Domain
- **Scale:** 920 patient records, 15 clinical attributes (Age, Sex, Chest Pain Type, Resting BP, Cholesterol, Fasting Blood Sugar, Resting ECG, Max Heart Rate, Exercise Angina, Oldpeak, Slope, CA, Thal)
- **Target Variable:** `num` (0 = No Disease, 1 = Mild, 2 = Moderate, 3 = Severe, 4 = Critical)

---

## Methodology
1. **Data Cleaning & Outlier Winsorization:** Extreme outliers capped at 1st/99th percentiles using custom transformers.
2. **Preprocessing Pipeline:** Column Transformer applying `OneHotEncoder` and `StandardScaler` strictly fitted on training splits ($80/20$).
3. **Model Candidates:** RandomForest, LightGBM, XGBoost, CatBoost, Extra Trees, Support Vector Classifier, Logistic Regression.
4. **Validation:** Stratified train-test split ($80/20$) with 10-Fold Cross-Validation and Calibrated Classifier probabilities.

---

## Verified Performance Metrics
*Extracted directly from notebook execution outputs.*

| Notebook | Task | Model | Validation Score | Test Accuracy | Test F1 Macro | Source Cell |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `Heart-Disease-Prediction-3-levels...` | Severity Classification | **RandomForest** | 0.6578 (Best CV Score) | **72.83%** | **0.6924** | Cell 15 |
| `Heart-Disease-Prediction-3-levels...` | Calibrated Model | **Calibrated Classifier (Sigmoid)** | N/A | **70.11%** | **0.6706** | Cell 18 |
| `❤️_Heart_Disease_Prediction...` | Multi-Class Severity | **Extra Trees** | 0.4970 (CV Balanced Acc) | Not reported | Not reported | Cell 42 |

> ⚠️ **Note on Multi-Class Complexity:** Multi-class disease severity prediction across 5 imbalance classes (0 through 4) exhibits lower macro F1 scores than binary classification due to class imbalance in severe disease categories.

---

## Known Limitations
1. **Dataset Path:** Hardcoded Kaggle path (`/kaggle/input/heart-disease-data/heart_disease_uci.csv`).
2. **Special Characters in Filename:** One notebook includes an emoji in its filename (`❤️_Heart_Disease_Prediction...`), which may cause path resolution issues on certain Linux environments.
3. **AWS Credential Scanner False Flag:** Matplotlib PNG metadata in output cells generated false positive scanner matches (`AKIA...`), which are image hash strings rather than AWS keys.

---

## How to Reproduce
1. Download `heart_disease_uci.csv` from Kaggle/UCI.
2. Install required packages:
   ```bash
   pip install pandas numpy scikit-learn xgboost lightgbm catboost matplotlib seaborn joblib
   ```
3. Execute `Heart-Disease-Prediction-3-levels-disease-severity.ipynb`.

---

## Notebook Fallback Links
- **Primary Severity Notebook:** [Heart-Disease-Prediction-3-levels-disease-severity.ipynb](../../PYTHON_MACHINE%20LEARNING%20PROJECTS/Heart-Disease-Prediction-3-levels-disease-severity.ipynb)
- **Advanced Multi-Class Classification Notebook:** [❤️_Heart_Disease_Prediction_Using_Advanced_Machine_Learning_with_Multi_Class_Classification.ipynb](../../PYTHON_MACHINE%20LEARNING%20PROJECTS/%E2%9D%A4%EF%B8%8F_Heart_Disease_Prediction_Using_Advanced_Machine_Learning_with_Multi_Class_Classification.ipynb)
- **Open in Google Colab:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Danish12365/PROJECTS/blob/main/PYTHON_MACHINE%20LEARNING%20PROJECTS/Heart-Disease-Prediction-3-levels-disease-severity.ipynb)
- **View on nbviewer:** [View on nbviewer](https://nbviewer.org/github/Danish12365/PROJECTS/blob/main/PYTHON_MACHINE%20LEARNING%20PROJECTS/Heart-Disease-Prediction-3-levels-disease-severity.ipynb)
