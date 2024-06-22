---
layout: post
title:  "Hedge Funds, Valuation"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

This is a summary made for ML4T class, 
referencing a book "What hedge funds really do: an introduction to portfolio management" (2014) by Romero and Balch.


## 1. Company Valuation
* Successfull investments hinge on having a more accurate view of an asset's true value than the seller.
* Different market participants have varying views of value, creating investment opportunities.


## 2. Fundamental Analysis vs. Technical Analysis
* Fundamental Analysis: Based on a company's business operations and finances.
* Technical Analysis: Also known as "charting", this method focuses on historical price patterns and market data.


## 3. Key valuation methods

1) Book Value
  * An estimate based on the sum of a company's assets and liabilities.
  * Represents the net asset value (NAV) per share.
  * Book Value = Total Assets - Total Liabilities

2) Intrinsic Value
  * An estimate based on future dividends to be paid by the company.
  * It uses the same equation as the Present Value/ Future Value.
    
  * $PV = FV \over (1 + IR)^i$
  * where PV as present value, FV as future value, and IR as interest rate.
    - e.g. If a bond suggest 5% of interest rate and promise $1 value after an year:
      - It's present value is $1 \over (1 + 0.05)^1 = 0.95$,
      - meaning that we could pay $0.95 at present for future $1.
      
  * Likewise, Intrinsic Value = $\sum {FV \over  (1 + DR)^i} = FV \over DR$
    - DR = discount rate (= a measure of how risky we think an investment in a company might be).
    - e.g. If a company pays a divident of $2 per year, and the discount rate is considered as 4%.
      - It's intrinsic value is $ FV \over DR = 2 \over 0.04 = 50 $
     
3) Market Capitalization
  * calculates company value as the product of the number of outstanding shares in the market and the current share price.
  * e.g. if Apple has 1,000,000 outstanding shares, priced at $1,000 per share:
      * Apple's value based on the market cap would be $1 billion (1,000,000,000).

4) Earnings Growth
  * Projects future earnings to estimate the company's value.
  * Often involves models like the Price/Earnings (P/E) ratio.
  * Earnings Grouth Valuation = Current Earnings X (1 + g)^n
  * where g is the growth rate and n is the number of years.


## 4. Market Efficiency and inefficiencies

1) Efficient Market Hypothesis (EMH)
  * Asserts that financial markets are efficient in reflecting all available information in asset prices.
  * Despite this, hedge funds seek to exploit occasional inefficiencies where prices diverge from true values.

2) Investment opportunities
  * Appear when the current price of an asset diverges from the investor's estimate of its true value.
  * Opportunities for going long (if undervalued), or short (if overvalued).


## 5. Margin of safety
* popularized by Benjamin Graham, it involves buying stocks well below their intrinsic value to ensure a "margin of safety".
* this approach minimizes downside risk and maximizes potential returns.


## 6. Application of valuation methods
* Fundamental Analysis techniques: used by investors to independently value companies and identify discrepancies between market price and true value.
* Critical for making informed investment decisions.


## 7. Examples and case studies
* Ex1. If total assets are $10 million, and total liabilities are $4 million:
  * The company's book value: $6 million.
  * If there are 1 million shares, the book value per share is $6.

* Ex2. If expected dividend (D) is $2 per share, required rate of return (r) is 8%, and growth rate (g) is 3%:
  * The intrinsic value = $2 / (0.08 - 0.03) = $40 per share





