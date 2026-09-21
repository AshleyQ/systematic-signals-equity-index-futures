# Systematic Signals Across Global Equity Index Futures

This project studies cross-sectional momentum, low-risk, and short-term reversal signals across 10 developed-country equity index futures using approximately 50 years of monthly returns.

The analysis was originally developed as a course project in Excel and rebuilt in Python to make the methodology easier to inspect, test, and extend.

## Methodology

Five signal specifications are evaluated:

- 12-month momentum
- 12-month momentum excluding the most recent month
- low total volatility
- low downside deviation
- one-month reversal

Signals are converted into dollar-neutral cross-sectional portfolios and scaled monthly to a 1% predicted annualized volatility target using rolling 36-month covariance estimates. The notebook also examines turnover, transaction-cost sensitivity, factor dependence, market exposure, and an illustrative three-signal portfolio.

## Results

Momentum produced the strongest standalone results in the sample. The skip-one-month specification achieved a Sharpe ratio of 0.28 with a mean-return t-statistic of approximately 2.0.

Short-term reversal generated positive gross returns but was substantially more sensitive to transaction costs because of its higher turnover. The total-volatility low-risk specification produced a negative result, while downside deviation produced a weak positive result.

An illustrative portfolio combining skip-one-month momentum, low downside deviation, and short-term reversal achieved a Sharpe ratio of 0.26 and a smaller historical drawdown than any of its three selected components.

## Data

The analysis uses course-provided monthly return data for 10 developed-country equity index futures. The underlying dataset is not redistributed in this repository.

To reproduce the notebook, place the return file at:

```text
Returns.xlsx
```

in the same directory as the notebook.

## Repository

- `systematic_signals.ipynb` — complete research workflow, methodology, results, and discussion
- `README.md` — project overview

## Notes

The notebook reports both positive and negative results and avoids selecting specifications solely because they perform well historically. The final combined portfolio is an illustrative in-sample construction rather than an independent out-of-sample test.
