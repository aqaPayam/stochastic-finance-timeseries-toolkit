# Stochastic Processes for Financial Time Series (S&P 500)

Stationarity testing, Random Walk & GBM modeling, Gaussian Process Regression, Hidden Markov Models, and a simple backtested regime-based strategy — all in one Jupyter notebook using S&P 500 (^GSPC) data.


## 🚀 What’s inside
- **Data**: downloads S&P 500 index (^GSPC) with `yfinance`
- **Exploratory analysis**: trend, distributions, rolling mean/std, daily returns
- **Stationarity tests**: ADF, KPSS, Phillips–Perron; ACF/PACF diagnostics; transformations to achieve stationarity
- **Models**:
  - **Random Walk** (baseline) — interpretation & limitations
  - **Geometric Brownian Motion (GBM)** — parameter estimation & simulation
  - **Gaussian Process Regression (GPR)** — nonparametric regression on prices/returns
  - **Hidden Markov Model (HMM)** — regime detection & decoding
  - (Notebook scaffolding mentions SARIMAX/LSTM; adjust or extend as needed.)
- **Strategy**: simple **regime-based trading** using HMM states with a quick backtest and performance metrics


## 📊 Notes on methodology
- **Stationarity** is validated using multiple unit-root tests (ADF/KPSS/PP) and visual diagnostics (ACF/PACF).
- **GBM** is fit by estimating drift and volatility; simulations compare model paths to observed prices.
- **GPR** provides flexible, non-linear fits; be mindful of overfitting.
- **HMM** segments market **regimes** (e.g., bull/bear/sideways). The simple strategy buys in “risk-on” states and holds cash otherwise. You can refine rules and re‑test.
- Backtesting here is **educational**; it does **not** account for transaction costs, slippage, or out-of-sample walk-forward validation.

## 🧪 Reproducibility
- Results may change as `yfinance` retrieves updated market data.
- For stable experiments, pin package versions and cache a fixed CSV of price history.

## 🏷️ Suggested GitHub topics
`time-series` · `finance` · `stochastic-processes` · `yfinance` · `gaussian-process` · `hidden-markov-models` · `gbm` · `backtesting` · `python` · `jupyter-notebook`

