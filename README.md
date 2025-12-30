# Fraud Detection for E-Commerce and Banking Transactions

## Project Overview

This project implements an end-to-end **fraud detection pipeline** for e-commerce and banking transactions. The goal is to build a robust machine learning model that can accurately identify fraudulent transactions, explain its predictions using **SHAP**, and translate those insights into **actionable business recommendations**.

The project follows a structured, production-oriented workflow covering:

* Data preparation and cleaning
* Exploratory data analysis (EDA)
* Feature engineering
* Model training and evaluation
* Model explainability using SHAP

---

## Project Structure

```
project-root/
├── data/
│   ├── raw/                    # Original datasets (not committed if large)
│   └── processed/              # Cleaned features and target files
│       ├── fraud_features.csv
│       └── fraud_target.csv
├── models/
│   ├── random_forest_fraud_model.joblib
│   └── feature_names.joblib
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_modeling.ipynb
│   └── 05_shap_explainability.ipynb
├── scripts/                    # (Optional) reusable Python scripts
├── README.md
└── requirements.txt
```

---

## Tasks Completed

### ✅ Task 1 — Data Preparation & Feature Engineering

* Cleaned raw transaction data
* Handled missing values and data types
* Engineered numerical and behavioral features
* Saved processed datasets to `data/processed/`

### ✅ Task 2 — Modeling

* Built a **baseline model**
* Trained an **ensemble RandomForestClassifier**
* Used cross-validation for model selection
* Final model configuration:

  ```python
  RandomForestClassifier(
      max_depth=10,
      n_jobs=-1,
      random_state=42
  )
  ```
* Saved trained model and feature names to `/models/`

### ✅ Task 3 — Model Explainability (SHAP)

Implemented full SHAP-based explainability **without retraining the model**:

#### Global Explainability

* Baseline feature importance (`model.feature_importances_`)
* SHAP summary plots (dot and bar)
* Identification of **Top-5 fraud drivers**
* Direction analysis (how features increase or decrease fraud risk)

#### Local Explainability

* Individual explanations for:

  * True Positive (TP)
  * False Positive (FP)
  * False Negative (FN)
* SHAP force / waterfall plots
* Plain-language explanations for each case

#### Business Recommendations

* SHAP-driven manual review rules
* Soft interventions for false positives
* Feature monitoring for drift detection
* Investigator-friendly explanations for decision support

---

## Key Technologies Used

* **Python**
* **Pandas / NumPy**
* **Scikit-learn**
* **SHAP**
* **Matplotlib**
* **Joblib**
* **Jupyter Notebook**

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repo-url>
cd project-root
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run notebooks in order

Open Jupyter Notebook or JupyterLab and execute:

1. `01_data_preparation.ipynb`
2. `02_exploratory_data_analysis.ipynb`
3. `03_feature_engineering.ipynb`
4. `04_modeling.ipynb`
5. `05_shap_explainability.ipynb`

> **Note:**
> The SHAP notebook loads the trained model from `/models/`.
> It does **not** retrain the model.

---

## Results Summary

* Ensemble Random Forest achieved strong fraud-detection performance
* SHAP revealed a small set of high-impact features driving predictions
* Local explanations highlighted why the model succeeds and fails
* Outputs are suitable for **both technical and business stakeholders**

---

## Repository Best Practices

* Clear folder separation (data, models, notebooks)
* No model retraining inside explainability notebook
* Saved artifacts for reproducibility
* Clean, modular notebook flow
* Ready for future extension into production pipelines

---

## Author

**Habtamu Wendifraw Eshibele**
Fraud Detection & Machine Learning Project
December 2025