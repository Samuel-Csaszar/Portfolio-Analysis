# Portfolio Diversification and Value at Risk: A Comparative Analysis

Monte Carlo simulation comparing the 10 day Value at Risk (VaR) and Conditional 
VaR of a sector diversified equity portfolio against a concentrated technology 
portfolio, both equally weighted across 11 large-cap stocks (2021–2026).

📄 **[Read the full report](Portfolio_Analysis.html)** · [PDF version](Portfolio_Analysis.pdf)

## Key Finding

The concentrated technology portfolio's simulated risk was consistently 
**~1.9–2x that of the diversified portfolio**, across both VaR and CVaR and 
both the 95% and 99% confidence levels, a gap driven primarily by average 
pairwise correlation among holdings (0.45 vs. 0.25).

## What's in this analysis

- **Correlation analysis** — pairwise correlation heatmaps and structure across sectors
- **Monte Carlo VaR/CVaR simulation** — 10,000 scenario simulation using historical mean/covariance
- **Model validation** — historical backtesting of breach rates and excess kurtosis diagnostics
- **10 stocks/6 sectors (diversified)** vs. **11 large cap tech stocks (concentrated)**

## Tools

R · tidyverse · tidyquant · ggplot2 · MASS · Quarto

## Repository contents

| File | Description |
|---|---|
| `Portfolio_Analysis.qmd` | Full source code and report (Quarto) |
| `Portfolio_Analysis.html` | Rendered report (HTML) |
| `Portfolio_Analysis.pdf` | Rendered report (PDF) |

## Running it yourself

This report pulls live data via `tidyquant::tq_get()` (Yahoo Finance). To 
reproduce:

```r
quarto::quarto_render("Portfolio_Analysis.qmd")
```

Requires: `tidyverse`, `tidyquant`, `ggplot2`, `patchwork`, `MASS`, `scales`, 
`knitr`, `kableExtra`, `e1071`, `zoo`
