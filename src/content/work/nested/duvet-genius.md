---
title: VaR and ES using Monte Carlo
publishDate: 2020-03-04 00:00:00
img: /assets/VaR MonteCarlo.png
img_alt: Pearls of silky soft white cotton, bubble up under vibrant lighting
description: |
  We estimate the value at risk and the expected shortfall using the Monte Carlo method. 
  Check my python program on my github page, or directly on this link: 
  https://github.com/titouanolier
tags:
  - MonteCarlo
  - Value at risk
  - Expected Shortfall
---

> Understanding Value at Risk (VaR) and Expected Shortfall with Monte Carlo Simulation

In the realm of risk management, accurately quantifying the potential losses associated with financial assets is paramount. Two widely-used metrics for this purpose are Value at Risk (VaR) and Expected Shortfall (ES). In this article, we delve into the estimation of VaR and ES using the powerful Monte Carlo simulation technique.


<img src="/assets/MonteCarlo formula.JPG" />


> Fetching Stock Data:

Our journey commences with fetching historical stock data for a chosen asset—in this case, let's consider Apple Inc. (AAPL). Utilizing the yfinance library, we retrieve the adjusted close prices from January 1, 2013, to January 1, 2024.

> Calculating Daily Returns:

Having obtained the stock data, we compute the daily returns, representing the percentage change in price from one day to the next. This serves as the foundation for our subsequent analysis.

> Simulating Future Prices with Monte Carlo:

Harnessing the power of Monte Carlo simulation, we project future price movements of the asset. By randomly sampling from a normal distribution with mean and standard deviation derived from historical returns, we generate multiple potential price paths over a specified number of days.

<img src="/assets/VaR MonteCarlo Simulation.JPG" />

> Estimating Value at Risk (VaR):

VaR quantifies the maximum potential loss that a portfolio may face over a specified time horizon, at a given confidence level. We calculate VaR by determining the price threshold below which a certain percentage of simulated prices fall. This threshold corresponds to the potential loss at the chosen confidence level.

> Computing Expected Shortfall (ES):

Expected Shortfall, also known as Conditional VaR, provides additional insights beyond VaR by quantifying the average loss magnitude, given that losses exceed the VaR threshold. We compute ES by averaging the losses exceeding the VaR threshold, providing a more comprehensive measure of downside risk.

> Visualizing Results:

To enhance understanding, we visualize the results of our Monte Carlo simulation. A histogram depicting the distribution of simulated prices allows us to visualize the potential range of future outcomes. Additionally, we mark the VaR threshold on the plot for reference, highlighting the level of potential loss at the chosen confidence level.

<img src="/assets/VaR MonteCarlo.png" />


Monte Carlo simulation emerges as a powerful tool for estimating risk metrics such as VaR and ES. By simulating multiple plausible future scenarios, we gain valuable insights into the potential downside risks associated with financial assets. Through continued refinement and analysis, practitioners can leverage these insights to enhance risk management practices and make informed investment decisions in dynamic market environments.

