
# Loan Approval Model Interpretability

## Project Overview

This project focuses on interpreting a machine learning model used for loan approval prediction. A Random Forest classifier was built and tuned using GridSearchCV, and explainable AI techniques were applied to understand how the model makes decisions.

The emphasis of this project is not just predictive performance, but model transparency and feature-level insights.

---

## Problem Statement

Given applicant demographic and financial information, predict whether a loan application will be approved (`Loan_Status`).

More importantly, analyze which features influence the model’s decisions and how they affect predicted approval probability.

---

## Model Development

- Built a Random Forest classifier.
- Performed hyperparameter tuning using GridSearchCV (5-fold cross-validation).
- Optimized model performance using ROC-AUC due to class imbalance.
- Achieved cross-validated ROC-AUC ≈ 0.73.

---

## Interpretability Techniques

### 1. Permutation Importance
- Computed using 20 repeats.
- Identified the top 5 most influential features.
- Observed that dependency-related variables had the strongest impact.

### 2. Partial Dependence Plots (PDP)
- Generated PDP for the top 5 features.
- Used consistent Y-axis scaling for fair comparison.
- Analyzed how predicted probabilities change when feature values vary.

---

## Key Insights

- `Dependents_0` was the most influential feature in the model.
- Having one dependent slightly reduces predicted loan approval probability.
- Gender and marital status showed relatively small individual effects.
- Income-related variables such as `ApplicantIncome` and `LoanAmount` did not appear in the top 5, which is somewhat surprising.
- No single feature alone drastically shifts the model’s prediction; the model relies on combined feature effects.

---

## Technologies Used

- Python
- Scikit-learn
- RandomForestClassifier
- GridSearchCV
- Permutation Importance
- Partial Dependence Plots
- Pandas
- NumPy
- Matplotlib

---

## Author

Vikram Krishnareddy  
M.S. Data Science
