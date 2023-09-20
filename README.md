# Credit Risk Classification

The purpose of this analysis was to create a supervised machine learning model that can predict whether an applicant will result in a healthy or high-risk loan. The data includes loan size, interest rate, borrower's income, debt-to-income ration, number of accounts, derogatory marks, total debt, and loan status (healthy or high risk).

I created a y set from the loan_status column and dropped it from the dataframe to create a features list "X" from the other remaining columns. Using value_counts, I determined how many of each loan type were included in the dataset. 75036 healthy loans and 2500 high-risk loans were included, which suggests this is not a balanced dataset.

I then split the data into training and testing groups. I fit the training data to a Logistic Regression model, then applied it to the test group and scored the model. I created a dataframe to compare predicted versus actual results for the test group. 

To analyze the performance, I applied a balanced accuracy score, created a confusion matrix, and printed a classification report. I chose a balanced accuracy because the dataset is imbalanced, as discovered during the value_counts function earlier in the analysis. 

These steps were then repeated on resampled data in order to determine if there would be a different result. Both models performed with identical results, suggesting that logistic regression model was already quite effective at handling the data distribution and did not require resampling in order to improve.