# Multi-Asset Return Distribution Analysis

Exploratory analysis of daily return distributions across five assets — SPY, TLT, GLD, HYG, and USD/TRY — covering 2015 to 2024.

## Objective

Before building any strategy, a quant researcher asks: *what does the return distribution of this asset actually look like?* Most financial models assume normality. This project tests that assumption and examines what happens when it breaks down.

## Key Findings

- **TLT posted negative annualized returns** over the period, driven by rising yields as inflation expectations increased — a direct consequence of the inverse price-yield relationship in long-duration bonds.
- **USD/TRY showed extreme volatility** (annualized vol of ~49%) reflecting multiple Turkish lira crises, where the central bank kept rates artificially low against surging inflation.
- **HYG and SPY delivered the best risk-adjusted returns** (Sharpe ~0.83), with HYG behaving more like an equity instrument due to its unsecured credit exposure.
- **TLT and USD/TRY have severely non-normal distributions** — kurtosis of 434 and 1,066 respectively. A VaR model assuming normality would dramatically underestimate tail risk for both assets.
- **EWMA volatility reacts faster** to market shocks than a simple rolling window, and normalizes more quickly after a spike — making it a better tool for risk managers monitoring current market conditions.

## Contents

| File | Description |
|------|-------------|
| `Multi-Asset Return Analysis.ipynb` | Main analysis notebook |
| `asset_prices.csv` | Daily price data for 5 assets (2015–2024) |

## Tools

Python · pandas · NumPy · matplotlib · SciPy
