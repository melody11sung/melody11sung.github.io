---
layout: post
title:  "Hedge Funds Ch9. Active Portfolio"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

This is a summary made for ML4T class, referencing a book "What hedge funds really do: an introduction to portfolio management" (2014) by Romero and Balch.

## Chapter 9. The Fundamental Law of Active Portfolio Management.
  
1) Fundamental Law of Active Portfolio Management
- developed by Richard Grinold
- serves as a quantitative tool that links a manager's performance directly to their skills, the breadth of their investment decisions, and the effectiveness of implementing those decisions.

2) Key Concepts
- Information Ratio (IR)
  - It measures the manager's ability to generate excess returns per unit of risk, relative to a benchmark.
  - IR = E(Return - Return_benchmark) / std(Return - Return_benchmark)
  - expected excess return over the standard deviation of the excess return.
    
- Information Coefficient (IC)
  - Represents the skill of the manager in forecasting asset returns.
  - It is a correlation between predicted and actual asset returns, ranging from -1 to 1.

- Breadth (BR)
  - Defined as the number of independent investment decisions or bets a manager makes over a given time period.
  - Higher breadth implies more opportunities to utilize forecasting skills.
  - Higher breadth allows for a more reliable estimate of IR due to the law of large numbers.

- Transfer Coefficient (TC)
  - Measures how effectively a manager's forecasts are translated into actual portfolio positions.
  - It reflects the fidelity with which a manager's views are implemented.
  - Higher TC indicates that the manager is effectively translating forecasts into proofitable trades.
 
- Active Risk
  - The risk (standard deviation) of the excess returns of the portfolio over the benchmark.

3) The Fundamental Law Equation
- IR = IC * root(BR) * TC
- How to utilize the law in practice:
  - Enhancing the IC by improving forecasting skills, such as better data analysis techniques and continuous learning.
  - Increasing the BR through diversification across many independent bets.
  - Optimizing the TC by aligning the portfolio with the manager's forecast as closely as possible, reducing any friction that might dilute performance.
- limiations
  - challenges of accurately estimating IC and BR
  - assumptioon that all decisions are independant.
  
