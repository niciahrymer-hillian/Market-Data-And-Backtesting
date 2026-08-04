# 📖 Lesson Plan — Market-Data-And-Backtesting

> **Chain S — FinTech Engineering** | Market data pipelines and honest backtesting: OHLCV handling, survivorship bias, look-ahead bias, and why most backtests lie.

## What This Project Is

Build a market-data pipeline and a backtester, then systematically dismantle your own results by hunting for the biases that make backtests lie.

## Learning Objectives

By the end I can:

1. Ingest and clean OHLCV data, handling splits and corporate actions.
2. Enforce **point-in-time** correctness so no future data leaks in.
3. Identify and eliminate **look-ahead bias**.
4. Correct for **survivorship bias** using a full historical universe.
5. Model transaction costs and slippage realistically.
6. Validate out-of-sample and with walk-forward analysis.

## Software You Will Use

- Python, pandas, NumPy.
- A market data source (yfinance or similar).
- vectorbt or a hand-rolled backtester.

## Build Order

1. Ingest price data; adjust for splits and dividends.
2. Implement a simple strategy and get a suspiciously good result.
3. Hunt for look-ahead bias; fix it and watch returns fall.
4. Add survivorship-free universe data; watch returns fall again.
5. Add realistic costs and slippage.
6. Run walk-forward validation and report the honest number.

## Common Mistakes to Avoid

- Using adjusted prices inconsistently across the backtest.
- Entering on the same bar's close that generated the signal.
- Testing only on companies that still exist today.
- Ignoring transaction costs, which erase most paper edges.
- Tuning parameters on the test set until the curve looks good.

## Check Your Understanding

The quiz covers look-ahead bias, survivorship bias, point-in-time data, and why walk-forward validation is stricter.

## Why This Matters (Industry Application)

Quant and market-data engineering roles pay extremely well, and the core skills — time-series pipelines,
point-in-time correctness, rigorous validation — transfer to any forecasting work. More broadly, the
mindset of "how is this result deceiving me?" is the single most valuable habit in data science.

## Reflection Questions

- Which bias was hardest to spot in your own backtest, and why did it hide?
- How does this discipline transfer to evaluating any predictive model?
