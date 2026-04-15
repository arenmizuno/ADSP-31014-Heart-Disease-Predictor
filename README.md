# ADSP – Statistical Models for Data Science
## Final Project: Heart Disease Prediction

**University of Chicago**  
**Instructor:** Francisco Azeredo  
**Term:** Fall 2025

**Team Members:**  
- Jared Maksoud  
- Danny Mendoza  
- Aren Mizuno  
- Kirk Waller  

---

## Overview
This repository contains my final project for a Statistical Models course focused on linear and generalized linear models (GLMs), as well as extensions to survival and nonlinear modeling techniques.

The course explored how traditional linear models extend beyond Gaussian assumptions to handle a wider range of data types and distributions. Topics included generalized linear models, model selection, multicollinearity, and statistical inference, with an emphasis on applying these methods to real-world problems.

Students developed the full statistical analysis workflow: discovering insights, formulating hypotheses, validating evidence, and building data-driven solutions. The course emphasized both technical implementation in Python and effective communication of results.

---

## Final Project
**Description:**  
This project predicts the presence of heart disease using clinical and demographic data, with the goal of identifying high-risk patients and understanding the key factors driving cardiovascular risk.

The dataset (`heart.csv`) contains patient-level medical and health-related features and was cleaned and processed into a modeling-ready dataset of approximately 700 observations :contentReference[oaicite:0]{index=0}.

---

### Methodology

- Performed **data preprocessing and feature engineering**:
  - One-hot encoded categorical variables  
  - Removed anomalies (e.g., negative values in `Oldpeak`)  
  - Applied log transformations for skewed variables  
  - Used IQR-based outlier detection to filter extreme values  

- Built a **Logistic Regression model (GLM)**:
  - Binary target: HeartDisease (1 = disease, 0 = no disease)  
  - Used logit link function to model probability of disease  
  - Estimated parameters via Maximum Likelihood Estimation (MLE)  

- Conducted **feature selection and model refinement**:
  - Statistical significance testing (p-values)  
  - Regularization methods:
    - LASSO (L1)  
    - Ridge (L2)  
    - Elastic Net  
  - Multicollinearity analysis using Variance Inflation Factor (VIF)  
  - Likelihood Ratio Test to compare full vs reduced models  

- Evaluated model performance using:
  - Accuracy, Precision, Recall, F1 Score  
  - Confusion matrix  
  - ROC-AUC curves for out-of-sample performance  

---

### Key Findings

- Logistic regression produced a **strong and interpretable model** for predicting heart disease  

- The most important predictors were:
  - Sex  
  - Exercise-induced angina  
  - Chest pain type  
  - ST segment slope  

- The model achieved:
  - ~84% accuracy  
  - Balanced precision and recall (~0.83–0.85)  
  - Strong trade-off between identifying true cases and avoiding false positives  

- Sensitivity analysis showed:
  - Being male more than **doubles the odds** of heart disease  
  - Exercise-induced angina nearly doubles risk  
  - Certain chest pain types significantly reduce relative risk  
  - ST slope has a strong protective association  

- Simpler models performed comparably to full models, supporting **model interpretability and parsimony**  

---

### Project Deliverables

- `stats_final.ipynb`  
  → Full Python analysis including data preprocessing, modeling, and evaluation  

- `stats_final.html`  
  → Exported notebook for easy viewing  

- `heart.csv`  
  → Dataset used for modeling  

- `Statistical Models Final Presentation.pdf`  
  → Summary of methodology, results, and interpretation  

---

## Skills & Concepts Demonstrated

- Generalized Linear Models (Logistic Regression)  
- Maximum Likelihood Estimation (MLE)  
- Feature selection and statistical inference  
- Regularization: **LASSO, Ridge, Elastic Net**  
- Multicollinearity analysis (VIF)  
- Model comparison (Likelihood Ratio Test)  
- Classification metrics: Accuracy, Precision, Recall, F1  
- ROC-AUC evaluation and model diagnostics  
- Data preprocessing and feature engineering  
- Interpreting statistical models for real-world applications  

---
