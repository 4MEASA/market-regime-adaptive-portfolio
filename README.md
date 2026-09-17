# Market Regimes & Adaptive Portfolio Construction

Exploratory academic backtesting study investigating latent market regime detection using Hidden Markov Models (HMMs) and dynamic asset allocation across 30 industry sectors[cite: 1, 2].

---

## Dataset & Scope
* **Data Sources:** Historical monthly return series spanning from the early 1990s through 2024 for **30 industry sector portfolios** combined with the **CBOE Volatility Index (VIX)** and term spread macroeconomic indicators.
* **Asset Universe:** 30 broad industry sectors representing diverse cyclical, neutral, and defensive classifications.

---

## Project Overview
This repository implements an adaptive quantitative framework to identify underlying market states (calm, normal, and stress) and dynamically manage risk exposure across industry portfolios[cite: 1, 2]. The core motivation of this project is empirical research and risk governance—specifically examining how dynamic exposure scaling and regime-conditional weighting affect metrics like Sharpe ratio, Value-at-Risk (VaR), and maximum drawdown[cite: 1, 2].

* **Dual-Model Regime Detection:** Combines a 3-state Gaussian Hidden Markov Model (HMM) with a percentile-based stress index incorporating the CBOE Volatility Index (VIX), rolling volatility, and rolling cross-industry correlations[cite: 1, 2].
* **Conservative Conflict Resolution:** When the HMM and percentile classifiers diverge, the framework defaults to the riskier state to ensure robust downside protection (**78% baseline agreement rate** between models)[cite: 1, 2].
* **Continuous Regime-Conditional Ranking:** Replaces rigid bucket classifications with a continuous score-based weighting model optimized for regime-specific characteristics (e.g., favoring returns during calm periods, and penalizing volatility, CVaR-5%, max drawdown, VIX beta, and volatility transmission during stress)[cite: 1, 2].

---

## Key Performance & Risk Highlights
* **Sharpe Ratio:** Improved to **1.04** (Continuous Regime Strategy) compared to **0.59** for the market benchmark and **0.72** for equal-weighted[cite: 1, 2].
* **Maximum Drawdown Control:** Contained max drawdown to **-36.08%**, outperforming both the equal-weighted benchmark (**-52.96%**) and the market benchmark (**-54.16%**)[cite: 1, 2].
* **Tail Risk Mitigation:** Reduced 5% Value-at-Risk (VaR-5%) to **-4.82%** (vs. **-7.60%** market) and worst-month loss to **-11.47%** (vs. **-17.20%** market)[cite: 1, 2].

---

## Repository Structure
* `market_regime_portfolio.ipynb`: Interactive Jupyter notebook containing end-to-end code for data processing, feature engineering, rolling correlations, HMM fitting, backtesting, and performance visualizations[cite: 1, 2].
* `market_regime_portfolio_report.pdf`: Detailed 12-page research report documenting background hypotheses, methodology breakdowns, empirical findings, and critical discussions on rolling indicator lag and correlation breakdown[cite: 1, 2].

---

## Academic Disclaimer & Limitations
* **Educational Scope:** This repository is an exploratory academic study conducted for educational and research purposes to demonstrate quantitative research capabilities and risk modeling[cite: 1, 2].
* **In-Sample Design & Frictionless Backtest:** The models rely on historical rolling indicators (VIX, volatility, cross-industry correlations) that exhibit inherent lag during abrupt structural market shifts and flash crashes[cite: 1, 2]. Results are presented on a frictionless backtesting basis—omitting transaction costs, market impact, and live execution friction—and should not be interpreted as financial, investment, or trading advice[cite: 1, 2].
