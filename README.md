# Credit Card Default Prediction

## Project Overview
This project predicts whether a credit card customer is likely to default on their payment in the next month.

The objective is to build a practical credit risk classification model and compare multiple machine learning approaches focusing not only on accuracy but also on AUC and defaulter recall which are critical in real world financial risk assessment.

The project follows an end-to-end ML workflow from data cleaning and EDA to model comparison and interpretation.

---

## Dataset Description

**Dataset Source:**  
The dataset contains customer level financial and demographic information including:
- Demographic details (age, gender, education, marital status)
- Credit limit (LIMIT_BAL)
- Monthly billing amounts (BILL_AMT1–6)
- Historical repayment status (PAY_0–PAY_6)
- Payment amounts (PAY_AMT1–6)

Target Variable:
Indicates whether the customer defaulted in the next month (1 = Default, 0 = No Default).

Source: UCI Machine Learning Repository – Credit Card Default Dataset

---

## Methodology

### 1. Data Cleaning and Preparation
- Removed non-informative columns (e.g., ID)
- Checked for missing values
- Verified data consistency
- Applied feature scaling for Logistic Regression
- Used stratified train-test split to maintain class balance

### 2. Exploratory Data Analysis (EDA)
- Identified class imbalance between defaulters and non-defaulters
- Analyzed repayment delay patterns
- Observed that recent payment delays (especially PAY_0, PAY_2) strongly relate to default risk

### 3. Model Building
Two classification models were implemented:

 **Logistic Regression**
- Used as an interpretable baseline model
- Applied feature scaling
- Evaluated using Accuracy, ROC–AUC, Recall, Confusion Matrix

 **Decision Tree Classifier**
- Captures non-linear relationships
- Limited tree depth to reduce overfitting
- Evaluated using Accuracy, ROC–AUC, Recall, Confusion Matrix
- Extracted feature importance


### 4. Model Evaluation Metrics
Models were evaluated using:
- Accuracy
- ROC-AUC Score
- Defaulter Recall
- Confusion Matrix
  
Since the dataset is imbalanced, ROC-AUC and Recall for defaulters were prioritized over accuracy.

## Model Comparison Summary

| Model               | Accuracy | AUC   | Defaulter Recall |
|---------------------|----------|-------|------------------|
| Logistic Regression | 0.808    | 0.715 | 0.236            |
| Decision Tree       | 0.816    | 0.743 | 0.341            |

**Interpretation:**  
The Decision Tree slightly outperforms Logistic Regression in terms of AUC and recall while both models achieve similar accuracy, the Decision Tree identifies a higher proportion of defaulters making it more suitable for credit risk applications where minimizing missed defaults is critical.

---

## Key Insights
- Both models achieve similar accuracy (~81%).
- Decision Tree performs better in terms of AUC and recall for defaulters.
- Logistic Regression remains a strong and interpretable baseline.
- Repayment delay variables (PAY_0, PAY_2) are the most important predictors of default.
- For credit risk use cases, identifying defaulters (recall) is more important than maximizing overall accuracy.

---
## Business Interpretation
In credit risk modeling failing to identify a defaulter is more costly than incorrectly flagging a safe customer.
The Decision Tree improves defaulter detection while maintaining comparable accuracy making it more suitable for risk-sensitive financial applications.

---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Conclusion
This project demonstrates how model selection depends on business objectives while Logistic Regression provides transparency and interpretability, the Decision Tree improves detection of risky customers through better recall and AUC performance.

The final model selection depends on whether the priority is interpretability or risk minimization.

---

## Author
 * Name: Anushka Singh
 * Institution: Gokhale Institute of Politics and Economics
 * Github: https://github.com/09AnushkaSingh
 * Linkedin: https://www.linkedin.com/in/anushka09singh/
 * Date: January 2026
