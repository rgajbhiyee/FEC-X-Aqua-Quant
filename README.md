## 📈 ML-Based Market Regime Detection (Ongoing)

This project explores machine learning and statistical modeling techniques for market regime detection using financial time-series data.
The goal is to identify Bull, Bear, and Sideways regimes and study how regime-aware decision rules can guide portfolio construction.

## 🧠 Approach

Began with GARCH(p, q) models for volatility estimation

Compared models using AIC and BIC, selecting EGARCH(1,1) for:

Asymmetric volatility behavior

Better handling of fat-tailed returns

Engineered additional features:

20-day momentum

Drawdown from rolling peak

Volatility trend

## 📊 Regime Classification Logic

Each stock is classified daily into:

Bull: positive momentum, low-to-moderate volatility, shallow drawdown

Bear: high volatility with deep drawdown, negative momentum, or rising volatility

Neutral: all other market conditions

Regimes are smoothed using short persistence rules to reduce noise.

## 📁 Portfolio Construction

Universe: NIFTY 50 stocks

Regimes are detected independently for each stock

Weekly rebalancing

Capital is allocated to Bull regime stocks

Weights are based on volatility-adjusted momentum

Bear regime stocks are excluded from investment

## 🔮 Future Work

Hidden Markov Models (Gaussian & Student-t) for regime detection

Ensemble / probabilistic regime voting across models

Reinforcement learning for adaptive regime confidence

Improved validation and robustness testing

Model selection and regime inference are treated as a probabilistic learning problem on time-series data.
