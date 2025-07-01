# Quant_Finance_BootCamp_Project

This project series applies quantitative finance techniques to analyze real stock data, estimate portfolio risk, simulate option pricing behavior, and evaluate hedging performance under varying market conditions. The analysis spans four mini projects, each targeting a key concept using both theoretical models and empirical methods.

Mini Project 1 – Normality of Log Returns
I collected historical closing prices from 8 major stocks (e.g., AAPL, MSFT, AMZN, NVDA) from Yahoo Finance (2015–2025), then computed daily log returns. We tested these returns for normality using Shapiro-Wilk and Anderson-Darling tests — two statistical methods that assess how closely data follows a normal distribution.

Why: Normality is a key assumption in many financial models.

What I found:

Raw stock returns often failed normality tests.

Removing extreme values (outliers) using a z-score method made some distributions appear normal.

Using a rolling time window (252 days) revealed that normality is time-varying, valid in calm markets but not in volatile ones.

This highlights the importance of checking assumptions over time and cleaning data before modeling.

Mini Project 2 – Value at Risk (VaR)
I constructed an equal-weighted portfolio using the same stocks and estimated Value at Risk (VaR) — a common risk measure showing the maximum expected loss over a given time horizon at a certain confidence level.

Methods used:

Parametric VaR: Assumes returns are normally distributed (mean-variance based).

Historical VaR: Uses actual past returns, without assuming any distribution.

What I found:

Historical VaR better captured market risk, especially when returns deviated from normality.

Backtesting showed that parametric VaR underestimated risk during turbulent periods.

This shows that model assumptions significantly affect risk estimates, and non-parametric methods may be safer in real markets.

Mini Project 3 – Black-Scholes Option Pricing
I simulated how the price and rate of change (delta) of European call and put options change with time to expiration and spot price, using the Black-Scholes model.

Why: To visually understand how option prices behave as market variables change.

Inputs: Spot price, strike price, volatility, time, and interest rate.

What I found:

Option values decrease over time (time decay), especially as expiration nears.

Sensitivity to price (delta) varies with moneyness — delta is highest when spot ~ strike.

Visualizations gave intuition on how calls and puts react differently to time and price.

This helps interpret Greeks (sensitivity measures) and how traders manage risk.

Mini Project 4 – Delta Hedging with Stochastic Volatility
I explored how delta hedging performs when volatility is not constant, which is often true in real markets. I simulated thousands of price paths using:

A custom model with randomly changing volatility per step.

The Heston model, where volatility evolves stochastically over time.

The GARCH model, which captures volatility clustering in time series.

We applied Black-Scholes delta hedging on each path and tracked profit/loss.

What we observed:

With constant volatility, hedging works well.

With changing volatility, hedging becomes imperfect, leading to varied profit distributions.

The Heston model showed fat tails, suggesting more extreme outcomes.

The GARCH model produced more clustered, realistic volatility patterns.

These findings reinforce that modeling realistic volatility is crucial for hedging and pricing derivatives accurately.

Take Home Point
Across all projects:

Real stock returns are not always normal and often include outliers.

Historical data and rolling tests are essential for understanding risk.

Option sensitivity varies with market conditions, which is critical for traders.

Stochastic volatility models like Heston and GARCH provide a better framework for simulating market behavior and evaluating hedging strategies.

Together, these projects illustrate how to combine statistical analysis and financial modeling to better understand and manage real-world market risks.


