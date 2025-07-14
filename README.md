# 📉 Stock Crash Early Warning System

A predictive alerting dashboard that identifies short-term signals (15–30 day horizon) indicative of potential market crashes—powered by XGBoost modeling and sentiment-based context from financial headlines.

[![Power BI Report](https://img.shields.io/badge/View-PowerBI-blue?logo=PowerBI)](https://powerbi.microsoft.com)
![Python](https://img.shields.io/badge/Language-Python-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Library-Pandas-yellow?logo=pandas&logoColor=white)
![Beautiful Soup](https://img.shields.io/badge/Library-Beautiful%20Soup-green?logo=beautifulsoup&logoColor=white)
![Web Scraping](https://img.shields.io/badge/Technique-Web%20Scraping-blue)
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
## 📌 Tech Stack

| Component        | Tool/Library              |
|------------------|---------------------------|
| Data Extraction  | `yfinance`, `pandas`      |
| Web Scraping     | `requests`, `BeautifulSoup4` (`bs4`) |
| Modeling         | `scikit-learn`, `xgboost` |
| NLP Sentiment    | `vaderSentiment`, `bs4`   |
| Visualization    | **Power BI Desktop**      |
---

## 🚀 Quick Access

[![View Dashboard in Power BI](https://img.shields.io/badge/View-Dashboard-blue?logo=PowerBI)](https://powerbi.microsoft.com)  
[![Explore Notebook in Jupyter](https://img.shields.io/badge/Explore-Notebook-yellow?logo=Jupyter)](https://jupyter.org)  

---

## 🖥️ Dashboard Features

Built with **Power BI**, this dashboard highlights:

- 📈 **Risk alerts via sentiment-weighted composite scores**
- 📉 **Historical trend overlays and crash probability spikes**
- 🎛️ **Slicers to explore specific stock setups, timelines, and market reactions**
- ⚙️ **Designed for scalability** with incremental refreshes—dashboard stays current with market changes and latest sentiment signals.

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
```
---
## 🧪 Setup Instructions

1. **Clone repo locally**
2. **Run each notebook in sequence**:
   - `01_StockData_Modeling_XGBoost.ipynb`
   - `02_NewsScraping_SentimentScoring.ipynb`
3. **Open dashboard from `dashboard_assets/` in Power BI**

```bash
pip install -r requirements.txt
```
---
## 📜 License & Usage

This project is licensed under the **Creative Commons Attribution–NonCommercial–NoDerivatives 4.0 International License**.

> 🔒 Redistribution, reproduction, or code reuse without **explicit credit** is prohibited. Please respect the creative intent and ownership.

View full terms in [LICENSE.md](./LICENSE.md) or [on Creative Commons](https://creativecommons.org/licenses/by-nc-nd/4.0/).

© Ramya Vijayalayan, 2025

---
## 📬 Author & Contact Info

For project insights or review requests:

**Ramya Vijayalayan**  
📧 [vrmya2510@gmail.com]  
🔗 [LinkedIn Profile](https://linkedin.com/in/ramya-vijayalayan-9a51b2289)

