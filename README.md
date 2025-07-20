# AI in Finance: Stress Testing a Markowitz Portfolio

![Finance AI](https://img.shields.io/badge/Finance-AI-blue) 
![Python](https://img.shields.io/badge/Python-3.8%2B-green)

This project implements a dynamic Minimum Variance Portfolio using Markowitz portfolio theory with stress testing capabilities. It evaluates portfolio performance under normal and stressed market conditions using Value-at-Risk (VaR) and Expected Shortfall (ES) metrics.

## Project Overview

The implementation covers four key components:
1. **Data Collection & Preparation**: Historical price data for MSFT and GLD (2010-2025)
2. **Portfolio Construction**: Dynamic minimum variance portfolio with constraints
3. **Stress Testing Framework**: Normal and stressed VaR/ES calculations
4. **Model Evaluation**: Backtesting and performance comparison

## Key Features

- Dynamic covariance estimation using Ledoit-Wolf shrinkage
- Portfolio constraints (20-80% allocation range)
- Transaction cost modeling (0.1% per rebalance)
- Stress scenario generation with:
  - Volatility shocks (2.5x multiplier)
  - Fat-tailed distributions (Student-t with df=3)
  - Correlation asymmetry
- Comprehensive performance metrics:
  - Annualized return/volatility
  - Sharpe ratio
  - Maximum drawdown
  - VaR violation analysis

## Results Highlights

| Metric                | Min Var Portfolio | 60/40 Portfolio | S&P 500 |
|-----------------------|------------------:|----------------:|--------:|
| Total Return          | 54.27%           | 54.68%          | 33.13%  |
| Annualized Return     | 32.72%           | 32.94%          | 20.54%  |
| Annualized Volatility | 12.85%           | 14.46%          | 16.97%  |
| Sharpe Ratio          | 254.51%          | 227.77%         | 121.06% |
| Max Drawdown          | 5.75%            | 6.47%           | 18.90%  |

**Stress Test Results:**
- Stressed VaR: 123.6% higher than normal VaR
- Stressed ES: 369.6% higher than normal ES
- VaR violations: 3.4% (normal) vs 0.8% (stressed)

## Repository Structure
