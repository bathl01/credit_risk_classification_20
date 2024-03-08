# Credit Risk Classification
### Module 20 Challenge
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending 
activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

NOTE: only one Model was run imbalanced learn was not covered in our course. 
# Credit Risk Analysis Report 
The purpose of this analysis is to create and evaluate the accuracy of a data model that predicts the credity worthiness of potential borrowers from peer-to-peer lending services

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

Factors considered in the analysis included data on:

the size of the loan
its interest rate
the borrower's income
the debt to income ratio
the number of accounts the borrower held
derogatory marks against the borrower
the total debt

The dataset (77,536 data points) was split into training and testing sets. The training set was used to build an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. Logistic Regression Model 1 was then applied to the testing dataset. 
The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk and results are summarized below.

This intial model was drawing from a dataset that had 75,036 low-risk loan data points and 2,500 high-risk data points. 
To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler module from imbalanced-learn. This generated 56,277 data points for both low-risk (0) and high-risk (1) loans, based on the original dataset.
## Results

### Logistic Regression Model 1:
* Balanced Accuracy Score: 95.20% --> this means that when taking into account the sensitivity (recall and/or true positive rate) and specificity (true negative rate) of the model, the balanced prediction accuracy was 95.2%
* Precision: 93% (an average--in predicting low-risk loans, the model was 100% precise, though the model was only 87% precise in predicting high-risk loans) This means 92% of predicted positives were correct
* Accuracy: 94%
* Recall: 95% (an average--the model had 100% recall in predicting low-risk loans, but 89% recall in predicting high-risk loans) this means that the model was 95% precise in measuring true positive values our of all positive predictions made
 
## Summary
I would recommend using this model to predict the creditworthiness of borrowers, because it has over 95% accuracy in predicting the outcome of the repayment of the initial loan. That accuracy range could be easily molded into a business risk profile to ensure sufficient capital 
flow for the lenders to remain in business/make a profit.
