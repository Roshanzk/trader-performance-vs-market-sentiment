# Trader Performance vs Market Sentiment
Analysis of trader performance on Hyperliquid under different Bitcoin sentiment regimes (Fear, Greed, Neutral). Includes EDA, segmentation, and actionable strategy insights for Primetrade.ai.

## Overview
This project examines whether Bitcoin market sentiment (Fear vs Greed) influences trader behaviour and profitability on Hyperliquid. The goal is to uncover patterns that can inform better trading strategies and segment‑specific recommendations.

## Datasets
**1. Trade Data (~211k rows)**
- Executions across 32 accounts
- Includes price, size, fees, timestamps, PnL

**2. Fear & Greed Index (2,644 days)**
- Daily sentiment score + category

## Methodology
- Loaded and validated both datasets  
- Extracted trading date + created flags (win/loss, long/short)  
- Aggregated trades to **account–day** level  
- Merged with corresponding daily sentiment  
- Compared performance across Fear, Greed, Neutral  
- Segmented traders by:
  - **Frequency** (High-Frequency vs Low-Frequency)
  - **Trade Size** (High-Size vs Low-Size)

## Key Insights
- **Fear days produce the highest average net PnL**, driven by volatility.  
- **High-Frequency traders** benefit the most from Fear conditions.  
- **Low-Size traders** respond aggressively to volatility and perform better on Fear days.  
- **High-Size traders** remain profitable but face higher risk on Fear days.

## Strategy Recommendations
- **HF traders:** Increase participation during Fear; reduce aggression on Greed.  
- **LF traders:** Maintain stable exposure; sentiment affects them less.  
- **Low-Size traders:** Lean into volatility on Fear days.  
- **High-Size traders:** Avoid scaling up during high-volatility Fear periods.

## How to Run
1. Clone the repository  
2. Install dependencies:
   ```
   pip install pandas numpy seaborn matplotlib
   ```
3. Open the notebook:
   ```
   trader_performance_vs_sentiment_analysis.ipynb
   ```
4. Run all cells top-to-bottom.

## Notes
All analysis is contained within the notebook and is reproducible.  
This project was completed as part of the Primetrade.ai Data Science Intern assignment.
