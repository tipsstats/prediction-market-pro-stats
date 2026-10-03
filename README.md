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

Weekly aggregate statistics on sports prediction markets, compiled by [SG Tips (sg.tips)](https://sg.tips/) from public data on Polymarket, Kalshi and SX.

Latest snapshot: 2026-w40 (data as of 2026-10-02T16:41:43Z).

## Files

### `top_pros_by_competition.csv`

For each competition (and each sport overall), the 10 listed pros with the highest hit rate over the last 30 days. One row per pro. Same data as [sg.tips/top-pros](https://sg.tips/top-pros).

| Field | Description |
|---|---|
| `as_of_utc` | Snapshot time (UTC) |
| `window_days` | Look-back window in days |
| `competition` | Competition name; `ALL <sport>` rows rank across the whole sport |
| `sport` | Sport |
| `ranked_pros` | Number of listed pros with settled predictions in this competition |
| `rank` | Rank by hit rate within the competition |
| `pro_display_name` | Public display name |
| `platform` | Polymarket, Kalshi or SX |
| `settled_predictions` | Settled predictions in the window |
| `correct` | Correct predictions in the window |
| `hit_rate_pct` | `correct / settled_predictions`, in percent |
| `profile_url` | Profile page on sg.tips |

### `market_favourite_calibration.csv`

How often the prediction-market favourite won, by probability band and by sport, for the last 7 and 30 days. Same data as [sg.tips/markets](https://sg.tips/markets).

| Field | Description |
|---|---|
| `as_of_utc` | Snapshot time (UTC) |
| `window` | `7d` or `30d` |
| `from_date`, `to_date` | Window boundaries |
| `group_type` | `all`, `favourite_probability_band_pct` or `sport` |
| `group` | Group value (band: `<50`, `50-60`, `60-75`, `75+`; or sport name) |
| `finished_matches` | Finished matches in the group |
| `favourite_won` | Matches won by the favourite |
| `favourite_win_rate_pct` | `favourite_won / finished_matches`, in percent |

### `overview.csv`

Platform-wide counts shown on [sg.tips/reports](https://sg.tips/reports), one row per metric (`as_of_utc`, `metric`, `value`).

## Definitions

- **Listed pro**: a public prediction-market account that passes Tips' proprietary multi-dimensional screening.
- **Hit rate**: correct ÷ settled predictions.
- **Market favourite**: the side with the highest prediction-market price before the match starts.
- **Privacy**: only public display names shown on the site are included. Display names that are wallet addresses appear as `anonymous wallet`; some display names are withheld. No wallet addresses or per-person position details are included.

## Source

Public data from Polymarket, Kalshi and SX, as collected and displayed on [sg.tips](https://sg.tips/).

## Update frequency

Weekly (Monday, UTC). Earlier snapshots are available in the repository history.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Attribution: "Source: SG Tips (sg.tips)" with a link to <https://sg.tips/reports>.

```
@misc{sgtips_prediction_market_pro_stats,
  title  = {Prediction Market Pro Stats (Sports)},
  author = {SG Tips},
  year   = {2026},
  url    = {https://sg.tips/reports}
}
```

## Limitations

Covers public on-platform activity only. Past data does not indicate future results. SG Tips displays data only and offers no trading services.
