# Technical Analysis Strategy Backtest vs TD Nasdaq® Index Fund

## Table of Contents

- [Project Objective](#project-objective)  
- [Strategies Compared](#strategies-compared)  
- [Evaluation Metrics](#evaluation-metrics)  
- [Dataset](#dataset)  
- [Tools & Libraries](#tools--libraries)  
- [Sample Output](#sample-output)  
- [How to Run](#how-to-run)  
- [Conclusion](#conclusion)

---

## Project Objective

This project aims to compare various algorithmic trading strategies against the performance of the **TD Nasdaq® Index Fund (TDB908)**. The goal is to determine which strategies outperform the mutual fund based on key performance metrics.

---

## Strategies Compared

Nine technical analysis strategies were implemented and backtested:

1. **EMA + RSI + Stop Loss**  
2. **Bollinger Bands + Williams %R**  
3. **Williams %R Only**  
4. **Aroon Oscillator**  
5. **Candlestick Hammer + Trailing Stop Loss + Take Profit**  
6. **Ultimate Oscillator**  
7. **Connors RSI**  
8. **Parabolic SAR**  
9. **Commodity Channel Index (CCI) + Stop Loss**

Each strategy's trades are evaluated and compared against the TDB908 fund performance.

---

## Evaluation Metrics

For each trade, a summary table is created with:

- Ticker  
- Buy Date / Sell Date  
- Buy / Sell Price  
- % Return  

From these, the following metrics are computed:

- Win Rate  
- Average Return Per Trade  
- Average Annual Return  
- Strategy vs Fund Comparative Performance  

---

## Dataset

- **Historical Stock Data:** Retrieved using [Yahoo Finance](https://finance.yahoo.com) via `yfinance`  
- **Mutual Fund Data (TDB908):** Manually inserted from historical returns between 2015–2024

---

## Tools & Libraries

- Python 3.x  
- `pandas`  
- `numpy`  
- `yfinance`  
- `matplotlib`, `seaborn`  

---

## Sample Output

Sample output for each strategy includes a detailed trade log and summary performance metrics:

**Trade Log Example:**

| Ticker | Buy Date   | Sell Date  | Buy Price | Sell Price | Return (%) |
|--------|------------|------------|-----------|------------|-------------|
| AAPL   | 2020-03-10 | 2020-04-05 | 256.75    | 278.93     | 8.64%       |
| MSFT   | 2019-07-15 | 2019-08-12 | 137.92    | 145.30     | 5.35%       |

**Strategy Performance Summary:**

- **Total Transactions:** 665  
- **Cumulative Return:** 65.13%  
- **Average Return per Trade:** 2.6%  
- **Win Rate:** 61.2%  
- **Maximum Drawdown:** -14.5%  
- **Benchmark (TDB908) Return for Same Period:** 93.5%

Visualizations may include:
- Running sum of returns vs. benchmark  
- Annual number of transactions  
- Return distribution per strategy  
- Correlation matrix among selected stocks

---

## How to Run

1. Clone this repository or download the notebook file.  
2. Install dependencies:

```bash
pip install yfinance pandas numpy matplotlib seaborn

