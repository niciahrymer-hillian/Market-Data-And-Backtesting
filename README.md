# Market-Data-And-Backtesting

### Market data pipelines and honest backtesting: OHLCV handling, survivorship bias, look-ahead bias, and why most backtests lie.

![Chain S](https://img.shields.io/badge/Chain%20S-0F766E?style=for-the-badge) [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge)](LICENSE-GPL) [![License: AGPL v3](https://img.shields.io/badge/License-AGPLv3-blue?style=for-the-badge)](LICENSE-AGPL)

[📖 Lesson Plan](docs/LESSON_PLAN.md)

<!-- SCREENSHOT PLACEHOLDER: docs/screenshots/overview.png -->

> ⬜ **Scaffold pending.** Directory created to portfolio standard; full content (README, lesson plan, tour + quiz, skeleton code) still to be built. Part of **Chain S — FinTech Engineering**.

## Why This Was Built

Backtesting is a fantastic lesson in fooling yourself. It is trivially easy to build a strategy that returns
400% on historical data and loses money immediately in production, and the reasons are specific and
learnable: look-ahead bias (using information you wouldn't have had yet), survivorship bias (testing only
on companies that still exist), and overfitting to noise.

I'm interested in this less as a trading ambition and more as a discipline. A backtest is a simulation of a
decision process, and the rigor it demands — strict point-in-time data, out-of-sample validation, honest
transaction costs — is the same rigor that keeps any predictive system honest.

## Why This Matters (Industry Application)

Quant and market-data engineering roles pay extremely well, and the core skills — time-series pipelines,
point-in-time correctness, rigorous validation — transfer to any forecasting work. More broadly, the
mindset of "how is this result deceiving me?" is the single most valuable habit in data science.

## Topics Covered

| Area | What this project covers |
|------|--------------------------|
| Market data | OHLCV bars, adjustments, corporate actions, and data quality |
| Point-in-time | Only using what was actually knowable at each moment |
| Look-ahead bias | The subtle ways future information leaks into a backtest |
| Survivorship bias | Testing on the winners that happened to survive |
| Costs | Slippage, commissions, and why they erase most paper edges |
| Validation | Out-of-sample testing and walk-forward analysis |

## How This Connects

Chain S (FinTech Engineering). Uses time-series handling from **Chain D** and the validation discipline from **Model-Evaluation-And-Experimentation**.

---
Dual licensed — [GPL v3](LICENSE-GPL) and [AGPL v3](LICENSE-AGPL).
