---
layout: post
title:  "Introduction to Statistical Learning Ch3. Linear Regression"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# Introduction to Statistcal Leearning with Applications in Python (2023) by Gareth James et al.
## Chapter 3. Lineear Regression

<br><br>
## 3.1. Simple Linear Regression
- Simple linear regression: A method for medeling the relationship between a scaler response and a single predictor variable.
- Objective: predict the response Y from the predictor X using a linear function.

### Model Representation
- $Y = \beta_0 + \beta_1X + e$
- where Y is the response variable,
- $\beta_0$ is the intercept,
- $\beta_1$ is the slope,
- e is the error term, assumed to be normally distributed with mean 0 and the constanct variance $\sigma^2$.

### Parameter Estimation
- Least Squares Method: used to estimate beta (weights, coefficients).
- ![Screenshot 2024-06-21 at 7 15 09 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/4f434586-58e3-4033-be32-391d0d20024a)

### Goodness of Fit
- Residual Standard Error(RSE), R-Squared
- ![Screenshot 2024-06-21 at 7 15 39 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/e0e4e000-5181-428b-bfd9-8652c1b91d43)

### Hypothesis Testing
- T-tests
- ![Screenshot 2024-06-21 at 7 19 18 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/d133ce26-eb24-413f-be27-68160ae1ce07)

### Assumptions of the Linear Regression Model
- Linearity: the relationship between X and Y is linear.
- Independence: observations are independent.
- Homoscedasticity: constant variance of the errors.
- Normality: errors are normally distributed.

<br><br>
## 3.2. Multiple Linear Regression
- Multiple Linear Regression: extends simple linear regression by modeling the relationship between a response variable and multiple predictor variables.
- Objective: predict the response Y from multiple predictors X1, X2, ..., Xp using a linear function.

### Model Representation
- ![Screenshot 2024-06-21 at 7 32 31 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/0b698ad9-3e46-45b4-8e42-1bea34f9753a)

### Matrix Formulation
- Unlike the simple linear regression estimates, the multiple regression coefficient estimates have more complicated forms.
- They usally are represented using matrix algebra.
- ![Screenshot 2024-06-21 at 7 33 19 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/a4986f75-b6c9-4168-824e-42be57d43665)

### Goodness of Fit
- Same as simple linear regression, it can be done with RSE and R-squared.
- ![Screenshot 2024-06-21 at 7 39 03 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/a53f42b3-68d3-478b-b673-da66d7ea206b)

### Hypothesis Testing
- F-statistics
- TSS is the error before the model, and RSS is the after the model.
- ![Screenshot 2024-06-21 at 7 54 40 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/abfe9876-1ca9-464e-8936-e5bce1d0b9c1)

### Variable Selection
- the first step in a multiple regression analysis is to compute the F-statistic of the model with all variables and to examine the associated p-value.
- If p-value shows that the model has any significance, then we need to know which subset of variables is associated with the response.
- Examining all possible combinations take $2^p$ when the model contains subsets of p variables, so it's not practical.
- Three classical approaches are,
  - Forward Selection: starts with no predictors and adds them one by one.
  - Backward Selection: starts with all predictors and removes them one by one.
  - Stepwise Selection: combination of forward and backward selection.
- Backward selection cannot be used if p > n, while forward selection can always be used.
- Forward selection is a greedy approach, and might include variables early that later become redundant.

### Multicollinearity
- Definition: when two or more predictors are highly correlated.
- Impact: can make estimates unstable and inflate standard errors.
- Detection: use Variance Inflation Factor(VIF).
- ![Screenshot 2024-06-21 at 7 57 19 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/72dcb316-05ec-41fb-88a0-95e0512edfc9)



