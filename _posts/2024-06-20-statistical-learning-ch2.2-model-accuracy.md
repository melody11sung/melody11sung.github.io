---
layout: post
title:  "Introduction to Statistical Learning Ch2.2 Assessing Model Accuracy"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# Introduction to Statistcal Leearning with Applications in Python (2023) by Gareth James et al.
## Chapter 2.2 Assessing Model Accuracy

<br><br>
## 1. Introduction
- Assising the accuracy of a statistical learning methods is crucial in both supervised and unsupervised learning.
- This section focuses on methods for measuring the quality of fit for supervised learning, the bias-variance trade-off, and evaluating classification methods.

<br><br>
## 2. Measuring the Quality of Fit

### Training and Testing
  - training data: used fo fit the model
  - test data: used to assess the model's performance.
<br>
### Key Metrics for Regression Models
  - Mean Squared Error (MSE): measures the average squared difference between observed and predicted values.
  - Lower MSE indicates a better fit.
  - ![Screenshot 2024-06-20 at 9 57 24 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/fbb7877f-3cb1-4c4c-acac-1ef1b39e13fe)
<br>
### R-Squared ($R^2$)
  - Proportion of the variance in the dependent variable that is predictable from the independent variables.
  - $R^2$ close to 1 indicates a better fit.
  - ![Screenshot 2024-06-20 at 11 23 50 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/6c3e8daf-80f0-4062-b5c6-20c7b6ed34ff)
<br>
### Validdation Set Approach
- procedure:
  1. split the data into a training set and validation set,
  2. fit the model on the training set,
  3. evaluate the model on the validation set.
<br>
### Leave-One-Out Cross-Validation (LOOCV)
- procedure:
  1. for each observation, fit the model on the remaining data,
  2. predict the left-out observations,
  3. calculate the overall error rate.
<br>  
### K-fold Cross-Validation
- procedure:
  1. split the data into k subsets (folds).
  2. for each fold, fit the model on the remaining k-1 folds and predict the fold left out.
  3. calculate the average error across all folds.
<br>
### Bootstrap Method
- procedure:
  1. randomly sample the data with replacement to create multiple datasets.
  2. fit the model on each dataset and evaluate performance.
  3. average the results to get an overall measure of model accuracy.

   
<br><br>
## 3. The Bias-Variance Trade-Off

### Bias-Variance Decomposition
- Bias: error due to the assumptions in the model.
- Variance: error due to the model's sensitivity to the fluctuations in the training set.
- irreducible error: error that cannot be reduced by any model.
<br>
### Total Error
- total error can be decomposed as,
- $Total Prediction Error = Bias^2 + Variance + Irreduccible Error
- bias-variance trade-off: increasing model complexity typically decreases bias, but increases variance, and vice versa.
- The relative rate of change of bias and variance determines whether test MSE increases or decreases.
- As we increase the flexibility of the model, the bias tends to initially decrease faster than the variance increases, resulting the expected test MSE decline at first. However, at some point increasing flexibility has little impact on the bias but starts to significantly increase the variance, making the test MSE increases.
<br> 
### Model Complexity
- Simple Models: high bias, low variance
- Complex Models: low bias, high variance

<br><br>
## 4. The Classification Setting

### Confusion Matrix: 
- composed of True Positives (TP), True Negatives (TN), False Positives (FP), False Negatives (FN).
<br>
### Metrics for Classification Models:
- Accuracy: proportion of correctly classified observations
  - $Accuracy = (TP + TN) \over (TP + TN + FP + FN)$
- Precision: proportion of positive identifications that were actually correct.
  - $Precision = TP \over (TP + FP)$
- Recall (Sensitivity): proportion of actual positives that were correctly identified.
  - $Recall = TP \over (TP + FN)$
- F1 Score: harmonic mean of precision and recall
  - $F1 = 2 * ((Precision * Recall) \over (Precision + Recall))$
<br>
### ROC Curve
- Reciever Operating Characteristic (ROC) Curve: plots the true positive rate (sensitivity) against the false positive rate (1-specificity).
- Area under the curve (AUC): measures the overall performance of the classification model.
<br>
### Validation Techniques
- same as those for regression models: validation set approach, cross-validation, and bootstrap.


<br><br>
## 5. Classifications

### Bayesian Classification
- assigns each observation to the most likely class, given its predictor values.
- bayes decision boundary: the boundary where the probability of classification changes from one class to another.
- bayes error rate: the lowest possible test error rate for a classifier, achieved by the Bayes classifier.
- ![Screenshot 2024-06-21 at 12 07 37 AM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/cd270a69-51de-473c-9017-dd6733f81ff3)
<br>
### K-Nearest Neighbors (KNN)
- assigns the class of the majority of the k-nearest neighbors.
- Distance metric: usually Euclidean distance is used to identify the nearest neighbors.
- Choice of K:
  - Small K: more flexible, can lead to high variance and overfitting.
  - Large K: less flexible, can lead to high bias and underfitting.
<br>
