# Credit-risk-classification
 

## Overview of the Analysis


The purpose of the analysis is to build a classification model for a peer to peer financial services company to predict the credit wothiness of the borrower to support a decision on extending the loan or not. The model was built and trained on the historical data which included information about Loan Size, Interest Rate, Borrower Income, Borrower GTotal Debt, Debt to Income etc.

The aim of the model was to predict, based on borrower profile and loan characteristics (on which the model was trained), whether the  borrower will default on the loan or not and  accordingly classify the target variable as  `1` or `0`.

Data preprocessing steps included dividing the data into feature variables and target variable and splitting the data into training and test data. Feature variables were  then scaled using standard scaler. Logistic Regression model  was trained on the scaled data and it was tested on the test data and its performance in terms of Accuracy, Precision and Recall  was evaluated using `sklearn` metrics - `Balanced Accuracy`, `Confusion Matrix` and `Classification Report`

Data set was highly imbalanced with only 3.22% of the instances belonging to `1` of target variable `loan_status`. Model was trained, evaluated and compared using both original data and resampled data. Data was resampled using `RandomOverSampler`  from the `imbalanced-learn` library to ensure equal instances of both the classes `1` and `0`


## Results

**<u>Machine Learning Model 1 (using original data)</u>**:

* Balanced Accuracy: 98.88%
* Recall: 98%
* Precision: 87%

**<u>Machine Learning Model 2 (using resampled data)</u>**:

* Balanced Accuracy: 99.47%
* Recall: 99%
* Precision: 99%


## Summary

Overall model 1 using original data performed reasonably well with its prediction on the test data. Performance of the model improved with resampled data as is evident from Precision and Recall scores. This is highly desirable and hence I would definitely recommend model 2. 

As a business manager, we would want to have high recall, as accurately predicting whether the borrower is going to default can have huge financial implications. Ultimately it will depend upon the business situation and objectives to arrive at a trade-off between Type 1 error (False Positives) which in this case will be missed bussiness revenue opportunity or Type 2 error (False Negative) meaning the financial implication of loan turning default.

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )


