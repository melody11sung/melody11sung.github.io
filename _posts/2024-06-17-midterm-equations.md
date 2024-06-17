---
layout: post
title:  "Trading Equations for ML4T"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

### Trading Equations for ML4T
  
##### 1. Global Statistics

* Daily Returns: The percentage change in the portfolio's value from one day to the next.
* $$ DailyReturn_t = {{Price_t \over Price_(t-1) } - 1 } $$

* Cumulative Returns: the total return of a stock over a large period of time starting from a specific date t0.
* $$ Cumulative Return_t = {{Price_t \over Price_t0 } - 1 }$$

* Rolling Mean: the average price of a stock over a specified window of time.

* Bollinger Bands: measures a stock's volatility using the rolling standard deviation
* $$ Upper band = {Rolling Mean + 2 * Rolling Std Dev }$$
* $$ Lower band = {Rolling MEan - 2 * Rolling Std Dev }$$


##### 2. Sharpe Ratio

* A measure of risk-adjusted return
* $$ S = {E[R_p - R_f] \over std[R_p = R_f]} $$
* where E[R_p] = expected portfolio return,
* R_f = Risk-free rate,
* std[R_p - R_f] = standard deviation of excess return.

* if different sampling frequencies adjustment:
* $$ S = {k * E[R_p - R_f] \over std[R_p = R_f] }$$
* where $$ k = \sqrt{Number of periods per year}


##### 3. Capital Asset Pricing Model (CAPM)

* A model used to determine the expected return of an asset based on its risk relative to the market
* $$ E(R_i) = { R_f + \beta{(E(R_m) - R_f)} $$
* where E(R_i) = expected return of the asset,
* R_f = risk-free rate,
* beta = beta of the asset,
* E(R_m) = expected market return,
* (E(R_m) - R_f) = market risk premium.


