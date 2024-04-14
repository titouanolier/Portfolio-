---
title: Exotic Option Pricer 
publishDate: 2020-03-02 00:00:00
img: /assets/call up and in.JPG
img_alt: Iridescent ripples of a bright blue and pink liquid
description: |
  Use of two moduiles to price an exotic option using Monte Carlo and VBA. 
  Check my python program on my github page, or directly on this link: 
  https://github.com/titouanolier
tags:
  - VBA
  - Option Pricing
  - Exotic
---

> Definition

Exotic options are financial derivatives that possess non-standardized features, distinguishing them from traditional options such as calls and puts. These options often incorporate complex structures or conditions, providing investors with unique risk management and investment opportunities. Unlike standard options traded on exchanges, exotic options are typically customized contracts tailored to specific needs or market conditions. 

Let's dive into the explanation of the VBA code for pricing exotic barrier options using both the binomial tree and Monte Carlo simulation methods.

> BarrierOption Module in VBA:

This module calculates prices for exotic barrier options, specifically "up-and-out" options, using the binomial tree method. Here's a brief overview:

Sub UpAndOutBarrierOption(): This procedure initializes parameters and calls functions to calculate call and put option prices.

Function UpAndOutBarrierCall(): Estimates the price of an "up-and-out" call option using the binomial tree method with a knockout barrier.

Function UpAndOutBarrierPut(): Estimates the price of an "up-and-out" put option using put-call parity and the calculated call option price.

>MonteCarloSimulation Module in VBA:

This module estimates prices for the same exotic "up-and-out" barrier options, but using the Monte Carlo simulation method. Here's a summary:

Sub UpAndOutBarrierOptionMonteCarlo(): Initializes parameters and calls functions to estimate call and put option prices using Monte Carlo simulation.

Function UpAndOutBarrierCallMonteCarlo(): Simulates asset price paths using Monte Carlo and computes the average payoff for "up-and-out" call options.

Function UpAndOutBarrierPutMonteCarlo(): Estimates the price of an "up-and-out" put option using put-call parity and the call option price obtained from Monte Carlo simulation.


These modules work together to provide price estimates for exotic options using both the binomial tree and Monte Carlo simulation methods.
