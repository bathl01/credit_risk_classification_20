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
![image](https://github.com/bathl01/credit_risk_classification_20/assets/145512041/28975e8a-a8fb-4e1b-a116-fc3349a1a994)

  
### Logistic Regression Model 1:
* Precision: 100% precise in predicting healthy loans, 87% precise in predicting high-risk loans. This means for the healthy loans the classifications was corerect 100% of the time but for high-risk loans it was only correct 87% of the time.
* Accuracy: 99% indicates this model does a good job predicting both healty and high-risk loans.  However, there is a significant inbalance in the data with target values (75036 out of 77536) are for the healthy loans.
* Recall: 100% for the healthy loans and 89% for the high-risk loans. This means that the model where the loans were actually healthy 100% of the time they were correct but only 89% of the time when they were high-risk loans.
 
## Summary
I would recommend using this model to predict the creditworthiness of borrowers, because it has over 95% accuracy in predicting the outcome of the repayment of the initial loan. That accuracy range could be easily molded into a business risk profile to ensure sufficient capital 
flow for the lenders to remain in business/make a profit.
