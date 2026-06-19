# Quantitative Momentum: A Practitioner's Guide

This repository contains a 7-day guided implementation of the trading architecture described in **"Quantitative Momentum: A Practitioner's Guide to Building a Momentum-Based Stock Selection System"** by Wesley R. Gray and Jack R. Vogel.

This project shifts away from high-frequency statistical arbitrage and focuses on lower-turnover, behaviorally driven factor investing. It constructs a systematic stock selection engine that identifies high-quality, continuous price trends while actively managing the risk of catastrophic "momentum crashes."

## 🛠️ Tech Stack
* **Language:** Python
* **Environment:** Jupyter Notebooks / Google Colab
* **Key Libraries:** `pandas`, `numpy`, `statsmodels`, `yfinance`, `matplotlib`

## 📅 The 7-Day Quantitative Momentum Architecture

Each folder contains a standalone Colab notebook translating Gray and Vogel's behavioral theories into a systematic trading pipeline.

| Day | Core Concept | Implementation Project |
| :--- | :--- | :--- |
| **Day 1: The Academic Baseline (12m-1m)** | Standard Momentum (WML), Short-term mean reversion, The 1-month skip. | Building the baseline cross-sectional momentum screener. Calculating the 12-month return while deliberately stripping out the most recent month's return. |
| **Day 2: Momentum Crashes & Trend Filters** | The "Bear Market Rally" trap, Absolute vs. Relative Momentum, Time-series rules. | Engineering a dual-momentum regime filter using the 200-day moving average to dynamically hedge the portfolio and prevent momentum crashes. |
| **Day 3: The "Frog-in-the-Pan" (High-Quality Momentum)** | Continuous vs. Discrete Information, Path smoothness, Investor attention. | Coding the "Information Discrete-ness" (ID) or Path Smoothness score ($R^2$ of the price path) to filter out jumpy, earnings-driven momentum in favor of smooth, steady trends. |
| **Day 4: Seasonality & The Rebalancing Premium** | Window dressing, Tax-loss harvesting bounce, Quarter-end dynamics. | Implementing a seasonal rebalancing engine that optimizes the exact timing of portfolio turnover (e.g., rebalancing prior to quarter-end markups). |
| **Day 5: Portfolio Construction (Concentration)** | Equal-weighting vs. Value-weighting, The "Diworsification" problem. | Constructing an Equal-Weighted, highly concentrated portfolio of the top 50 momentum names, actively breaking the Market-Cap weighting trap. |
| **Day 6: The Holy Grail (Value + Momentum)** | Factor correlation, Blending methodologies, Diversifying behavioral biases. | Engineering a multi-factor ranking system that blends Deep Value metrics (EBIT/TEV) with High-Quality Momentum to create a highly robust cross-sectional strategy. |
| **Day 7: The Production Momentum Engine** | End-to-end system integration, Turnover calculations, Out-of-sample backtest. | Building the final pipeline: Screening the universe, applying the 12m-1m rule, filtering for path smoothness, applying the trend-filter hedge, and calculating historical equity curves. |

## 🧠 Core Philosophy
> *"Momentum is a behavioral anomaly, not a risk premium."* This project operates on the premise that markets are not perfectly efficient because human investors suffer from cognitive biases (anchoring, disposition effect). By systematically buying stocks with smooth, continuous momentum and equal-weighting them, we can harvest the premium left behind by emotional investors.

## 📖 Reference
* Gray, Wesley R., and Jack R. Vogel. *Quantitative Momentum: A Practitioner’s Guide to Building a Momentum-Based Stock Selection System*. Wiley, 2016.
