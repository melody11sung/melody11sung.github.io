---
layout: post
title:  "ML Ch3. Decision Tree Learning"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# "Machine Learning" by Tom M. Mitchell (1997)
## Chapter 3. Decision Tree Learning

1. Introduction to Decision Trees
- Decision trees are a model for learning disjunctive expressions.
- They are particularly good at handling instances where attributes are categorical or where there are clear boundaries between the classes.

2. Representation
- A decision tree represents a function that takes as input a vector of attribute values and returns a "decision"—a single output value.
- Trees are organized as a series of questions which lead to a decision through a flowchart-like structure.

3. Algorithm for Learning Decision Trees
- The basic algorithm (ID3, C4.5, CART) involves choosing an attribute and partitioning the data into subsets based on the attribute values. This process repeats recursively for each derived subset in a greedy manner.
- The selection of attributes at each step is crucial and is typically done using a statistical measure. Common measures include:
  - Entropy: Measures the impurity in a group of examples.
    - <img width="247" alt="Screenshot 2024-07-26 at 1 19 55 PM" src="https://github.com/user-attachments/assets/af0fbcce-79d8-460c-b2bf-d9f30ed09c3c">

  - Information Gain: Based on the decrease in entropy after a dataset is split on an attribute. It aims to find the attribute that returns the highest gain.
    - <img width="286" alt="Screenshot 2024-07-26 at 1 20 13 PM" src="https://github.com/user-attachments/assets/0945141c-72c2-4dcb-8e17-41cf9a561bf3">
    - where p(t) is the proportion of the number of elements in class t to the number of elements in set S.
  - Gini Index: Used by the CART algorithm, it measures the impurity of an attribute in a dataset.

4. Recursion in Tree Construction
- The recursion proceeds by choosing an attribute, partitioning the dataset, and then recursively operating on each partitioned subset.
- The recursion can terminate under several conditions, such as when no attribute remains on which to further subdivide the data, or when all the instances in a partition are of the same class.

5. Handling Overfitting
- Decision trees are prone to overfitting, particularly when the trees are deep.
- Methods to avoid overfitting include:
  - Pruning: Simplifying the decision tree by removing parts of the tree that do not provide power to classify instances.
  - Setting a minimum size for splitting: Prevents the algorithm from defining leaves for small datasets, which might be noise.

6. Advantages and Disadvantages of Decision Trees
- Advantages: Easy to interpret and understand, can handle both numerical and categorical data, and robust to outliers.
- Disadvantages: Prone to overfitting, can be biased toward attributes with more levels, and may be unstable with small changes in data leading to a completely different tree being generated.

7. Applications of Decision Trees
- Used widely in operational settings, including customer relationship management, fault diagnosis, and classification tasks where human readability of the learned model is crucial.
