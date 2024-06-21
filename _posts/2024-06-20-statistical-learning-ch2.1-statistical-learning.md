---
layout: post
title:  "Introduction to Statistical Learning Ch2.1 Statiscal Learning"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# Introduction to Statistcal Leearning with Applications in Python (2023) by Gareth James et al.
## Chapter 2.1 Statistical Learning


### Definitions
- Input Variables(predictors/ independent variables/ features): denoted as X1, X2, ..., X_p.
- Output Variables (response/ dependent variable): denoted as Y.
- Modeling Relationship: assumed to be Y = f(x) + e, where f represents the systematic information, and e represents the random error.


### Estimating f
- Objective 1. Prediction
  - predict the value of Y for a given value of X.
  - Accuracy: f(X) should approximate Y accurately for future predictions.
- Ovjective 2. Inference
  - understand the relationship between X and Y.
  - Understanding: assess the relationship and impact of each predictor on the response.
 
- Method 1. Parametric Methods
  - Assumption: assume a functional form for f(X).
  - Steps:
    1. Model Assumption: choose a form (e.g. linear, polynomial).
    2. fit the model: estimate parameters using training data.
    3. prediction: use the estimated model for predictions.
  - Trade-Off: simpler, interpretable, but may be inaccurate if the chosen form is incorrect.

- Method 2. Non-parametric Methods
  - Assumtion-Free: no specific functional form is assumed.
  - Flexibility: Capable of fitting a wider variety of shapes for f(X).
  - Trade-Off: flexible, potentially more accurate, but can be complex and harder to interpret.

 
### Prediction Accuracy vs. Model Interpretability
1. Model Flexibility
  - High Flexibility: can model complex relationships but may overfit (high variance).
  - Low Flexibility: simpler models with potential underfitting (high bias).

2. Bias-Variance Trade-Off
  - Variance: Error due to sensitivity to small fluctuations in the training set.
  - Bias: Error due to overly simplistic assumptions in the learning algorithm.


### Supervised vs. Unsupervised Learning
1. Supervised Learning
  - Regression Problems: predicting a continous response (e.g. predicting sales revenue).
  - Classification Problems: predicting a categorical response (e.g. classifying emails as spam or not).
 
2. Unsupervised Learning
  - Clustering: grouping observations into distinct clusters.
  - Dimension Reduction: simplifying data by reducing the number of variables.

