# Trading Bots — weekly data (2026-09-12 → 2026-09-19)
_generated 2026-09-19 20:24 UTC_

- Balance **$9276.14** | NAV $9381.23 | open: [{'instrument': 'GBP_JPY', 'units': '-36484'}, {'instrument': 'USD_JPY', 'units': '-22458'}]
- Week P&L: **$-868.99 (-8.57%)** (start $10145.13)
- Uptime (7d): **100.0%** | last beat 2.0 min ago
- API health (7d): **2 failed poll cycles** (0.1% of polls, falling vs prior week) — {'auth_401': 2, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 6 | 16.7 | 0.02 |
| rsi_reversion_nogate | yes | 2.0% | 003 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 5 | 0.0 | 0.0 |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | no | - | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, NZD_USD, EUR_JPY | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion, rsi_reversion_nogate | 5 | 20.0 | 0.04 |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion_nogate | 1 | 0.0 | 0.0 |
| GBP_JPY | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| GBP_USD | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| NZD_USD | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| USD_CAD | rsi_reversion, rsi_reversion_nogate | 5 | 0.0 | 0.0 |
| USD_JPY | rsi_reversion, rsi_reversion_nogate | 0 | None | None |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $9276.14 | $-868.99 (-8.57%) | 2 |
| 003 ⚠ SHARED | rsi_reversion_nogate, weekend_gap | $9209.0 | $-576.26 (-5.89%) | 2 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |

_⚠ a SHARED account's week P&L cannot be attributed to one strategy, and each strategy's risk limits are affected by the other's losses._

## GBP_USD forward-test (since 2026-08-07)
- trades 5 | win 40.0% | live PF 1.34 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 9, "logged": 26, "win_pct": 77.8, "pf": 5.52, "expectancy_R": 0.382, "verdict": "GATE IS COSTING US (skipped set is profitable) \u2014 revisit"}
