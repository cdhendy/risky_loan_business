# Credit Risk Report for Peer-to-Peer Loans

## Overview of the Analysis

- Credit risk poses a classification problem that is inherently imbalanced. The purposee of this analysis is to assist a peer-to-peer lending services company in building a model that can identify the creditworthiness of borrowers.

- Obviously a goal for these models should be to accurately predict high-risk loans, as selling a high-risk loan as a healthy one would be bad for business. Similarily, we wouldn't want to sell a healthy loan as high-risk, but unfortunately for the consumer, that wouldn't be bad for business.  

- The financial information used is a CSV file containing loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt, and loan status. 

- In our case `value_counts` was used to count the loan_status variable.

- First, a logistic regression model was used without resampling. Then, due to the highly inbalanced nature of the dataset, a logistic regression model was used with resampling. The process follows the standard process of: model, fit, predict, evaluate. 


## Results

*Due to the imbalanced nature of the data set provided (75,036 healthy to 2,500 high risk), the below results will only reflect high-risk loan values.*

**Machine Learning Model 1:**

  * Balanced Accuracy Score = 95.2%
  * Precision = 85%
  * Recall = 91%


**Machine Learning Model 2:**

  * Balanced Accuracy Score = 99.3%
  * Precision = 84%
  * Recall = 99%

## Summary

* Models need high recall when you need output-sensitive predictions. Recall evaluates the total number of *right* predictions made by the model - by considering the number of false-negatives to the number of true-positives we get a more accurate model with regards to the inbalance in the dataset.

* The linear regression model with resampling was inherently a better choice considering its higher recall rate - due to the inbalanced nature of the dataset it was imperative that the model accurately predict the much lower number of high-risk loans.

