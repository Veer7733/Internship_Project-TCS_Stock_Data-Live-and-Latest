# Internship_Project-TCS_Stock_Data-Live-and-Latest
---
# TCS Stock Price Analysis & Forecasting using Machine Learning

A comprehensive data analysis and stock price prediction project on **Tata Consultancy Services (TCS)** using historical financial data from **2002 to 2021**. This project explores stock trends, trading behavior, and financial patterns through EDA and implements predictive models to forecast future closing prices. The analysis supports strategic decision-making for trading insights and investment planning.

---

## Project Objective

- Analyze TCS stock performance over time
- Identify price trends, market movement, and volatility
- Engineer features based on trading indicators
- Develop machine learning models to **predict future closing prices**
- Generate **data-backed insights** to support stock trading strategies

---

## Dataset Details

Extracted from historical TCS stock records  
**Total Records:** 4,463 rows  
**Columns:** 8 (Open, High, Low, Close, Volume, Dividends, Stock Splits, Date)  
**Time period:** *12 August 2002 – 30 September 2021*

| Column | Description |
|--------|-------------|
| Date | Trading day |
| Open | Opening price |
| High | Intraday high |
| Low | Intraday low |
| Close | Closing price |
| Volume | Shares traded |
| Dividends | Payouts |
| Stock Splits | Corporate actions |

✔ No duplicate or missing values found in data. 
✔ Converted dates to `datetime`, sorted chronologically. 

---

## Tools & Technologies

| Category | Tools |
|----------|------|
| Language | Python |
| Notebook | Jupyter Notebook |
| Libraries | Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels |
| Domain | Data Analytics, Machine Learning |

---

## Exploratory Data Analysis (EDA)

### Time-Based Trends
- **Steady stock growth from 2002 to 2021** with significant upward momentum post-2016.
- **Highest price months:** August & September. *(Based on visualization)* 
- **Highest trading volume:** April & October. 
- **Major volume spikes after 2003.** 

### Moving Averages & Trading Strategy
- Implemented **30-day and 5-day moving averages**.  
- Generated **Buy/Sell trading signals using SMA crossover** (5-day vs 30-day). 

### Market Volatility
- Price stable on most days, but **contains significant outliers** during high market activity. 

---

## Feature Engineering

Generated additional features for improved prediction accuracy:
- `Year`, `Month`
- `ST_MA` (5-day short-term moving average)  
- `LT_MA` (30-day long-term moving average)
- `DailyPrice_Percentage_Change`
- `Signal` (Trading indicator based on moving average crossover) 

Final features used for modeling:  
`['Open', 'High', 'Low', 'Volume', 'ST_MA', 'LT_MA', 'DailyPrice_Percentage_Change']`

---

## Machine Learning Modeling

### 1️. Linear Regression Model
| Metric | Score |
|--------|-------|
| **R²** | 0.99941 |
| **MSE** | 208.08 |
| **RMSE** | 14.42 |
| **MAE** | 10.39 |

📌 *Strong predictive power with minimal average error.* 

### 2️. Time Series (ARIMA)
Implemented ARIMA model for advanced financial forecasting based on time-dependent patterns (details included in notebook). 

> The model effectively captures long-term growth trends and cyclical movements.

---

## Key Business Insights

| Insight | Impact |
|--------|--------|
| TCS stock shows **long-term upward trajectory** | Promising long-term investment |
| **Volume peaks in April & October** | Trade execution optimization |
| **SMA crossover generates accurate buy/sell signals** | Supports automated trading |
| **Low correlation of dividends & stock splits with price** | Price largely driven by market forces |
| **Excellent model accuracy (99.9%)** | Reliable for forecasting strategies |

---

##  How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/Veer7733/Internship_Project-TCS_Stock_Data-Live-and-Latest
   ``` 
2. Navigate to the project folder:
   ```bash
   cd Internship_Project-TCS_Stock_Data-Live-and-Latest
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook TCS_Stock_Data.ipynb
   ```
