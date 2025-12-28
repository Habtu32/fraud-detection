# Fraud Detection System
## Project Overview

This project implements an end-to-end **Fraud Detection System** designed to identify **fraudulent transactions** from historical transactional data using machine learning techniques. The system follows a structured and modular data science workflow, ensuring clarity, reproducibility, and scalability.

The project covers data ingestion, preprocessing, feature engineering, model training, and evaluation. It is currently prepared for **model explainability** using **SHAP (SHapley Additive exPlanations)** to interpret model predictions and understand key fraud drivers.

---

## Objectives

* Detect fraudulent transactions accurately using machine learning
* Build a clean and reusable data processing pipeline
* Engineer meaningful features that improve fraud detection performance
* Train and evaluate classification models
* Prepare the system for explainable AI using SHAP

---

## Project Structure

```
fraud-detection/
├── .vscode/
│   └── settings.json
├── .github/
│   └── workflows/
│       └── unittests.yml
├── data/
│   ├── raw/                 # Original datasets (excluded from version control)
│   └── processed/           # Cleaned and feature-engineered data
├── notebooks/               # Exploratory analysis and experiments
├── src/
│   ├── data_processing.py   # Data cleaning and preprocessing
│   ├── feature_engineering.py
│   ├── model_training.py    # Model training and evaluation
│   └── app.py               # API entry point (FastAPI)
├── models/                  # Saved trained models
├── tests/                   # Unit tests
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Dataset Description

The dataset consists of historical transaction records containing both **legitimate** and **fraudulent** transactions. Each record includes transaction-level attributes such as amounts, timestamps, and other behavioral or engineered indicators.

* **Target variable**:

  * `is_fraud` (1 = Fraudulent, 0 = Legitimate)

* **Data location**:

  * Raw data: `data/raw/`
  * Processed data: `data/processed/`

---

## Task Progress

### Task 1: Data Preparation & Feature Engineering ✅

Completed steps:

* Data ingestion from raw files
* Handling missing values and inconsistent records
* Encoding categorical variables
* Scaling and normalizing numerical features
* Feature creation to capture transactional patterns
* Saving cleaned and processed datasets

Output:

* Clean, model-ready dataset stored in `data/processed/`

---

### Task 2: Modeling ✅

Completed steps:

* Train-test data splitting
* Training multiple classification models
* Model evaluation using appropriate metrics for fraud detection:

  * Precision
  * Recall
  * F1-score
  * ROC-AUC
* Selection of the best-performing model
* Saving trained model artifacts

Output:

* Trained models stored in the `models/` directory
* Performance metrics documented in notebooks and logs

---

### Task 3: Explainability (SHAP) 🔄 *(Next Step)*

Planned steps:

* Apply SHAP to the selected model
* Analyze global feature importance
* Explain individual fraud predictions
* Visualize SHAP summary, dependence, and force plots
* Improve transparency and trust in the fraud detection model

---

## Technologies Used

* **Programming Language**: Python
* **Libraries**:

  * pandas, numpy
  * scikit-learn
  * matplotlib, seaborn
  * SHAP (planned)
  * FastAPI (API deployment)
* **Version Control**: Git & GitHub

---

## How to Run the Project

1. Clone the repository:

   ```
   git clone https://github.com/Habtu32/fraud-detection
   cd fraud-detection
   ```

2. Create and activate a virtual environment:

   ```
   python -m venv .venv
   source .venv/bin/activate   # Linux/Mac
   .venv\Scripts\activate      # Windows
   ```

3. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

4. Run the API:

   ```
   uvicorn src.app:app --reload
   ```

---

## Future Improvements

* Advanced feature engineering using time-window aggregation
* Handling class imbalance with SMOTE or cost-sensitive learning
* Model explainability with SHAP
* Real-time fraud detection API deployment
* Monitoring model drift and performance

---

## Author

**Habtamu Wendifraw Eshibele**
Fraud Detection & Machine Learning Project