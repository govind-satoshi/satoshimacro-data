---
license: cc-by-4.0
pretty_name: SatoshiMacro Bitcoin Cycle Model and Altcoin Season Index
language:
- en
tags:
- bitcoin
- ethereum
- crypto
- finance
- time-series
- market-cycles
size_categories:
- 1K<n<10K
configs:
- config_name: smm_btc_daily
  data_files: data/smm_btc_daily.csv
- config_name: smm_eth_daily
  data_files: data/smm_eth_daily.csv
- config_name: altcoin_season_index_monthly
  data_files: data/altcoin_season_index_monthly.csv
- config_name: smm_btc_signals_latest
  data_files: data/smm_btc_signals_latest.csv
---

# SatoshiMacro Bitcoin Cycle Model and Altcoin Season Index

Daily Bitcoin and Ethereum cycle scores from the SatoshiMacro Model (a 48-signal, six-tier cycle confluence model, 0-100 scale), plus a monthly Altcoin Season Index. Updated daily by SatoshiMacro.

Source and live charts: [satoshimacro.com](https://satoshimacro.com/). Methodology: [SatoshiMacro Model](https://satoshimacro.com/tools/crypto/satoshimacro-model/).

Latest reading (2026-10-06): Bitcoin SMM **42.1** (Neutral), Ethereum SMM **43.9** (Neutral), Altcoin Season Index **72** (Lean alt).

## Files

| File | Rows | Description |
|---|---|---|
| `data/smm_btc_daily.csv` | 5027 | Daily Bitcoin SMM score since 2013-01-01: calibrated score, raw composite, zone, and the six tier scores |
| `data/smm_eth_daily.csv` | 3930 | Daily Ethereum SMM score since 2016-01-01, same columns |
| `data/smm_btc_signals_latest.csv` | 48 | Latest percentile score (0-100) for each of the Bitcoin model's signals |
| `data/altcoin_season_index_monthly.csv` | 106 | Month-end Altcoin Season Index: share of the top 50 coins (point-in-time, stablecoins excluded) that beat Bitcoin over 90 days |
| `data/latest.json` | 1 | Latest readings with links to the live pages |

## Zones

| SMM | Zone |
|---|---|
| 0-15 | Deep Value |
| 15-30 | Accumulation |
| 30-50 | Neutral |
| 50-70 | Caution |
| 70-85 | Distribution |
| 85-100 | Cycle Top |

Tier weights (Bitcoin): cycle timing and mass psychology 30%, valuation 25%, sentiment 20%, rotation 10%, miner 10%, macro 5%. Each signal is an expanding-window percentile rank, so historical readings use only data available at the time.

## Licence and attribution

CC BY 4.0. Free to use, including commercially, with credit. Please attribute as:

> Data: SatoshiMacro (https://satoshimacro.com)

and link to the source page where practical. Not financial advice.

## Citation

See `CITATION.cff`. Quarterly snapshots are archived on Zenodo with a DOI.
