# ASX Momentum Factor Scanner & Backtester

A systematic cross-sectional momentum strategy backtested on ASX 200 stocks.

## Strategy Overview
- **Signal:** 12-1 month price momentum (buy winners, short losers)
- **Universe:** 50 liquid ASX 200 stocks across all GICS sectors
- **Rebalancing:** Monthly
- **Transaction Costs:** 10 basis points per leg (realistic ASX assumption)
- **Benchmark:** ASX 200 via STW.AX ETF
- **Risk-Free Rate:** RBA cash rate (4.35%)

## Performance Results
| Metric | L/S Strategy | Long-only Q5 | ASX 200 |
|---|---|---|---|
| Ann. Return | -1.6% | 15.7% | 11.0% |
| Volatility | 18.6% | 17.8% | 13.1% |
| Sharpe Ratio | -0.31 | 0.59 | 0.47 |
| Max Drawdown | -44.8% | -24.8% | - |
| Monthly Hit Rate | 48.4% | - | - |

## Notes on Results
The long-only Q5 (high momentum) portfolio outperformed the ASX 200 benchmark
with a Sharpe of 0.59 vs 0.47, confirming momentum as a valid factor in Australian
equities. The long/short spread underperformed due to the small universe size (50 stocks)
limiting short-side diversification - a known limitation at this scale.

## Visualisations
![Backtest Results](asx_momentum_backtest.png)

## Tools & Libraries
- Python 3
- yfinance
- pandas / numpy
- matplotlib / seaborn
- quantstats
- scipy

## Files
- `Project_1_ASX_Momentum.ipynb` - Full Colab notebook
- `asx_momentum_backtest.png` - Performance dashboard

## Key Concepts Demonstrated
- Cross-sectional momentum factor construction
- Quintile portfolio formation and rebalancing
- Transaction cost modelling
- Sharpe ratio, drawdown, and hit rate analysis
- Long/short equity strategy backtesting
