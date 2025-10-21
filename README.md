# 📉 Stock Crash Early Warning System

A predictive alerting system that identifies short-term signals (15–30 day horizon) indicative of potential market crashes—powered by XGBoost modeling and sentiment-based context from financial headlines.

[![Power BI Report](https://img.shields.io/badge/View-PowerBI-yellow?logo=PowerBI)](https://powerbi.microsoft.com)
![Python](https://img.shields.io/badge/Language-Python-3776AB?logo=python&logoColor=white)
![Beautiful Soup](https://img.shields.io/badge/Library-Beautiful%20Soup-green?logo=beautifulsoup&logoColor=white)
![Web Scraping](https://img.shields.io/badge/Technique-Web%20Scraping-blue)
![yFinance](https://img.shields.io/badge/API-yFinance-lightorange)
![Sentiment Analysis](https://img.shields.io/badge/Task-Sentiment%20Analysis-yellow)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)

> *This is a personal portfolio project created for skill demonstration purposes only. Not intended for commercial use or code redistribution.*

---

## Overview

This project blends technical market data with NLP-based sentiment scoring to deliver a scalable **Early Warning System**. It identifies high-risk setups based on historical stock behavior, enriched by recent news sentiment to improve decision context.

-  Historical pattern detection for 7 US stocks *(MAANG + Microsoft + Tesla)* and 3 Indian stocks *(Reliance, Infosys Ltd, HDFC Bank)* 
-  Machine Learning-driven crash prediction using technical indicators
-  Real-time news scraping and sentiment scoring from **Finviz** and **Economic Times**
-  Fully interactive dashboard built in **Power BI** to visualize risk triggers and sentiment-weighted alerts

---

##  Methodology Highlights

- Stock data collected via `yfinance` spanning **5 years**
- Modeled short-term market inflection points using:
  - Logistic Regression
  - Random Forest
  - **XGBoost** *(final choice—best performance)*
- Crash flags and probabilities calibrated on features like:
  - `RSI_14`, `Volatility`, `MACD`, `MA_20`, `MA_50`, `Volume Surge`, `Max Drawdown_30`, `Daily Returns`, etc.

> Instead of predicting a literal crash for "today," the system evaluates if current conditions **resemble historical setups** that **typically preceded downturns within 15–30 days**.

### Sentiment Module

- Headlines fetched for each stock from curated sources
- Scored using `vaderSentiment.SentimentIntensityAnalyzer`
- Weighted into final risk scores to reflect public mood alongside technical signals

### Alert Logic
Alerts are triggered when:
- Crash Probability ≥ 70%
- Sentiment Score ≤ -0.5
- Volume spike ≥ 2× average
- Price drop ≥ 5% in 1 day”

---
## Tech Stack

| Component        | Tool/Library              |
|------------------|---------------------------|
| Data Extraction  | `yfinance`, `pandas`, `finviz`      |
| Web Scraping     | `requests`, `BeautifulSoup4` (`bs4`) |
| Modeling         | `scikit-learn`, `xgboost` |
| NLP Sentiment    | `vaderSentiment`, `bs4`   |
| Visualization    | **Power BI Desktop**      |
---

## 🚀 Results preview

[Stock Crash Early Warning Alerting Dashboard](./dashboard-preview/Stock%20Crash%20Early%20Warning%20System%20Report.png)  
> For python scripts and dashboard access, refer to the **google drive** link provided in the **resume**
---

## Dashboard Features

Built with **Power BI**, this dashboard highlights:

- 📈 **Risk alerts via sentiment-weighted composite scores**
- 📉 **Historical trend overlays and crash probability spikes**
- 🎛️ **Slicers to explore specific stock setups, timelines, and market reactions**
- ⚙️ **Designed for scalability** with incremental refreshes—dashboard stays current with market changes and latest sentiment signals.

---

##  Repository Contents

```bash
Stock-Crash-Early-Warning-System/
├── data_model/
      ├──Crash_Prediction_Results.csv
      ├──Daily_Sentiment_Data_for_Stocks.csv
      ├──News_Headlines_Data.csv
├── notebook_scripts/
      ├── 01_Model_Building.ipynb        # Data collection + predictive modeling
      ├── 02_Web_Scrapper.ipynb    # News extraction + sentiment computation
├── dashboard-preview/                              # Power BI report snapshot
├── requirements.txt                               # Package dependencies
├── LICENSE.md                                     # Attribution & usage guidelines
├── README.md                                      # Project overview
```
---

## License & Usage

This project is licensed under the **Creative Commons Attribution–NonCommercial–NoDerivatives 4.0 International License**.

> This repository is for demonstration purposes only. No reuse, modification, or redistribution is permitted without **explicit permission**.

View full terms in [LICENSE.md](./LICENSE.md) or [on Creative Commons](https://creativecommons.org/licenses/by-nc-nd/4.0/).

© Ramya V, 2025

---
## ✨ Author & Contact info 

Created by Ramya Vijayalayan as a portfolio project  



