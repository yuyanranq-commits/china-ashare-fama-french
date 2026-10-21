# Data

## `Monthly_PB_PS_PE_MV_R_TR.xlsx` (not included)

This is a monthly panel of China A-share stocks, Dec 2005 to Feb 2022, with 416,841 rows and 3,146 stocks. It came from
a commercial data vendor and is not redistributed here. To run the notebook, put a file with these columns in this
folder:

| Column | Description |
|---|---|
| `stock` | Ticker, e.g. `600000.SH` |
| `number` | Company short name |
| `date` | Last trading day of the month |
| `Trading_Volume` | Monthly trading value (CNY) |
| `return` | Monthly return, **percent** |
| `Turnover_Rate` | Monthly turnover rate, percent |
| `market_value` | Total market capitalization (CNY) |
| `PE`, `PB`, `PS` | Valuation ratios at month end |
| `next_month_return` | `return` of the following month, percent |

## `Rf_data.xlsx` (included)

The People's Bank of China one-year deposit benchmark rate in percent per year, one row per rate change
(`adjusted_date`, `Rf`). The notebook forward-fills it to each month end with `merge_asof` and divides it by 12.
