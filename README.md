# Commodity Trading Strategies

## Overview

This project explores quantitative trading strategies applied to commodity-related assets, with a particular focus on the palm oil sector.

The objective is to identify statistical relationships between economically related assets and exploit temporary market inefficiencies through systematic trading strategies. The project combines statistical arbitrage, cointegration analysis, portfolio optimization and backtesting techniques commonly used in quantitative finance.

Developed as part of the Financial Engineering program at ESILV.

---

## Project Objectives

The project investigates whether market-neutral strategies can generate consistent returns by exploiting mean-reverting relationships between commodity-linked assets.

Two complementary approaches were developed:

### Game 1
Market-neutral statistical arbitrage strategy based on:

- Correlation analysis
- Cointegration testing
- Z-score trading signals
- Portfolio optimization
- Risk-adjusted position sizing

### Game 2
Optimized pair trading strategy inspired by academic research on multivariate statistical arbitrage and quantitative portfolio construction.

---

## Methodology

### Asset Selection

The strategy focuses on the palm oil sector using:

- RJA Commodity Index (benchmark asset)
- AALI
- LSIP
- SIMP
- SMAR
- SSMS

These assets were selected because they share common economic drivers and are exposed to similar commodity market conditions. :contentReference[oaicite:0]{index=0}

---

### Statistical Analysis

#### Correlation Analysis

A correlation matrix is used to identify assets exhibiting similar market behavior and potential statistical relationships. :contentReference[oaicite:1]{index=1}

#### Cointegration Testing

Cointegration tests are performed to identify long-term equilibrium relationships between assets.

This ensures that price deviations are expected to revert over time, which is a key assumption for statistical arbitrage strategies. :contentReference[oaicite:2]{index=2}

---

### Signal Generation

For each asset, a spread is constructed relative to the commodity benchmark:

\[
Spread = \log(Stock Price) - \log(Index Price)
\]

The spread is standardized using a Z-score.

Trading rules:

- Z-score > 2 → Short position
- Z-score < -2 → Long position

The strategy assumes that extreme deviations will revert toward their historical mean. :contentReference[oaicite:3]{index=3}

---

### Portfolio Optimization

Portfolio weights are determined using Gurobi optimization.

The optimization objective balances:

- Expected return
- Portfolio risk
- Market neutrality constraints

A market-neutral condition is imposed to minimize exposure to overall market movements. :contentReference[oaicite:4]{index=4}

---

### Backtesting

The strategy is evaluated using:

- Daily returns
- Transaction costs
- Market-neutral portfolio construction
- Benchmark comparison

To avoid look-ahead bias, portfolio weights from the previous trading day are used during the simulation. :contentReference[oaicite:5]{index=5}

---

## Results

### Optimized Strategy

Performance achieved during the test period:

- Total Return: ~14.7%
- Annualized Return: ~8.1%
- Volatility: ~7.9%
- Sharpe Ratio: ~1.03
- Maximum Drawdown: ~-9.8%

The optimized portfolio generated lower volatility and smoother performance than the benchmark strategy while maintaining attractive risk-adjusted returns. :contentReference[oaicite:6]{index=6}

---

## Quantitative Finance Concepts

This project covers several key quantitative finance topics:

- Statistical Arbitrage
- Pair Trading
- Cointegration
- Correlation Analysis
- Mean Reversion
- Market-Neutral Strategies
- Portfolio Optimization
- Gurobi Optimization
- Risk Management
- Backtesting
- Sharpe Ratio Analysis

---

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-Learn
- Gurobi
- Jupyter Notebook

---

## Project Structure

```text
.
├── Game1.ipynb
├── Game2.ipynb
├── Report_Game1.pdf
├── Research_Paper.pdf
├── datasets/
└── README.md
```

---

## Learning Outcomes

Through this project, I gained practical experience in:

- Designing statistical arbitrage strategies
- Applying cointegration analysis to financial markets
- Building market-neutral portfolios
- Portfolio optimization using Gurobi
- Backtesting systematic trading strategies
- Evaluating risk-adjusted performance

