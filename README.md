# Credit-Risk-Analysis

This project aims to predict whether a loan will be paid back or default using a dataset containing various financial and demographic features. The dataset includes columns like income, debt-to-income ratio, credit score, loan amount, and other attributes to assist in building a classification model.


## Dataset

The dataset contains 593,994 entries and 13 columns, including the following key features:

- **annual_income**: The annual income of the applicant.
- **debt_to_income_ratio**: The ratio of the applicant's debt to income.
- **credit_score**: The applicant's credit score.
- **loan_amount**: The amount of the loan applied for.
- **interest_rate**: The interest rate of the loan.
- **loan_paid_back**: Whether the loan was paid back (1 for Yes, 0 for No).


## Steps in the Analysis
### 1. Exploratory Data Analysis (EDA):
- Load the dataset and check for missing values.
- Analyze distributions for features like **annual_income**, **credit_score**, and **loan_amount**.
- Visualize relationships using boxplots, histograms, and correlation heatmaps.
### 2. Feature Engineering:
- Create new features like **loan_to_income_ratio**, **interest_burden**, and **credit_segment**.
- Classify debt-to-income ratios into categories (**very_low**, **low**, **medium**, **high**, **very_high**).
- Extract numerical values from **grade_subgrade**.
### 3. Preprocessing:
- Handle missing values with imputation.
- Scale numeric features using RobustScaler.
- Encode categorical features using OneHotEncoder.
### 4. Modeling:
- Train a Logistic Regression and XGBoost model to predict loan default.
- Use metrics such as ROC-AUC, F1 score, precision at k%, and confusion matrix for evaluation.
### 5. Spark Implementation:
- The analysis also demonstrates how to scale the dataset and perform aggregation using PySpark for handling large datasets.


## Metrics and Results

The models' performance was evaluated using the following metrics:
- ROC-AUC: Measures the model's ability to distinguish between classes.
- F1 score: Harmonic mean of precision and recall, useful for imbalanced classes.
- Precision at k%: Precision at top k% of predicted probabilities.
- Confusion Matrix: Provides a breakdown of predicted vs. actual classes.


## Example Results:

### Logistic Regression:
- ROC-AUC: 0.9129
- F1 Score: 0.7429
- Precision@20%: 0.75
- Confusion Matrix:
[[True Positive, False Positive]
[False Negative, True Negative]]


### XGBoost:
- ROC-AUC: 0.9150
- F1 Score: 0.7450
- Precision@20%: 0.74
