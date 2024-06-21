---
layout: post
title:  "Deep Learning Ch2. Probabilities"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# Deep Learning: Foundations and Concepts (2023) by Christopher M. Bishop and Hugh. Bishop
## Chapter 2. Probabilities

### Introduction    
- Uncertainty in Machine Learning: Every machine learning applications deals with uncertainty. There are two steps.
    - Epistemic Uncertainty: arises from the finite size of data sets, and can be reduced by observing more data.
    - Aleatoric Uncertainty: also known as intrinsic or stochastic uncertainty, arises from partial information and cannot be eliminated by observing more data.
 


### 2.1 The Rules of Probability

![Screenshot 2024-06-20 at 10 11 41 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/2a95c4a4-e0fa-4fd4-ae3e-cdb271f51de3)

- A medical screening example
  - False Positives: a test result indicating a condition when it is not present (3% false positive rate for cancer when it was not cancer).
  - False Negative: a test result not indicating a condition when it is present (10% false negative rate for cancer when it was cancer).
 
  - Probability Calculation
    - Probability of testing positive: having test positive, regardless of having cancer.
      - p(T=1) = p(T=1 | C=0) / p(C=0) + p(T=1 | C=1) / p(C=1)
        = 3/100 * 99/100 + 90/100 * 1/100 = 0.0387
      - Thus, roughly 4% chance that the test comes out to be positive, even though there is a 1% chance having cancer.
    - Probability of having cancer given a positive test: when test was positive, probability of having cancer.
      - p(C=1 | T=1) = p(T=1 | C=1) X p(C=1) / p(T=1)
        = 90/100 * 1/100 * 10000/387 = 0.23
      - If the test was positive, there is a 23% probability that the person actually have cancer.
      - In other words, even if the test was positive, there is 77% chance that the person do not have cancer.
      - It is because of the low (1%) prior probability (prior because it is available before observing the test result) of having cancer.


- Sum and Product Rules
![Screenshot 2024-06-20 at 10 18 29 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/77f83a1f-21e8-45c2-bdf3-a4a3a706568d)


### 2.2 Probability Densities
![Screenshot 2024-06-20 at 10 19 12 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/e1c1305b-9d78-4453-91ab-52435b10a17f)

     
### 2.3 Gaussian Distribution
![Screenshot 2024-06-20 at 10 19 35 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/f3175f0c-d4d0-48c2-a131-5ea9be636de1)

    
### 2.4 Expectations and Covariance
![Screenshot 2024-06-20 at 10 20 58 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/e4fe082d-9d3d-4541-b609-6fc71fd663eb)



