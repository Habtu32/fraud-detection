# Credit Risk Modeling Project

## Interim Project Report

---

## 1. Project Overview

This project focuses on building a **Credit Risk Prediction System** that estimates the likelihood of loan default using historical customer and loan data. The objective is to apply data science and machine learning techniques to support **risk-aware lending decisions** in financial institutions.

The project follows a structured machine learning lifecycle, including:

* Data understanding and preparation
* Exploratory data analysis (EDA)
* Feature engineering
* Predictive modeling
* Model evaluation and interpretation

This repository represents the **interim submission**, covering **Task 1: Data Preparation and Feature Engineering**, and preparing the foundation for **Task 2: Modeling**.

---

## 2. Project Objectives

* Understand and clean raw credit risk data
* Explore patterns and risk drivers through EDA
* Engineer meaningful features for modeling
* Prepare a modeling-ready dataset
* Establish a scalable and reproducible project structure

---

## 3. Project Structure

```
credit-risk-model/
├── data/
│   ├── raw/                # Original, unprocessed datasets
│   └── processed/          # Cleaned and feature-engineered data
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_eda.ipynb
│   └── 04_feature_engineering.ipynb
├── src/
│   ├── __init__.py
│   ├── data_processing.py  # Reusable data preparation functions
│   └── config.py           # Configuration variables
├── reports/
│   └── figures/            # EDA plots and charts
├── .gitignore
├── requirements.txt
└── README.md
```

---

## 4. Task 1 Summary: Data Preparation & Feature Engineering

### 4.1 Data Understanding (Task 1.1)

* Reviewed dataset structure, size, and variable definitions
* Identified target variable (loan default status)
* Classified features into numerical and categorical types
* Assessed data quality issues (missing values, inconsistencies)

**Outcome:** Clear understanding of the dataset and modeling target.

---

### 4.2 Data Cleaning (Task 1.2)

* Handled missing values using appropriate strategies:

  * Median imputation for numerical variables
  * Mode or “Unknown” category for categorical variables
* Removed duplicate records
* Standardized column names and formats
* Ensured correct data types for all features

**Outcome:** Clean and consistent dataset ready for analysis.

---

### 4.3 Exploratory Data Analysis – EDA (Task 1.3)

* Analyzed target variable distribution (default vs non-default)
* Studied relationships between features and credit risk
* Visualized:

  * Income vs default
  * Loan amount vs default
  * Employment length and credit behavior
* Identified class imbalance and potential risk drivers

**Outcome:** Key insights into factors influencing credit risk.

---

### 4.4 Feature Engineering (Task 1.4)

* Created new informative features, such as:

  * Debt-to-income ratio
  * Credit utilization indicators
  * Loan-to-income ratios
* Encoded categorical variables using suitable encoding techniques
* Scaled numerical features where required
* Saved the final modeling dataset to `/data/processed`

**Outcome:** Model-ready dataset with enhanced predictive power.

---

## 5. Tools and Technologies Used

* **Programming Language:** Python
* **Libraries:**

  * pandas, numpy – data manipulation
  * matplotlib, seaborn – visualization
  * scikit-learn – preprocessing and modeling (upcoming)
* **Environment:** Jupyter Notebook, VS Code
* **Version Control:** Git

---

## 6. Current Project Status (Interim Submission)

✅ Task 1 completed:

* Data Understanding
* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering

⏳ Task 2 pending:

* Model selection
* Model training
* Performance evaluation
* Model comparison

---

## 7. Next Steps: Task 2 – Modeling

In the next phase, the project will:

* Split data into training and testing sets
* Train baseline models (Logistic Regression)
* Experiment with advanced models (Decision Tree, Random Forest, etc.)
* Evaluate models using accuracy, precision, recall, F1-score, and ROC-AUC
* Select the best performing model for credit risk prediction

---

## 8. How to Run the Project

1. Clone the repository

   ```bash
   git clone <repository-url>
   ```
2. Create a virtual environment and install dependencies

   ```bash
   pip install -r requirements.txt
   ```
3. Run notebooks in order from the `notebooks/` directory

---

## 9. Author

**Habtamu Wendifraw Eshibele**
IT Support Officer | Aspiring Data Scientist
Credit Risk Modeling Project – Interim Submission