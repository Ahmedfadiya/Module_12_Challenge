# Module_12_Challenge

## Overview of the Analysis

Credit risk classification is used to identify the risks associated with loans. I have used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

* The purpose of the analysis is to predict the loan status of different credit data.
* Loan size, interest rate, debt to income ratio, total debt and loan status were the information provided along with borrower income.
* The y variable was loan status and x variable was rest of the columns. I tried using logistic regression using original data and with random resampled data.
* Dataframe was created and then columns were separated into x and y variables. I then scaled the x variable, checked the balance of target values and the created a model, fit and trained and preditcted.
* Two methods were used `LogisticRegression` on scaled data and Random resampling method.

## Results

* Machine Learning Model 1: LogisticRegression
  * Logistics regression on original scaled data was used. Below is the classification report which clearly shows that the model is very biased to 1. Accuracy was at 99% but the imbalance of variables clearly makes this model not recommendable.
                precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.98      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384


* Machine Learning Model 2: RandomOverSampler
  * RandomOver Sampler on scaled data was used. Below is the classification report which shows that f1 score is very biased to 1. Accuracy is at 98%. Although the value counts shows balanced variables, the f1 score is very biased. Hence, this model is not recommended.
                   pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.98      1.00      0.99      0.98     18765
          1       0.84      0.98      0.99      0.91      0.99      0.98       619

avg / total       0.99      0.99      0.98      0.99      0.99      0.98     19384



## Summary

From both the machine learning models, I conclude that both are not fit for decision making process. I strongly feel that random sampling has a copied version of the same data to balance the variables - hence this is unfit.
My strong recommendation would be to try Smoteenn.

