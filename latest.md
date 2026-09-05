# Trading Bots — weekly data (2026-08-29 → 2026-09-05)
_generated 2026-09-05 11:00 UTC_

- Balance **$10150.01** | NAV $10150.01 | open: flat
- Week P&L: **$-270.58 (-2.6%)** (start $10420.59)
- Uptime (7d): **98.9%** | last beat 2.0 min ago
- API health (7d): **0 failed poll cycles** (0.0% of polls, flat vs prior week) — {'auth_401': 0, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 8 | 0.0 | 0.0 |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | yes | 2.0% | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, EUR_JPY, USD_JPY, EUR_GBP | 1 | 0.0 | 0.0 |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_GBP | weekend_gap | 0 | None | None |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion | 2 | 0.0 | 0.0 |
| GBP_JPY | rsi_reversion | 0 | None | None |
| GBP_USD | rsi_reversion | 2 | 0.0 | 0.0 |
| NZD_USD | rsi_reversion | 2 | 0.0 | 0.0 |
| USD_CAD | rsi_reversion, weekend_gap | 2 | 0.0 | 0.0 |
| USD_JPY | rsi_reversion | 1 | 0.0 | 0.0 |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $10150.01 | $-270.58 (-2.6%) | 0 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |
| 003 | weekend_gap | $9785.26 | $-200.63 (-2.01%) | 0 |

## GBP_USD forward-test (since 2026-08-07)
- trades 5 | win 40.0% | live PF 1.34 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 3, "logged": 4, "win_pct": 100.0, "pf": 99.9, "expectancy_R": 1.104, "verdict": "GATE IS COSTING US (skipped set is profitable) \u2014 revisit"}
