# AAPL Stock Price Analysis (2004 – 2024, 20-Year Window)

Financial dataset analysis assignment: descriptive statistics, time-series analysis, and
visualisation of Apple Inc. (AAPL) daily stock prices over a 20-year period.

## Business Objective
Evaluate AAPL's long-term price trend, return, and volatility characteristics over a
20-year window to inform a buy-and-hold vs. active-trading decision, and quantify risk.

## Contents
- `apple_stock_20y.csv` — raw source data (OHLCV, Yahoo Finance via public GitHub dataset)
- `apple_stock_clean_20y.csv` — cleaned, structured data with engineered fields (returns, moving averages, volatility)
- `AAPL_Financial_Analysis_20y.ipynb` — full Jupyter notebook: data acquisition, integrity checks, descriptive stats, time-series analysis, and 3 charts
- `AAPL_Financial_Analysis_Report_20y.docx` — written report covering all assignment sections
- `chart1_price_trend.png`, `chart2_returns_distribution.png`, `chart3_volume.png` — exported charts

## Key Findings
- Period return: +22,920.84% (Close $1.03 → $237.33), CAGR ~31.25%/year
- Annualised volatility: ~32.2%
- 5,036 trading days (2004-11-29 to 2024-11-29), zero missing values / duplicates / invalid prices
- Log-scale price chart shows long-run exponential growth, with sharp drawdowns during the 2008 financial crisis and 2020 COVID crash, each followed by recovery to new highs

## Reproduce
```bash
pip install pandas numpy matplotlib jupyter
jupyter nbconvert --to notebook --execute AAPL_Financial_Analysis_20y.ipynb
```

## Data Source
Daily AAPL OHLCV data, originally from Yahoo Finance, redistributed in the public
[FarhanAli97/Apple-AAPL-Stock-Data-1980-to-December-2024](https://github.com/FarhanAli97/Apple-AAPL-Stock-Data-1980-to-December-2024)
GitHub repository, filtered to the most recent 20 years (2004-11-29 to 2024-11-29).
