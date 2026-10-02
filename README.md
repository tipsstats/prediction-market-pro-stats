---
license: cc-by-4.0
language:
- en
pretty_name: Prediction Market Pro Stats (Sports)
tags:
- sports
- football
- basketball
- prediction-markets
- probability
- calibration
size_categories:
- n<1K
configs:
- config_name: top_pros_by_competition
  data_files: top_pros_by_competition.csv
- config_name: market_favourite_calibration
  data_files: market_favourite_calibration.csv
- config_name: overview
  data_files: overview.csv
---

# Prediction Market Pro Stats (Sports)

Weekly aggregate statistics on sports prediction markets, compiled by [SG Tips (sg.tips)](https://sg.tips/) from public trades and positions on Polymarket, Kalshi and SX.

Latest snapshot: **2026-w40** (data as of 2026-10-02T16:41:43Z).

## Key numbers

- Public prediction-market accounts analysed: **791,417**
- Accounts that pass our long-term profitability screens: **11,733** (only **1.5%**)
- Combined cumulative P&L of those accounts: **$127.7M**
- The market favourite won **54.7%** of 5,370 finished matches in the last 30 days

## Files

| File | What it contains |
|---|---|
| `top_pros_by_competition.csv` | For each competition (and each sport overall): the 10 profitable pros with the highest hit rate over the last 30 days, with settled predictions, correct calls and hit rate, as shown on [sg.tips/top-pros](https://sg.tips/top-pros). One row per pro. |
| `market_favourite_calibration.csv` | As shown on [sg.tips/markets](https://sg.tips/markets): how often the prediction-market favourite actually won, by the favourite's probability band (<50%, 50–60%, 60–75%, ≥75%) and by sport, for the last 7 and 30 days. |
| `overview.csv` | Platform-wide figures shown on [sg.tips/reports](https://sg.tips/reports) and the site's data pages (accounts analysed, profitable pros, predictions tracked, matches covered). |

## Definitions

- **Profitable pro**: a public prediction-market account that passes Tips' proprietary screening for long-term profitability.
- **Hit rate**: correct ÷ settled predictions.
- **Market favourite**: the side with the highest prediction-market price before kick-off.
- **Privacy**: only public display names shown on the site are included. Accounts whose display name is a wallet address are shown as `anonymous wallet`; a few display names are withheld. No wallet addresses and no per-person position details are published.

## Update frequency

Updated weekly (Monday, UTC), together with the [weekly data reports](https://sg.tips/reports). Historical snapshots are kept in the repository history.

## Live versions

- Match probabilities and pro positions for upcoming matches: <https://sg.tips/markets>
- Most accurate pros by competition: <https://sg.tips/top-pros>
- Weekly reports (pros vs. the market, favourite hit rate, profitable share): <https://sg.tips/reports>
- Free embeddable widgets: <https://sg.tips/widgets>

## Citation

Please credit the source when you use or quote this data: **"Source: SG Tips (sg.tips)"** with a link to <https://sg.tips/reports>.

```
@misc{sgtips_prediction_market_pro_stats,
  title  = {Prediction Market Pro Stats (Sports)},
  author = {SG Tips},
  year   = {2026},
  url    = {https://sg.tips/reports}
}
```

## Limitations

Past data is for reference only and does not indicate future results. Data covers only public on-platform activity. SG Tips displays data only and offers no trading services.
