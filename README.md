Market News Sentiment & Impact Intelligence
### Global Financial Events Analysis — 3,024 Events | 18 Sectors | 20 Event Types | Python EDA
[financial_data.xlsx](https://github.com/user-attachments/files/26866014/financial_data.xlsx)
<img width="1485" height="878" alt="01_sector_distribution" src="https://github.com/user-attachments/assets/77a96481-d55e-40ac-8880-895cddff268a" />
[financial_EDA.ipynb](https://github.com/user-attachments/files/26866017/financial_EDA.ipynb)
![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![pandas](https://img.shields.io/badge/pandas-2.0-green?logo=pandas)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
# Market-News-Sentiment-Impact-Intelligence-Global-Financial-Events-Analysis-2025
## Overview

Financial markets generate hundreds of news events daily across sectors,
indices, and geographies. This project analyzes **3,024 global financial
news events** to answer three operational questions:

1. Which sectors absorb the most negative sentiment — and by how much?
2. Which market event types produce the largest and most *consistent* index swings?
3. Does trading volume predict market direction, or does sentiment matter more?

The findings provide a data-driven prioritization framework for market
monitoring — identifying which sectors and event types warrant the highest
alert sensitivity in a real-time surveillance system.
## Key Findings

| Finding | Detail |
|---|---|
| Highest negative sentiment sector | Construction & Real Estate (~38% negative) |
| Steepest average index drop | Stock Market Crash events (-2.5% to -3.0%) |
| Most unpredictable event type | Geopolitical Events (widest std deviation) |
| Sentiment vs Volume as predictor | Sentiment r=0.35 vs Volume r~0.00 |
| Panic selling pattern | Negative events occur across ALL volume levels |
## Dataset

| Attribute | Value |
|---|---|
| Records | 3,024 financial news events |
| Columns | 12 (Date, Headline, Source, Market_Event, Market_Index, |
|         | Index_Change_Percent, Trading_Volume, Sentiment, Sector, |
|         | Impact_Level, Related_Company, News_Url) |
| Sectors | 18 (Technology, Healthcare, Energy, Finance, etc.) |
| Market Indices | 18 global indices (Nifty, Sensex, S&P 500, Nasdaq, etc.) |
| Event Types | 20 (Market Rally, Stock Market Crash, IPO Launch, etc.) |
| Null handling | Sentiment nulls filled as Neutral; Index_Change nulls dropped |
| Final clean records | 2,863 |
## Analysis Structure

| # | Analysis | Business Question |
|---|---|---|
| 1 | Sector Coverage Distribution | Which sectors dominate news volume? |
| 2 | Sentiment Distribution by Sector | Where is negative sentiment concentrated? |
| 3 | Index Change by Market Event | Which events move markets most — and how consistently? |
| 4 | Trading Volume vs Index Change | Does volume amplify market direction? |
| 5 | Impact Level by Sector | Which sectors face the most high-impact events? |
| 6 | Correlation Matrix | How do sentiment, volume, and impact interrelate? |
| 7 | Market Event Summary Table | Frequency + impact profile of all 20 event types |
## Tech Stack

```python
pandas    # data loading, cleaning, groupby aggregations
numpy     # derived feature computation (abs change, encodings)
matplotlib # bar charts, scatter plots, error-bar charts, table viz
seaborn   # heatmap, scatterplot with hue encoding
openpyxl  # Excel file ingestion
```
## How to Run

```bash
git clone https://github.com/YOUR_USERNAME/market-news-sentiment-analysis
cd market-news-sentiment-analysis
pip install pandas numpy matplotlib seaborn openpyxl
jupyter notebook financial_EDA.ipynb
```
## Business Takeaway

Sentiment is a stronger directional signal than volume (r=0.35 vs r~0.00).
A sentiment-aware monitoring layer — prioritizing Construction, Real Estate,
and Energy sectors, with elevated sensitivity during Stock Market Crash and
Currency Devaluation events — would outperform a volume-threshold-only
alerting system based on this analysis.

