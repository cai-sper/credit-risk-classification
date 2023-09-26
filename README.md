# Credit Risk Classification

## Overview
The purpose of this project is to build a machine learning model that can accurately predict the creditworthiness of borrowers. Using logistic regression, the model classifies loans into "Healthy" or "High-Risk" categories based on various features such as loan size, interest rate, borrower's income, and more. 

## Table of Contents
1. [Data Preprocessing](#data-preprocessing)
2. [Model Building](#model-building)
3. [Performance Metrics](#performance-metrics)
4. [Conclusion](#conclusion)

## Data Preprocessing
- Created a target set `y` from the `loan_status` column.
- Created a feature set `X` from the remaining columns.
- Data was split into training and testing datasets using `train_test_split`.

## Model Building
- Utilized logistic regression to fit the model on the training data (`X_train` and `y_train`).
- Made predictions on the testing data (`X_test`) using the fitted model.

## Performance Metrics
- **Balanced Accuracy Score**: 0.9520
- **Confusion Matrix**: 
    * True Positive: 563
    * True Negative: 18663
    * False Positive: 102
    * False Negative: 56
- **Classification Report**:
    * Healthy Loans Precision: 1.00
    * High-Risk Loans Precision: 0.85
    * Healthy Loans Recall: 0.99
    * High-Risk Loans Recall: 0.91
    * Weighted Average F1-Score: 0.99

### Analysis of Model Performance
The model shows a high balanced accuracy score of 0.9520, indicating that it is effective in classifying both healthy and high-risk loans. The precision, recall, and F1-score for "Healthy Loans" are near perfect, showcasing the model's reliability for this class. For "High-Risk Loans," the precision and recall are also commendable, revealing the model's aptitude in identifying risky lending cases. 

## Conclusion
The logistic regression model demonstrates excellent performance in predicting both healthy and high-risk loans. Given its high balanced accuracy and precision-recall scores, this model is highly recommended for evaluating the credit risk of borrowers.
