# Credit Card Default Prediction

## Project Overview
This project aims to predict whether a credit card customer is likely to default on their payment in the following month. The goal is to build a practical credit risk model that balances interpretability and predictive performance, similar to real-world financial risk assessment use cases.

The project follows an end-to-end machine learning workflow, starting from data understanding and preprocessing to model comparison and interpretation.

---

## Dataset Description
The dataset includes customer-level information such as:
- Demographic details (age, gender, education, marital status)
- Credit limit
- Monthly billing amounts
- Historical repayment status and payment behavior

The target variable indicates whether the customer defaulted on payment in the next month.

---

## Methodology

### 1. Data Cleaning and Preparation
- Removed non-informative columns such as customer ID
- Verified absence of missing values
- Ensured data consistency before modeling

### 2. Exploratory Data Analysis (EDA)
- Studied class imbalance between defaulters and non-defaulters
- Analyzed repayment behavior patterns linked to default risk
- Observed that recent payment delays are strongly associated with defaults

### 3. Feature Selection and Train-Test Split
- Selected all relevant financial and demographic features
- Used stratified train-test split to preserve class distribution
- Applied feature scaling where required

### 4. Model Building
- **Logistic Regression** used as an interpretable baseline model
- **Decision Tree Classifier** applied to capture non-linear relationships

### 5. Model Evaluation
- Evaluated models using accuracy, precision, recall and F1-score
- Gave special importance to recall for defaulters due to business relevance

---

## Key Insights
- Logistic Regression provides a strong and interpretable baseline.
- Decision Tree improves recall for defaulters, making it more suitable for identifying high-risk customers.
- Repayment delay variables emerge as the most important predictors of default risk.

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## Conclusion
This project demonstrates how different machine learning models can be applied to a real-world credit risk problem. While simpler models offer transparency, tree-based models add value by better capturing risky customer behavior, which is critical in financial decision-making.
