# 📉 Stock Crash Early Warning System

A predictive alerting dashboard that identifies short-term signals (15–30 day horizon) indicative of potential market crashes—powered by XGBoost modeling and sentiment-based context from financial headlines.

[![Power BI Report](https://img.shields.io/badge/View-PowerBI-blue?logo=PowerBI)](https://powerbi.microsoft.com)
[![Notebook Viewer](https://img.shields.io/badge/Explore-Notebook-yellow?logo=Jupyter)](https://jupyter.org)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

> *This is a personal portfolio project created for skill demonstration purposes only. Not intended for commercial use or code redistribution.*

---

## 🚀 Overview

This project blends technical market data with NLP-based sentiment scoring to deliver a scalable **early warning system**. It identifies high-risk setups based on historical stock behavior, enriched by recent news sentiment to improve decision context.

- 🔍 Historical pattern detection for 7 US stocks *(MAANG + Microsoft + Tesla)* and 3 Indian stocks *(Reliance, Infosys Ltd, HDFC Bank)*
- 🧠 Machine Learning-driven crash prediction using technical indicators
- 📰 Real-time news scraping and sentiment scoring from **Finviz** and **Economic Times**
- 📊 Fully interactive dashboard built in **Power BI** to visualize risk triggers and sentiment-weighted alerts

---

## 🧠 Methodology Highlights

- Stock data collected via `yfinance` spanning **5 years**
- Modeled short-term market inflection points using:
  - Logistic Regression
  - Random Forest
  - XGBoost *(final choice—best performance)*
- Crash flags and probabilities calibrated on features like:
  - `RSI_14`, `Volatility`, `MACD`, `MA_20`, `MA_50`, `Volume Surge`, `Max Drawdown_30`, `Daily Returns`, etc.

> Instead of predicting a literal crash for "today," the system evaluates if current conditions **resemble historical setups** that **typically preceded downturns within 15–30 days**.

### 📰 Sentiment Module

- Headlines fetched for each stock from curated sources
- Scored using `vaderSentiment.SentimentIntensityAnalyzer`
- Weighted into final risk scores to reflect public mood alongside technical signals

---

## 📁 Repository Contents

```bash
📦 Stock-Crash-Early-Warning-System/
├── python notebook scripts/
      ├──01_StockData_Modeling_XGBoost.ipynb        # Data collection + predictive modeling
      ├── 02_NewsScraping_SentimentScoring.ipynb    # News extraction + sentiment computation
├── dashboard_assets/                              # Power BI files & reports
├── requirements.txt                               # Package dependencies
├── LICENSE.md                                     # Attribution & usage guidelines
├── README.md                                      # Project overview
