# Market Regimes & Adaptive Portfolio Construction

Exploratory study on market regime detection using Hidden Markov Models (HMMs) and dynamic portfolio asset allocation across 30 industry sectors.

## Project Overview
This repository implements a quantitative framework to identify latent market regimes (calm, normal, and stress) and dynamically adjust portfolio risk exposure across 30 industry sectors. 

* **Regime Detection:** Utilizes 3-state Hidden Markov Models (HMMs) and percentile-based stress indicators drawing on the CBOE Volatility Index (VIX), rolling volatility, and cross-industry correlations.
* **Portfolio Allocation:** Contrasts discrete industry bucket allocation with continuous regime-conditional ranking models optimizing for CVaR, maximum drawdown, and VIX beta.

---

## Key Performance Highlights
* **Sharpe Ratio:** Improved to **1.04** (Continuous Regime) compared to **0.59** for the market benchmark.
* **Max Drawdown Reduction:** Controlled maximum drawdown to **-36.08%**, outperforming the equal-weighted (**-52.96%**) and market (**-54.16%**) benchmarks.

---

## Repository Structure
* `market_regime_portfolio.ipynb`: Full interactive Jupyter notebook containing data preprocessing, model fitting, backtesting, and visualization code.
* `market_regime_portfolio_report.pdf`: Detailed 12-page research report breaking down hypotheses, mathematical formulations, and empirical results.

---

## Academic Disclaimer & Limitations
* **Educational Scope:** This repository is an exploratory academic backtesting study conducted for educational and research purposes.
* **In-Sample Design & Limitations:** The models analyze historical relationships and feature rolling indicators that exhibit lag during sudden market transitions (e.g., flash crashes, structural regime shifts). Results do not account for transaction costs, market impact, or live execution friction and should not be construed as financial or trading advice.
