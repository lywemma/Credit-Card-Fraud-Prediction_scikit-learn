# Credit Card Fraud Prediction_scikit-learn

## Introduction
Fraud might happen in any business. It could lead to profit loss and damage brand reputation. There are various of supervised and unsupervised models for abnormal pattern detection. 

In this case, I used several supervised models to predict Credit Card Fraud. Because fraud usually accounts for a small proportion of the total number (less than 1%), the data is unbalanced. For highly skewed data, a Naive approach: identify all data as Not_Fraud (majority rule) could get high accuracy. However, it would be useless to classify Fraud. In order to build a better prediction model, we need to use Undersampling, Oversampling or SMOTE to get a balanced data. Since we have enough data in this case, I used Undersampling method.

## Data Description

Credit Card Fraud Data is from Kaggle. It has anonymized credit card transactions labeled as fraudulent or genuine. The csv file contains  284807 rows and 31 columns. The variables are transformed features from Principal Component Analysis (PCA). The original features are not provided.

Data Source: https://www.kaggle.com/mlg-ulb/creditcardfraud/data

## Approaches

1. Undersampling: convert data into balanced data.

2. Split data into training and test.

3. Establish cross validation to tune the best parameters for each model

4. Measures: calculate accuracy, confusion matrix, precision and recall for each model

5. Compare model performance based on measures and ROC curve and AUC

6. Classifier used in this case:

   a. K-Neighbors

   b. Decision Tree

   c. Support vector machine

   d. GradientBoosting

   e. Neural Network

***see "CreditCard_Fraud_Prediction_scikit-learn.ipynb"***

## Results

Neaural Network has the highest Accuracy score 0.95. For fraud detection, we would prefer greater recall number, because it indicates that the model could identify most of the fraud. Neaural Network has recall as 0.91, meaning 91% of the Fraud could be identified. According to ROC curve and AUC, Neaural Network also has better performance.