# Credit Risk Classification
### Module 20 Challenge
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending 
activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

NOTE: only one Model was run imbalanced learn was not covered in our course. 
# Credit Risk Analysis Report 
The purpose of this analysis is to create and evaluate the accuracy of a data model that predicts the credity worthiness of potential borrowers from peer-to-peer lending services

Factors considered in the analysis included data on:
loan_size	
interest_rate	
borrower_income	
debt_to_income	
num_of_accounts	
derogatory_marks	
total_debt
loan_status

The dataset (77535 data points) was split into training and testing sets. The training set was used to build an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. Logistic Regression Model 1 was then applied to the testing dataset. 
The purpose of the model was to determine whether a loan to the borrower in the testing set would be healthy or high-risk and results are summarized below.
	        
![image](https://github.com/bathl01/credit_risk_classification_20/assets/145512041/08a81654-57cc-4795-95a9-173281966c7b)


This intial model was drawing from a dataset that had 18,759 healthy loan data points and 625 high-risk data points. 

## Results
Classification Report
                precision    recall  f1-score   support

  healthy loan       1.00      1.00      1.00     18759
high-risk loan       0.87      0.89      0.88       625

      accuracy                           0.99     19384
     macro avg       0.94      0.94      0.94     19384
  weighted avg       0.99      0.99      0.99     19384
  
### Logistic Regression Model 1:
* Precision: 94% (an average--in predicting healthy loans, the model was 100% precise, though the model was only 87% precise in predicting high-risk loans) This means 92% of predicted positives were correct
* Accuracy: 99% indicates this model does a good job predicting both healty and high-risk loans.  However, there is a significant inbalance in the data with target values (75036 out of 77536) are for the healthy loans.
* Recall: 97% (an average--the model had 100% recall in predicting healthy loans, but 95% recall in predicting high-risk loans) this means that the model was 94% precise in measuring true positive values our of all positive predictions made
 
## Summary
I would recommend using this model to predict the creditworthiness of borrowers, because it has over 95% accuracy in predicting the outcome of the repayment of the initial loan. That accuracy range could be easily molded into a business risk profile to ensure sufficient capital 
flow for the lenders to remain in business/make a profit.
