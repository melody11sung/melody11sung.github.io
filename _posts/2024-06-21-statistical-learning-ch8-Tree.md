---
layout: post
title:  "Introduction to Statistical Learning Ch8. Tree-Based Methods"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# Introduction to Statistcal Leearning with Applications in Python (2023) by Gareth James et al.
## Chapter 8. Tree-Based Methods

- Tree-Based Methods: used for both regression and classification by segmenting the predictor space into regions.
- Decision Trees: involve stratifying the predictor space into regions based on simple splitting rules, represented in a tree structure.

<br><br>
## 1. Regression Trees

### Steps:
- Splitting: segment the predictor space into regions based on conditions on the predictors.
- Prediction: for an observation in a region, the preiction is the mean of the response values for training observations in that region.

### Tree Structure:
- Internal Nodes: points where the data splits.
- Terminal Nodes (Leaves): endpoints that contain the predictions.

### Recursive Binary Splitting:
- Objective: minimize the Residual Sum of Squares (RSS).
- Algorithm:
  1. choose the best predictor and split point that minimize the RSS.
  2. Recursively apply the process to each region.
 
<br><br>
## 2. Classification Trees
- Task: predict a qualitative response.
- Prediction: Assign the most commonly occuring class in each region.

### Growing a classification Tree:
- similar to regression trees, but uses different criteria(e.g. Gini index, entropy) for making splits.

![Screenshot 2024-06-21 at 8 06 24 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/e8a927ba-6a71-41f0-af46-dd6d85a02591)

### Tree Pruning
- Purpose: avoid overfitting by simplifying the tree.
- Cost Complexity Pruning Algorithm:
  1. grow a large tree
  2. prune the tree back using a tuning parameter $\alpha$ to control complexity.
  3. use cross-validation to select the optimal $\alpha$

<br><br>
## 3. Bagging, Random Forest, Boosting

### Bagging (Bootstrap Aggregating)
- to reduce variance by averaging multiple trees trained on bootstrap samples.
- algorithm:
    1. create multiple bootstrap samples from the training data.
    2. train a tree on each sample
    3. average the predictions.

### Random Forest
- enhancement of bagging: adds an additional layer of randomness.
- algorithm:
    1. for each split in the tree, a random subset of predictors is considered.
    2. this decorrelates the trees, leading to improved prediction accuracy.

### Boosting
- to improve model accuracy by combining weak learners.
- algorithm:
    1. sequentially fit trees, each trying to correct the errors of the previous ones.
    2. update the weights of observations based on the errors.
    3. combine the trees for the final prediction.
