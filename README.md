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
- config_name: mstr_mnav_daily
  data_files: data/mstr_mnav_daily.csv
- config_name: bmnr_mnav_daily
  data_files: data/bmnr_mnav_daily.csv
- config_name: strc_dividend_rate_history
  data_files: data/strc_dividend_rate_history.csv
---

# SatoshiMacro Bitcoin Cycle Model and Altcoin Season Index

Daily Bitcoin and Ethereum cycle scores from the SatoshiMacro Model (a 48-signal, six-tier cycle confluence model, 0-100 scale), a monthly Altcoin Season Index, and daily mNAV for the corporate crypto treasuries Strategy (MSTR) and BitMine (BMNR) built from SEC filings. Updated daily by SatoshiMacro.

Source and live charts: [satoshimacro.com](https://satoshimacro.com/). Methodology: [SatoshiMacro Model](https://satoshimacro.com/tools/crypto/satoshimacro-model/).

Latest reading (2026-11-21): Bitcoin SMM **24.9** (Accumulation), Ethereum SMM **23.9** (Accumulation), Altcoin Season Index **44** (Lean BTC).

## Files

| File | Rows | Description |
|---|---|---|
| `data/smm_btc_daily.csv` | 5073 | Daily Bitcoin SMM score since 2013-01-01: calibrated score, raw composite, zone, and the six tier scores |
| `data/smm_eth_daily.csv` | 3976 | Daily Ethereum SMM score since 2016-01-01, same columns |
| `data/smm_btc_signals_latest.csv` | 48 | Latest percentile score (0-100) for each of the Bitcoin model's signals |
| `data/altcoin_season_index_monthly.csv` | 107 | Month-end Altcoin Season Index: share of the top 50 coins (point-in-time, stablecoins excluded) that beat Bitcoin over 90 days |
| `data/mstr_mnav_daily.csv` | 1579 | Daily mNAV of Strategy (MSTR) since 2020-08-11: market value divided by the value of its Bitcoin, with the Bitcoin held and the estimated share count behind each day |
| `data/bmnr_mnav_daily.csv` | 252 | Daily mNAV of BitMine (BMNR) since 2025-11-20: market value divided by Ether, Bitcoin and cash, plus an Ether-only multiple |
| `data/strc_dividend_rate_history.csv` | 9 | Every stated dividend rate of Strategy's STRC preferred share, with the date it applied from and the Form 8-K that announced it |
| `data/latest.json` | 1 | Latest readings with links to the live pages |

## Corporate treasury series

mNAV is a company's market value divided by the value of the crypto it holds. Holdings come from each company's weekly Form 8-K on SEC EDGAR. Share counts start from the cover of each 10-Q and 10-K; for Strategy, shares sold under its at-the-market programme (reported in the same weekly filings) are added between covers, and for BitMine the count is interpolated between covers and marked provisional after the latest one. Prices are daily closes and are not included in these files. Live charts and method: [MSTR mNAV](https://satoshimacro.com/tools/crypto/treasuries/mstr-mnav/), [BMNR mNAV](https://satoshimacro.com/tools/crypto/treasuries/bmnr-mnav/), [STRC dividend rate and yield](https://satoshimacro.com/tools/crypto/treasuries/strc-yield/).

Latest (2026-11-21): Strategy mNAV **0.6651** on 2026-11-20, BitMine mNAV **0.7892** on 2026-11-20, STRC stated rate **12%**.

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
