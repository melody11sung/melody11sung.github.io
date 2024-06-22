---
layout: post
title:  "Hedge Funds, Arbitrage"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

This is a summary made for ML4T class, 
referencing a book "What hedge funds really do: an introduction to portfolio management" (2014) by Romero and Balch.

  
## 1. Definition of Arbitrage
- The simultaneous purchase and sale of an asset to profit from a difference in the price.
- Exploits price discrepancies of identical or similar financial instruments in different markets or forms.


## 2. Types of Arbitrage
1) Pure Arbitrage
  - Involves no risk as the transactions are done simultaneously to lock in profits.
  - Example: Buying gold in one market at a lower price and selling it in another market at a higher price at the same time.
2) Risk Arbitrage:
  * Involves a certain level of risk as it often deals with future events.
  * Example: Merger Arbitrage, where one buys the stock of a company being acquired and shorts the stock of the acquiring company.


## 3. Arbitrage Strategies
1) Convertible Arbitrage:
  * Involves buying convertible securities and hedging by shorting the underlying stock.
  * Profits arise from the convertible security's price discrepancies and its underlying stock.
2) Fixed-Income Arbitrage:
  * Exploits price differences between related fixed-income securities.
  * Often involves Treasury bonds, interest rate swaps, and other fixed-income instruments.
3) Statistical Arbitrage:
  * Uses statistical and mathematical models to identify and exploit inefficiencies in the price relationships between securities.
  * Involves high-frequency trading and sophisticated algorithms.


## 4. Mechanics of Arbitrage

1) Execution Speed:
  * Essential to arbitrage success due to the rapid correction of price discrepancies.
  * High-frequency trading (HFT) and co-location of servers near exchanges are used to gain speed advantages.

2) Market Impact:
  * Arbitrage activities can help in making markets more efficient by correcting price discrepancies.
  * Large-scale arbitrage can influence market prices and liquidity.


## 5. Risks and Challenges

1) Execution Risk:
  * The risk that simultaneous transactions do not occur as planned, leading to potential losses.
  * Market volatility and liquidity can exacerbate this risk.

2) Model Risk:
  * The risk that the mathematical or statistical models used to identify arbitrage opportunities are flawed or based on incorrect assumptions.
  * Continuous monitoring and updating of models are necessary to mitigate this risk.

3) Regulatory Risk:
  * Changes in regulations can affect the feasibility and profitability of arbitrage strategies.
  * Compliance with regulations is crucial to avoid penalties and ensure long-term viability.


## 6. Example Equations and Calculations

1) Sharpe Ratio:
  * Sharpe Ratio = ( 𝑟_portfolio − 𝑟_risk-free ) / standard deviation of portfolio
  * Example: If the long-term nominal return for the S&P 500 is 10%, the risk-free rate is 2.5%, and the standard deviation is 15%, then:
    * Sharpe Ratio = ( 10% − 2.5% ) / 15% = 7.5% / 15% = 0.5
