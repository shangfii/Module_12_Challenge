# Module_12_Challenge
Module 12 Challenge: Supervised learning methods an algorithms 


## Overview of the Analysis

The purpose of this analysis is to use various techniques to train and evaluate models with imbalanced classes using the case of loans. 
We used a dataset of historical lending activity from a peer-to-pear lending services company to build a model that can identify the creditworthiness of borrowers.

We have the features of the loans which are loan size,  interest rate, borrower income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt that we use to predict the out come of the loans which is wheather the borrow will pay back or defualt. The value of 0 is used to mean borrow was able to pay back (healthy loan) and the value of 1 to indicate that the borrow was not able to pay (high resk loan). Using this historical data we then create a model that can be used in the future to predict if a loan is healthy or unhealthy and check how good this method is using the classification report.

Using the value_counts function we are able to see the inherent imbalance that credit risk poses which is of the 77,536 loans in the data, 2500 (about 3.2%) of them were high-risk loans while 75036 were healthy loans. Which shows that even without using a method, one will be about 97% correct in getting healthty loans. This is an issue as a bad loan will cost the company to lose money and should be avoided

We used the model-fit-predict-evaluate machine learning process as part of the analysis. We split the data into training and testing datasets and used the Logistic Regression model to fit the Original Data which was used to train the model and then we made predictions with the model and tested with the test datasets. We then used the classification_report to see how well our model was performing and will possibly perform when given new data.

Because of the imbalance nature of the data, we further used the RandomOverSampler model to try and get a more balance data to use in our model. 



## Results


There is an accuracy score of 0.992 with the original data and and accuracy score of 0.994 with the balanced data. The balanced data shows more accuracy than the original data because of oversampling.

Both methods do a good job of getting the 0 target (with an accuracy of 1) but the oversampled method gets .84 for 1 target and the original data gets .85.

When we look at the recall the original data gives .91 in catching the 1 and the oversample data gives .99. So by oversampling we have improved on the recall.


* Machine Learning Model 1:

   Model 1: Healthy score Accuracy=0.992
   
   Precision: for the 0 is 1
              for the 1 is .85
   
   Recall scores: for the 0 is .99
                   for the 1 is .91



* Machine Learning Model 2:

  Accuracy = 0.9936781215845847
  
  Precision: for 0 is 1
             for 1 is .84
  
  Recall scores: for the 0 is .99
                  for the 1 is .99

## Summary

This models are 100% precise in detecting the healthy loans but our issue is to catch the risky loans as much as possible
This is an imbalance data problem that deals with loans, missing 1 loan out of any number of loans is not good for the business and we must try to get as accurate as possible. The accuracy is higher in the second model and this seems to show that if all we had was this two models we should go with model two which tries to address the imbalance and gets a higher accurancy and recall on the risky loans. It will be better to try other models before we canclude which models will be best for this as missing any loan will cost a lot of money



