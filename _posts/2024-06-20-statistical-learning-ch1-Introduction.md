---
layout: post
title:  "Introduction to Statistical Learning Ch1. Introduction"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# Introduction to Statistcal Leearning with Applications in Python (2023) by Gareth James et al.
## Chapter 1. Introduction


### Statistcal Learning
- Refers to a set of tools for understanding data, classified as supervised or unsupervised.
- Supervised Learning: involves predicting or estimating an output based on one or more inputs. Common in fields like business, medicine, astrophysics, and public policy.
- Unsupervised Learning: involoves learning relationships and structure from data without supervising output.


### Notation and Simple Matrix Algebra
- $n$: number of distinct data points or observations.
- $p$: number of variables avialable for predictions.
- $x_(ij)$: value of the j-th variable for the i-th observation.
- $X$: an n * p matrix where (i, j)-th element is $x_(ij)$
- $x_i$: a vector of length p containing the p variable measurements for the i-th observation.


### Statistical Learning Methods
- Regression Problem: predicting a continuous or quantitative output value.
- Classification Problem: predicting a categorical or qualitative output value.


### Example Applications
- Stock Market Data:
  - Objective: Predict whether the S&P index will increase or decrease using past 5 days’ percentage changes.
  - Observations:
    - No simple strategy to use past movements for future predictions.
    - Some weak trends suggesting possible prediction accuracy around 60%.

- Gene Expression Data:
  - Objective: Determine groups or clusters among cancer cell lines based on gene expression measurements.
  - Methods: Use principal components analysis to reduce dimensionality for visualization and clustering.

