# **Credit Risk Analysis**

## **Overview**
The purpose of this project was to use machine learning to find a model that was able to detect applicants who are a risk (or not)when applying for a loan/credit card. 

The data used for this project is located in "LoanStats_2019Q1.csv".

Scikit Learn, Imbalanced Learn, and python libraries (numpy and pandas) were used to create this model. 


## **Results**
Scikit learn feature selection method SelectKBest was used to fine the top 25 features from our dataset. Only 16 of these features were used. 

The target value was the loan status (high_risk and low_risk).

Several techniques such as oversampling, undersampling, combination approach of both oversampling and undersamping, and bootstrap bagging & boosting were used to find the best model that could predict the potential risk of an applicant. 

### **Oversampling**
1. **RandomOverSampler**
    *  Balanced accuracy score: ~58%
    *  Classification report: ![img](https://github.com/tutran90/Credit_Risk_Analysis/blob/main/Random_OverSampling_CR.png)

2. **SMOTE Oversampling**
    * Balanced accuracy score: ~60%
    * Classification report: ![img](https://github.com/tutran90/Credit_Risk_Analysis/blob/main/SMOTE_Oversampling_CR.png)

### **Undersampling**
1. **ClusterCentroids**
    * Balanced accuracy score: ~53% 
    * Classification report: ![img](https://github.com/tutran90/Credit_Risk_Analysis/blob/main/UnderSample_CR.png)

### **Combination Sampling**
1. SMOTEENN
    * Balanced accuracy score: ~62%
    * Classification report: ![img](https://github.com/tutran90/Credit_Risk_Analysis/blob/main/SMOTEEN_CR.png)

### **Bagging and Boosting**
1. BalancedRandomForestClassifer
    * Balanced accuracy score: ~68%
    * Classification report: ![img](https://github.com/tutran90/Credit_Risk_Analysis/blob/main/BRFC_CR.png)

2. EasyEnsembleClassifer
    * There is a known bug with the EasyEnsembleClassifier package therefore results could not be collected using this method. 

## **Summary**
Overall all models were not able to predict high risk applicants due to the low number of high risk data within the data set. The precision in predicting high risk applicants were between 1-2%. The data used was based off of Quarter 1. If LendingClub or any financial institution had more time and budget, several quarter worth of data used to see the potential these models have in detecting high risk applicants. 

Out of all the methods that were used, bootstrap boosting BalancedRandomForestClassifier had the best results. The balance accuracry score was ~68%; the best score compared to the other models that were tested. This method had 100% precision in detecting low risk applicants. However, this model should not be used on future applicants. 

Again, there was not enough data used to accurately predict high risk individuals. If there was more time and resource, the features used could be increased to see if this produced better results. 
