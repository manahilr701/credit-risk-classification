# Module 20 Report

## Overview of the Analysis

The purpose of this analysis was to evaluate the creditworthiness of borrowers by building a machine learning model that can classify loans as either healthy (`0`) or high-risk (`1`). This analysis aims to assist the lending company in making informed decisions about loan approvals, thereby reducing financial risks associated with loan defaults.

The dataset contains various financial attributes of borrowers, including:
- **Loan size**: The loan amount requested.
- **Interest rate**: The annual percentage rate of the loan.
- **Borrower income**: The borrower’s annual income.
- **Debt-to-income ratio**: The ratio of total debt to annual income.
- **Number of accounts**: The borrower’s total number of financial accounts.
- **Derogatory marks**: Negative marks in the borrower’s credit history.
- **Total debt**: The total outstanding debt for the borrower.

The target variable, `loan_status`, indicates whether a loan is healthy (`0`) or high-risk (`1`). Analyzing the value counts of the target variable showed an imbalance in the dataset, with healthy loans being the majority and high-risk loans being the minority. This imbalance was considered throughout the analysis to ensure accurate model evaluation.

### Stages of the Machine Learning Process
The machine learning process included the following stages:
1. **Data Preprocessing**:
   - The dataset was loaded into a Pandas DataFrame.
   - Features (`X`) and target labels (`y`) were separated.
   - The data was split into training and testing sets, with 75% allocated for training and 25% for testing using `train_test_split`.

2. **Model Training**:
   - A Logistic Regression model was selected and trained on the training dataset (`X_train` and `y_train`).
   - Logistic Regression is a binary classification algorithm that predicts probabilities and makes classifications based on a decision threshold (default: 0.5).

3. **Model Evaluation**:
   - Predictions were made on the test dataset (`X_test`).
   - A confusion matrix and classification report were generated to evaluate the model’s performance using accuracy, precision, recall, and F1-score.

### Methods Used
The analysis used **Logistic Regression** due to its simplicity and effectiveness in binary classification problems. Logistic Regression provides interpretable results and works well with structured datasets, making it suitable for predicting loan status. While this was the primary algorithm, alternative models like Random Forest or Gradient Boosting could be explored in the future for comparison.

## Results

- **Accuracy**: 99%
- **Precision**:
  - Healthy Loans (0): 100%
  - High-Risk Loans (1): 85%
- **Recall**:
  - Healthy Loans (0): 100%
  - High-Risk Loans (1): 91%
- **F1-Score**:
  - Healthy Loans (0): 100%
  - High-Risk Loans (1): 88%

## Summary

The logistic regression model demonstrates excellent performance, achieving a high accuracy of 99%. It performs exceptionally well in identifying healthy loans, with perfect precision and recall. For high-risk loans, the model achieves strong recall (91%), indicating it successfully identifies most high-risk loans, though precision (85%) shows that some loans are incorrectly classified as high-risk.

### Recommendation
This model is recommended for use by the company due to its strong predictive capabilities. However, efforts to further improve precision for high-risk loans could enhance the model's overall reliability. This might include incorporating additional features or testing alternative algorithms like Random Forest or Gradient Boosting.
