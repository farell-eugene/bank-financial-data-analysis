# Bank Financial Performance Analysis (Internship Project)

Time-series analysis of a rural bank's (*Bank Perkreditan Rakyat*, BPR) monthly financial reports. Built during a data analyst internship to track growth, liquidity, profitability and efficiency, and to compare the bank against the national BPR industry.

> **No data is included.** The bank's financial reports are confidential, so all notebook outputs were cleared. The repository contains only the analysis code.

## Analyses

| Area | Metrics / methods |
|---|---|
| **Growth** | Month-over-month and year-over-year growth of total assets, third-party funds (DPK: savings + time deposits), loans and equity |
| **Volatility & shocks** | Monthly returns, standard deviation, 12-month rolling volatility, shock detection (±2σ) |
| **Liquidity** | Asset-to-DPK ratio, liquidity gap, **Loan-to-Deposit Ratio (LDR)** and modified LDR |
| **Early warning** | Composite stress index with a threshold-based early-warning signal |
| **Profitability** | **Return on Assets (ROA)** from current-year profit |
| **Efficiency** | **BOPO** (operating expenses / operating income), yearly patterns 2020–2025 |
| **Interbank positions** | Interbank assets (ABA) and interbank liabilities (ABP) over time |
| **Benchmarking** | Market share and YoY growth vs. national BPR statistics from Bank Indonesia |
| **Output** | Merged monthly dataset exported for a Power BI dashboard |

## Workflow

1. Load the monthly financial report (Excel) and reshape the wide table (one column per month) into a tidy time series
2. Extract key line items (total assets, savings, deposits, loans, equity, profit, operating income and expenses)
3. Compute ratios and growth metrics; visualize trends with Matplotlib
4. Load Bank Indonesia BPR industry statistics and align them by year for benchmarking
5. Export the merged dataset for Power BI

## Repository structure

```
notebooks/bank_financial_analysis.ipynb   # analysis code (outputs cleared)
```

## Run

The notebook was written for Google Colab (`files.upload()`). To run it, provide your own monthly financial report in the same layout (a `Pos` column of line items plus one column per month) and Bank Indonesia's BPR statistics table.

```bash
pip install pandas matplotlib openpyxl jupyter
```

## Tech stack

Python · pandas · Matplotlib · Google Colab · Power BI
