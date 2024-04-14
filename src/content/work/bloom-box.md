---
title: Optimizing Portfolio Allocation
publishDate: 2019-12-01 00:00:00
img: /assets/portfolio allocation.png
img_alt: A bright pink sheet of paper used to wrap flowers curves in front of rich blue background
description: |
 Optimizing Portfolio Allocation with VaR: A Data-Driven Approach
  Check my python program on my github page, or directly on this link: 
  https://github.com/titouanolier
tags:
  - Allocation
  - Python
  - Optimisation
---

In the realm of finance, constructing a well-balanced investment portfolio is essential for managing risk and maximizing returns. Modern portfolio theory provides a framework for optimizing allocations based on historical data and risk preferences. In this article, we explore a data-driven approach to portfolio optimization using Value at Risk (VaR) and showcase how Python can be leveraged to achieve optimal asset allocation.

>Fetching Stock Data

We begin by fetching historical stock data for a selection of tickers from Yahoo Finance using the yfinance library. This data serves as the foundation for our analysis, providing insights into the historical performance of each stock.

>Calculating Daily Returns:

Using the downloaded data, we calculate the daily returns of each stock. These returns represent the percentage change in price from one day to the next and are crucial for assessing the performance and volatility of each asset.

>Defining the Initial Allocation:

We initialize the portfolio with an equal distribution of allocations across all selected stocks. This initial allocation serves as a starting point for our optimization process.

>Portfolio VaR Calculation:

We define a function to calculate the Value at Risk (VaR) of the portfolio at a 95% confidence level. VaR quantifies the maximum potential loss that the portfolio may face over a specified time horizon, providing valuable insights into downside risk.

>Optimization Process:

Utilizing the scipy.optimize.minimize function, we optimize the portfolio allocation to maximize VaR. We set constraints to ensure that the allocations sum to 1 and bounds to restrict allocations between 0 and 1 for each stock. The objective function seeks to minimize the negative VaR, effectively maximizing VaR.

<img src="/assets/function min.JPG" />

>Results and Analysis:

Upon optimization, we obtain the optimal allocation for the portfolio, maximizing VaR while adhering to the defined constraints and bounds. We present the allocation for each stock and quantify the portfolio VaR at a 95% confidence level.

 
Best Allocation:
AAPL: 0.02
MSFT: 0.04
GOOGL: 0.00
AMZN: 0.01
META: 0.00
TSLA: 0.00
BRK-B: 0.00
JNJ: 0.00
V: 0.00
PG: 0.01
NVDA: 0.00
DIS: 0.00
PEP: 0.00
HD: 0.09
INTC: 0.11
CSCO: 0.00
CMCSA: 0.04
PFE: 0.00
NFLX: 0.10
KO: 0.00
NKE: 0.00
MRK: 0.04
T: 0.09
ABT: 0.12
ORCL: 0.11
CRM: 0.08
ABBV: 0.00
ACN: 0.00
VZ: 0.04
WMT: 0.10
Portfolio VaR (95% confidence): -1.25%




In conclusion, our data-driven approach to portfolio optimization using VaR provides investors with a systematic method for constructing robust and well-diversified portfolios. By leveraging historical data and modern optimization techniques, investors can make informed decisions to mitigate risk and enhance returns in dynamic market environments.