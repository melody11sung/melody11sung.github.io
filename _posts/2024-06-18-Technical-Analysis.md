---
layout: post
title: "Technical Analysis"
categories: [ML4T]
author_profile: true
sidebar_main: true
---


## Technical Analysis

## 1. Characteristics

- looks only at historical * price and volumn *, unlike fundamental analysis which uses factors like earnings, dividends, cash flow, book value, etc.
- compute statistics called indicators
- indicators are heuristics
- do not consider company value
- works better over the short period of time than over the long term.


## 2. Indicators - Momentum
- the relative price change over a certain number of days.

![Screenshot 2024-06-18 at 5 47 32 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/26820fdc-0ba9-4d23-91b1-852e35491a8c)

- $m_t = {p_t \over p_(t-n)} - 1$



## 3. Indicators - Simple Moving Average
- computes the average price over the previous n days, known as an n-day window.
- SMA plot looks like a smoothed version of the price chart, with a lag of the movement
- we focus on the crossovers between the current price and the SMA plot
- coupled with supporting momentum, a crossover might constitute a strong buy or sell signal.
- Also, the average price over a large enough window can be regarded as a estimated true value of the company.

![Screenshot 2024-06-18 at 5 57 43 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/f4e2121b-4ad8-4f6d-bcec-4a84a3cdc0d5)

- To quantify the SMA, we can calculate the ratio of the momentum.

  ![Screenshot 2024-06-18 at 6 01 49 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/08699542-0252-4018-8e74-b605a94da3ed)
  - Reference: [ML4T Notes](https://www.omscs-notes.com/machine-learning-trading/technical-analysis/)



## 4. Indicators - Bollinger Bands

![Screenshot 2024-06-18 at 6 14 02 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/c19aefce-5d90-4197-bc8f-6fdcad769fd9)
![Screenshot 2024-06-18 at 6 15 00 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/c7f8a9a1-7eb6-459e-90ff-febd05f971a2)
![Screenshot 2024-06-18 at 6 17 35 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/ca4ec223-5dc6-4b2f-9046-4f34933fb84d)



## 5. Normalization
- The parameters have different value ranges, making the machine learning algorighm place different importance among the indicators.
- To prevent that, we need normalization, which takes each of these parameters and compresses or stretches them so that they vary, on average, from -1 to 1, with a mean of 0
![Screenshot 2024-06-18 at 6 19 19 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/89126423-0f79-43c0-af31-b758035e457b)
