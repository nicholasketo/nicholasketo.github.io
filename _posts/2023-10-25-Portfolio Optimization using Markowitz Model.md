---
title: "Portfolio Optimization using Markowitz Model"
layout: post
---


## Two Asset Portfolio Optimization

Using the Markowitz Model, I have created a portfolio optimization of VOO(Vanguard 500 Index Fund ETF) and BLV(Vanguard Long-Term Bond Index Fund ETF).

First, all the data was compiled from 2011 to 2019 for every month. The Growth Percentage was calculating looking at the adjusted close per month. The adjusted close is a more accurate representation as it takes into consideration stock splits and dividends. 

After taking the Growth Percentage, the mean, variance, standard deviation and sharpe ratio was calculated of both assets. The Sharpe ratio was 0.262154371 for VOO and 0.166307286 for BLV. The higher the sharpe ratio, the better its risk-adjusted performance. 

A negative Sharpe ratio could mean either the risk-free or benchmark rate is greater than the portfolio's historical or projected return or the portfolio's return is expected to be negative. 

After finding the Sharpe ratio for the individual assets, I moved on to calculating the Sharpe ratio with a distribution of the assets. After doing the calculations, the results shwoed that 50% in VOO and 50% in BLV gave the highest Sharpe ratio. 

![Markowitz Model .png](/nicholasketo.github.io/assets/Markowitz Model .png)
