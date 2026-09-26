# Trading Bots — weekly data (2026-09-19 → 2026-09-26)
_generated 2026-09-26 11:00 UTC_

- Balance **$9415.28** | NAV $9415.28 | open: flat
- Week P&L: **$139.14 (1.5%)** (start $9276.14)
- Uptime (7d): **100.0%** | last beat 0.0 min ago
- API health (7d): **2 failed poll cycles** (0.1% of polls, flat vs prior week) — {'auth_401': 2, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 5 | 40.0 | 1.63 |
| rsi_reversion_nogate | yes | 2.0% | 003 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 5 | 40.0 | 1.62 |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | no | - | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, NZD_USD, EUR_JPY | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| GBP_JPY | rsi_reversion, rsi_reversion_nogate | 4 | 50.0 | 1.29 |
| GBP_USD | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| NZD_USD | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| USD_CAD | rsi_reversion, rsi_reversion_nogate | 0 | None | None |
| USD_JPY | rsi_reversion, rsi_reversion_nogate | 6 | 33.3 | 1.86 |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $9415.28 | $139.14 (1.5%) | 0 |
| 003 | rsi_reversion_nogate | $9343.09 | $134.09 (1.46%) | 0 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |

## GBP_USD forward-test (since 2026-08-07)
- trades 5 | win 40.0% | live PF 1.34 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 26, "logged": 42, "win_pct": 69.2, "pf": 1.76, "expectancy_R": 0.129, "verdict": "GATE IS COSTING US (skipped set is profitable) \u2014 revisit"}
