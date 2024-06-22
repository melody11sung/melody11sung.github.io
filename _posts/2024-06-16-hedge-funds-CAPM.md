---
layout: post
title:  "Hedge Funds CAPM"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

This is a summary made for ML4T class, referencing a book "What hedge funds really do: an introduction to portfolio management" (2014) by J. Romero and T. Balch.


## CAPM (Capital Assets Pricing Model)
* Developed by Merton Miller, Franco Modigliani, and William Sharpe, who received the Nobel Prize in Economics in 1990.
* CAPM provides a rigorous framework for appraising and designing portfolios.
* The model is influential in both academic finance and practical investment management.   


## Basic Premise of CAPM   
* CAPM assumes markets are efficient, meaning that asset prices reflect all avialable information.
* Investors cannot consistently achieve returns higher than market averages without taking on additional risk.   

* According to CAPM, buying a broad market index (e.g. S&P 500) is a strategy likely to yield superior results compareed to most other strategies.
* Hedge funds challenge this view by seeking to outperform market indicies through active management.   



## Core Components of CAPM   
- CAPM calculates the expected return of an asset based on its risk relative to the overal market.

- ![Screenshot 2024-06-21 at 9 16 20 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/6cc81674-db17-4a4a-8866-af42e84a24f1)
- (Referenced from [OMSCS ML4T Notes](https://www.omscs-notes.com/machine-learning-trading/capital-assets-pricing-model/#the-capm-equation))

- Beta
  * Beta greater than 1 indicates higher volatility than the market,
  * Beta less than 1 indicates lower volatility than the market.
  * In general, the equation asserts that a significant portion of the return is affected by the market movement.
  * e.g. if a stock has a beta of 2, it means that when the market moves 1%, the stock moves 2%.

- Alpha
  * Meanwhile, alpha captures the residual.
  * The CAPM asserts that alpha to be 0, but technically, alpha is a random variable with an expectation to be 0.

- How to capture the values
  - When we plot the stock against SP500, the slope becomes beta, and the y-intercept becomes alpha.
  - However, this is just a historical data, that cannot be true for the future.
  - ![Screenshot 2024-06-21 at 9 23 54 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/5ccf475e-2e08-4a16-967b-e5ab23599f74)


## Two Stock Math   

1. If an active manager puts stock A $50 long, and stock B $50 short positions, and the market goes down 10%.
  * $r_a$ is 1 ($beta_a$) * -10 + 1 = -9%, making $50 * -9% = -$4.5
  * $r_b$ is - {2 ($beta_b$) * -10 - 1} = 21%, making $50 * 21% = $10.5
  * Total earning is -9 * 0.5 + 21 * 0.5 = 6%, and $6   

![Screenshot 2024-06-18 at 3 38 35 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/69386b7d-eec0-40f8-a23e-6938b7eba82e)

  - this approach may loose money even with accurate predictions of alpha and beta.   


2. For CAPM, to remove the market affect/risk ($r_m$), how could we make $\beta_p$ = 0?   

![Screenshot 2024-06-18 at 3 41 59 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/dd428e55-a564-48f3-89e8-8912167950f1)
   
  * $\beta_p = w_A * 1 + w_B * 2 = 0$
  * since B is short position, w_B should be a negabive value.
  * We also know that $abs(w_A) + abs(w_B) = 1$
  * Thus, $w_B = -1/3, and w_A = 2/3$   

![Screenshot 2024-06-18 at 4 02 48 PM](https://github.com/melody11sung/melody11sung.github.io/assets/125707768/2d7ff6ed-f237-4b1a-a2dd-736ec4edc7ac)


* In summary, if we have information about alpha, a prediction to which way it's going to go,
* and if we could minimize the market risk by finding beta_portfolio = 0,
* which can be done by finding the right weights of each individual stock,
* we could build a portfolio that is less exposed to market risk.   



## Systematic vs. Unsystematic risk   
* Systematic risk is risk interent to the entire market or market segment.
* it cannot be diversified away.

* Unsystematic risk is specific to a particular company or industry.
* it can be reduced through diversification.   



## Security Markeet Line (SML)   
* Graphical representation: the SML plots expected return of assets against their beta.
* The slope of the SML represents the market risk premium.
* E(Ri) = Rf + beta(E(Rm) - Rf)   
  
* Assets above the SML are undervalued (offering higher return for their risk),
* and below the SML are overvalued (offering lower return).   



## Practical application   
* CAPM helps in constructing portfolios that balance expected return with risk.
* It provides a basis for comparing the attractiveness of different investments.   



## Limitations   
* assums investors can borrow and lend at the risk-free rate.
* assums all investors have the same expectations and hold the market portfolio.
* does not account for anomalies like momentum and size effeccts.   

