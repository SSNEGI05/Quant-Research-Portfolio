# 05 — Nifty 50 vs India VIX: A Regime-Based Analysis

## Overview
Quantitative analysis of the relationship between India VIX and Nifty 50 
forward returns, with regime classification, mean reversion testing, 
and signal construction.

## Key Findings
- **VIX is mean-reverting** with a half-life of ~41 trading days (~2 months)
- **High VIX predicts higher forward returns**: 20-day mean +4.80%, hit rate 82.1%
- **Leverage effect is 3.2x asymmetric**: VIX reacts 3.2x more to market drops than rallies
- **India VIX is fairly priced**: Realized/Implied ratio = 1.05 (no significant variance risk premium)
- **VIX cycles**: Spikes build over ~5.5 months (median), recover in ~3.7 months
- **Low Vol Trap debunked**: Prolonged low VIX does NOT predict imminent spikes

## Methodology
- Expanding percentile regime classification (no look-ahead bias)
- Forward return analysis with next-day-open execution assumption
- Granger causality testing (bidirectional at multiple lags)
- Non-overlapping trade backtest (18 trades, 2010-2026)
- OHLCV intraday range analysis across VIX regimes

## Statistical Methods Used
- Augmented Dickey-Fuller test (stationarity)
- Jarque-Bera test (normality)
- Granger causality (predictive relationship)
- OLS regression (leverage effect, mean reversion)
- Autocorrelation analysis

## Data
- **Nifty 50**: Daily OHLCV from Yahoo Finance (2009-2026)
- **India VIX**: Daily close from Yahoo Finance (2009-2026)
- 4,249 aligned trading days

## Tools
Python, pandas, numpy, scipy, statsmodels, matplotlib, yfinance
