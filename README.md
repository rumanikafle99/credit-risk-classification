# Credit Risk Analysis Report 

## Overview of the Analysis 

  In this analysis, I used logistic regression as well as logistic regression with oversampled/resampled data to train and evaluate a model for predicting whether a loan is healthy or at high risk. The source dataset used for the model includes financial information about borrowers, such as their loan status, which helps lenders make informed decisions about loan approvals. The loan_status column was used as the target variable for classification, where 0 represents a "Healthy Loan" and 1 represents a "High-Risk Loan." The goal of this analysis is to determine the creditworthiness of borrowers. 

The machine learning process was as follows ... 
  1. Clean and prepare the data by splitting away the target "loan_status" column to be used for classification. 
  2. Train the original dataset on a logistic regression model.
  3. Train the logistic regression model on resampled data to address class imbalance.
  4. Evaluate both models using their accuracy score, confusion matrix, and classification report.

## Results

Here are the results for both models:

Machine Learning Model 1 - Logistic Regression:
  - Accuracy Score: 96.80%
  - The confusion matrix results show that 110 healthy loans were misclassified as high-risk (false positives), while 36 high-risk loans were
    misclassified as healthy (false negatives).
  - The classification report shows 100% precision and 99% recall for healthy loans, while only 84% precision and 94% recall for high-risk loans.
    This reveals that while the model is trained quite accurately, especially with healthy loans, it still struggles to predict high-risk loans as
    some were misclassified as healthy.


Machine Learning Model 2 - Logistic Regression with Resampled Data:
  - Accuracy Score: 99.36%
  - The confusion matrix results show that 119 healthy loans were misclassified as high risk (false positives), while only 4 high-risk loans were
    misclassified as healthy. Compared to the model without oversampled data, this model led to fewer false negatives but higher false positives.
  - The classification report shows 100% precision and 99% recall for healthy loans, while high-risk loans stayed at 84% precision but saw an
    increase in recall to 99%. This reveals that while this model still predicts some false positives, it better detects high-risk loans.
  

## Summary

The first model used logistic regression on the original dataset and achieved an accuracy score of 96.80%. Based on its classification report, this model demonstrated perfect precision and near-perfect recall, which indicates that healthy loans were classified almost without fault. However, a lower precision for high-risk loans indicates misclassification of some high-risk loans as healthy. On the other hand, the second model used resampled data, which lowered bias, so the accuracy score increased to 99.36%. The resampled model maintained perfect precision for healthy loans while significantly improving the recall for high-risk loans, meaning it misclassified fewer actual high-risk loans as healthy. While the precision for high-risk loans remained at 0.84, like the previous model, the improved recall indicates that the resampled model is more effective in identifying borrowers with higher credit risk.

In this situation, where the goal is to determine the "creditworthiness of borrowers," the logistic regression using resampled data performs better, as it manages to identify high-risk loans more effectively. This is important to minimize risk and be reliable for financial risk assessment.

