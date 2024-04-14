---
title: Markowitz efficient frontier
publishDate: 2020-03-02 00:00:00
img: /assets/efficient frontier.png
img_alt: Iridescent ripples of a bright blue and pink liquid
description: |
  Implementation of the markowitz efficient frontier, and visualisation of the optimal portfolio. 
  Check my python program on my github page, or directly on this link: 
  https://github.com/titouanolier
tags:
  - Markowitz
  - Portfolio Management
  - Optimisation
---

> Exploring Modern Portfolio Theory with Python

In the realm of finance, making informed investment decisions is paramount. Modern Portfolio Theory (MPT), developed by Nobel laureate Harry Markowitz, provides a framework for constructing portfolios that optimize the trade-off between risk and return. In this article, we delve into MPT using Python, simulating portfolios and visualizing the efficient frontier to identify optimal investment strategies.

<img src="/assets/Markowitz.jpg" />


> Setting the Stage:

We kick off our journey by importing essential libraries such as numpy, yfinance, and matplotlib.pyplot. These tools empower us to conduct numerical computations, fetch historical stock data, and visualize results seamlessly.

> Data Acquisition and Preparation:

Our journey begins by defining our universe of assets—two tech giants, Apple Inc. (AAPL) and Microsoft Corporation (MSFT). Utilizing the yfinance library, we fetch their adjusted closing prices from January 2010 to January 2023. These prices serve as the foundation for our analysis.

> Calculating Returns and Initialization:

With our data in hand, we compute the daily returns of the selected stocks. These returns provide insights into the performance of each asset over time. Additionally, we initialize arrays to store weights, returns, volatilities, and Sharpe ratios for our simulated portfolios.

> Simulating Portfolios:

The heart of our analysis lies in simulating random portfolios. Leveraging the power of Python, we iterate through thousands of portfolio combinations, assigning random weights to each asset while ensuring they sum up to one. With these weightings, we calculate the expected return, volatility, and Sharpe ratio for each portfolio, incorporating Markowitz's pioneering insights into portfolio optimization.

<img src="/assets/code markowitz.JPG" />

> Identifying the Optimal Portfolio:

After simulating a myriad of portfolios, we pinpoint the holy grail—the portfolio with the highest Sharpe ratio. This portfolio represents the pinnacle of risk-adjusted returns, showcasing the epitome of Markowitz's vision.

> Visualizing the Efficient Frontier:

To provide clarity and insight, we visualize our findings through the lens of the efficient frontier. This graphical representation illustrates the spectrum of risk-return trade-offs available to investors, with each point on the frontier representing a unique portfolio. Through color coding, we highlight the portfolio with the maximum Sharpe ratio, guiding investors towards optimal asset allocation strategies.

<img src="/assets/efficient frontier.png" />


Our exploration of modern portfolio theory using Python underscores the timeless wisdom of Harry Markowitz. By leveraging computational tools, we enable investors to navigate the complex landscape of financial markets, constructing portfolios that maximise returns while minimising risk. However, this model does not take into account well-established assumptions such as no transaction costs or taxes for investors, or the assumption that all investors are rational. Furthermore, this model does not take into account investors' market expectations. Through continuous innovation and analysis, we strive to open new frontiers in portfolio optimisation, guiding investors to prosperity in a constantly changing world.