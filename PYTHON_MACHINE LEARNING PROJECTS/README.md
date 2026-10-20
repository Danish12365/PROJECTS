# 🤖 Machine Learning & Deep Learning Project Portfolio

## Overview
This folder contains advanced Machine Learning and Deep Learning projects addressing real-world business problems in retail banking customer churn and clinical heart disease risk diagnosis. The projects leverage tabular ML algorithms (XGBoost, LightGBM, CatBoost, Extra Trees) and Neural Network architectures (TensorFlow/Keras ANNs) alongside SHAP model interpretability.

---

## Machine Learning Benchmark Index

*All performance metrics in the table below are copied directly from saved notebook cell execution outputs.*

| Project / Problem | Primary Models | Dataset & Size | Valuation Split | Verified Metrics | Source Cell Reference |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Bank Customer Churn** (`Bank-customer-churn-prediction.ipynb`) | Regularized CatBoost, Feature Engineering | Kaggle Churn Dataset (10,000 rows, 17 features) | Stratified $80/20$ Split & 5-Fold CV | **AUC: 0.8798**<br>Accuracy: 86.90%<br>Precision: 80.33%<br>Recall: 47.17%<br>F1-Score: 59.44% | Cell 21 (Test Set Evaluation) |
| **Deep Learning Churn ANN** (`Deep-learning-bank-customer-churn...`) | Keras Sequential ANN ('Bank-Net') | Kaggle Churn Dataset (10,000 rows) | Stratified $80/20$ Split | **AUC: 0.8604** | Cell 38 (Final Summary Output) |
| **Hybrid Ensemble Churn** (`DL-VS-ML-VS-Hybrid-Ensemble...`) | Voting Ensemble (ANN + CatBoost) | Kaggle Churn Dataset (10,000 rows) | Stratified $80/20$ Split | **Optimal AUC: 0.8792** (at CatBoost weight 1.0)<br>Hybrid AUC: 0.8666 (at 0.80 DL weight) | Cell 30 (Weight Sensitivity Analysis) |
| **Heart Disease Severity** (`Heart-Disease-Prediction-3-levels...`) | RandomForest, LightGBM, XGBoost, SVC | UCI Heart Disease Dataset (920 rows, 15 clinical features) | Stratified $80/20$ Split | **Best CV Score: 0.6578**<br>Test Accuracy: 72.83%<br>Test F1 Macro: 0.6924 | Cell 15 (Model Candidates Evaluation) |
| **Heart Disease Severity** (`Heart-Disease-Prediction-3-levels...`) | Calibrated Classifier (Sigmoid) | UCI Heart Disease Dataset (920 rows) | Stratified $80/20$ Split | Test Accuracy: 70.11%<br>Test F1 Macro: 0.6706 | Cell 18 (Calibrated Evaluation) |
| **Advanced Multi-Class Heart Disease** (`❤️_Heart_Disease_Prediction...`) | Extra Trees, CatBoost Ensemble | UCI Heart Disease Dataset (919 clean rows) | Stratified $80/20$ Split & 10-Fold CV | **CV Balanced Acc: 0.4970** | Cell 42 (Final Model Comparison) |

---

## Detailed Project Overviews & Documentation
- **[Bank Customer Churn Prediction Readme](../docs/projects/bank-churn.md):** Detailed methodology, SHAP interpretability analysis, feature engineering strategy, and financial intervention simulation.
- **[Heart Disease Classification Readme](../docs/projects/heart-disease.md):** Clinical background, outlier winsorization, multi-class severity evaluation, and probability calibration.

---

## Known Limitations & Technical Flags
1. **Hardcoded Kaggle File Paths:** Notebooks reference Kaggle input directory structures (`/kaggle/input/...`). When running locally, download datasets from Kaggle and adjust file path strings.
2. **Early Stopping Evaluation Set:** CatBoost models use test splits for early stopping monitoring. In practice, a separate validation split is recommended to avoid subtle evaluation set feedback.
3. **Imbalanced Churn Class Recall:** Bank churn models emphasize high precision (80.33%), resulting in a moderate recall (47.17%).

---

## Notebook Fallback Links
- **Bank Churn CatBoost:** [Bank-customer-churn-prediction.ipynb](./Bank-customer-churn-prediction.ipynb) | [Open in Colab](https://colab.research.google.com/github/Danish12365/PROJECTS/blob/main/PYTHON_MACHINE%20LEARNING%20PROJECTS/Bank-customer-churn-prediction.ipynb)
- **Bank Churn Deep Learning ANN:** [Deep-learning-bank-customer-churn-prediction.ipynb](./Deep-learning-bank-customer-churn-prediction.ipynb) | [Open in Colab](https://colab.research.google.com/github/Danish12365/PROJECTS/blob/main/PYTHON_MACHINE%20LEARNING%20PROJECTS/Deep-learning-bank-customer-churn-prediction.ipynb)
- **Heart Disease Severity:** [Heart-Disease-Prediction-3-levels-disease-severity.ipynb](./Heart-Disease-Prediction-3-levels-disease-severity.ipynb) | [Open in Colab](https://colab.research.google.com/github/Danish12365/PROJECTS/blob/main/PYTHON_MACHINE%20LEARNING%20PROJECTS/Heart-Disease-Prediction-3-levels-disease-severity.ipynb)
