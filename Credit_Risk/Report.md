# Module 20 Report

## Overview of the Analysis

The purpose of this analysis was to create a supervised machine learning model that can predict whether an applicant will result in a healthy or high-risk loan. The data includes loan size, interest rate, borrower's income, debt-to-income ration, number of accounts, derogatory marks, total debt, and loan status (healthy or high risk).

I created a y set from the loan_status column and dropped it from the dataframe to create a features list "X" from the other remaining columns. Using value_counts, I determined how many of each loan type were included in the dataset. 75036 healthy loans and 2500 high-risk loans were included, which suggests this is not a balanced dataset.

I then split the data into training and testing groups. I fit the training data to a Logistic Regression model, then applied it to the test group and scored the model. I created a dataframe to compare predicted versus actual results for the test group. 

To analyze the performance, I applied a balanced accuracy score, created a confusion matrix, and printed a classification report. I chose a balanced accuracy because the dataset is imbalanced, as discovered during the value_counts function earlier in the analysis. 

These steps were then repeated on resampled data in order to determine if there would be a different result.


## Results

* Machine Learning Model 1:
  * Balanced accuracy: a score of 0.95 suggests that the model is successfully classifying both high-risk and healthy loans
  * Precision: a score of 0.85 means that out of all instances predicted as high-risk loans, 85% were actually high risk
  * Recall: a score of 0.91 indicates that the model correctly identified 91% of all actual high-risk loans

* Machine Learning Model 2:
  * Note: the results for this model were identical to Machine Learning Model 1
  * Balanced accuracy: a score of 0.95 suggests that the model is successfully classifying both high-risk and healthy loans
  * Precision: a score of 0.85 means that out of all instances predicted as high-risk loans," 85% were actually high risk
  * Recall: a score of 0.91 indicates that the model correctly identified 91% of all actual high-risk loans


## Summary

Both high risk and healthy loans are equally significant for lenders. If the model misses a healthy loan, it could be a lost opportunity for  business; if it misses a high-risk loan, this crucial information cannot be taken into account when making lending decisions. Since no part of the confusion matrix is more or less important than any other, accuracy and f1-score are the two best metrics for assessing the model. 

The logistic regression model predicts both healthy and high-risk loans extremely well. The accuracy is 99% which is an excellent score. The model scored an f1-score of 100% for healthy loans and 88% for high-risk loans. Although the model is better at identifying healthy loans, 88% is still a very good f1-score and the model can be used to accurately assess loan risk. It is important to note that more data was available in the healthy loan group, which may be why the model scored higher in that category.

The resampled model resulted in identical metrics for precision, recall, f1-score, and balanced accuracy score. This suggestes that the logistic regression model is already quite effective at handling the data distribution and did not require resampling in order to improve.
