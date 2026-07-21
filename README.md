# Credit Delinquency Prediction using Machine Learning

## Project Overview

This project focuses on predicting whether a banking customer is likely to become delinquent based on their financial profile, repayment history, and credit behavior.

The project covers the complete machine learning workflow including:

- Business understanding
- Data cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Preprocessing Pipeline
- Class Imbalance Handling using SMOTE
- Logistic Regression Model
- Model Evaluation
- Business Recommendations

---

## Business Problem

Financial institutions lose significant revenue due to customers failing to repay loans on time.

The objective of this project is to build a predictive model that identifies customers who are at risk of becoming delinquent, enabling banks to:

- Reduce financial losses
- Improve risk management
- Prioritize high-risk customers
- Take preventive actions before default occurs

---

## Dataset Features

The dataset contains customer demographic, financial, and repayment information such as:

- Age
- Income
- Employment Status
- Credit Score
- Credit Utilization
- Loan Balance
- Debt-to-Income Ratio
- Account Tenure
- Monthly Payment History
- Credit Card Type
- Location

### Target Variable

**Delinquent_Account**

- 0 → Non-Delinquent
- 1 → Delinquent

---

# Project Workflow

## 1. Data Cleaning

The following data quality issues were identified and resolved:

- Missing values in Income
- Missing values in Credit Score
- Missing values in Loan Balance
- Inconsistent Employment Status values
- Credit Utilization values above 100%
- Duplicate record check
- Data type verification

---

## 2. Missing Value Treatment

| Column | Method Used | Reason |
|----------|------------|--------|
| Income    | median | 7.8% missing values|
| Credit Score | Mean |5.8% missing values |
| Loan Balance | Median | Slightly skewed distribution |

---

## 3. Exploratory Data Analysis

EDA included:

- Missing value analysis
- Distribution plots
- Boxplots
- QQ Plots
- Correlation analysis
- Target class distribution
- Outlier detection
- Credit behavior analysis

### Key Findings

- Dataset is imbalanced.
- Approximately **84%** customers are non-delinquent.
- Approximately **16%** customers are delinquent.
- Credit Utilization above 100% indicates potential data anomalies.
- Some customers have zero account tenure.

---

## 4. Feature Engineering

The following preprocessing techniques were applied:

- Mean Imputation
- Median Imputation
- One-Hot Encoding
- Ordinal Encoding
- Standard Scaling
- ColumnTransformer
- Machine Learning Pipeline

---

## 5. Handling Class Imbalance

Since the dataset is highly imbalanced, **SMOTE (Synthetic Minority Oversampling Technique)** was applied to improve the model's ability to identify delinquent customers.

---

## 6. Machine Learning Model

Model Used:

- Logistic Regression

Pipeline Components:

- Data Preprocessing
- Feature Encoding
- Feature Scaling
- SMOTE
- Logistic Regression

---

# Model Performance

| Metric | Score |
|---------|--------|
| Accuracy | **58%** |
| ROC-AUC | **0.461** |

Classification Report:

| Class | Precision | Recall | F1 Score |
|--------|-----------|---------|----------|
| Non-Delinquent | 0.85 | 0.61 | 0.71 |
| Delinquent | 0.17 | 0.42 | 0.24 |

### Confusion Matrix

| | Predicted 0 | Predicted 1 |
|------|-----------|-----------|
| Actual 0 | 77 | 49 |
| Actual 1 | 14 | 10 |

---

# Important Predictive Features

Based on the analysis, the most influential variables include:

- Credit Utilization
- Credit Score
- Debt-to-Income Ratio
- Repayment History
- Loan Balance
- Income

---

# Business Insights

- Customers with high credit utilization are more likely to become delinquent.
- Lower credit scores are associated with higher repayment risk.
- Customers with higher debt-to-income ratios require closer monitoring.
- Historical repayment behavior strongly influences delinquency.
- Missing payments are an early warning indicator of future default.

---

# Recommendations

### High Risk Customers

- Increase monitoring frequency.
- Trigger early warning alerts.
- Offer repayment restructuring options.

### Medium Risk Customers

- Send payment reminders.
- Recommend financial planning assistance.
- Encourage partial repayments.

### Low Risk Customers

- Maintain regular monitoring.
- Offer loyalty rewards.
- Cross-sell banking products.

---

# Ethical Considerations

- Avoid discrimination based on demographic characteristics.
- Ensure transparency in credit decisions.
- Protect customer privacy.
- Regularly monitor the model for bias.
- Periodically retrain the model using updated data.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Jupyter Notebook

---


# Future Improvements

- Improve feature engineering.
- Tune model hyperparameters.
- Compare multiple machine learning algorithms.
- Use ensemble methods such as Random Forest or XGBoost.
- Improve minority class prediction through advanced sampling techniques.
- Deploy the model as a web application using Streamlit or Flask.

---

# Conclusion

This project demonstrates an end-to-end machine learning solution for predicting customer delinquency. Although the baseline Logistic Regression model shows limited predictive performance, the workflow establishes a strong foundation for future model improvements through advanced feature engineering, hyperparameter tuning, and more powerful classification algorithms.
