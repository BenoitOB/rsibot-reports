# Trading Bots — weekly data (2026-10-17 → 2026-10-24)
_generated 2026-10-24 11:00 UTC_

- Balance **$9851.9** | NAV $9851.9 | open: flat
- Week P&L: **$-54.68 (-0.55%)** (start $9906.59)
- Uptime (7d): **100.0%** | last beat 4.0 min ago
- API health (7d): **2 failed poll cycles** (0.1% of polls, falling vs prior week) — {'auth_401': 2, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 6 | 50.0 | 0.7 |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | no | - | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, NZD_USD, EUR_JPY | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion | 1 | 100.0 | 99.9 |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion, weekend_gap | 0 | None | None |
| GBP_JPY | rsi_reversion | 0 | None | None |
| GBP_USD | rsi_reversion | 1 | 100.0 | 99.9 |
| NZD_USD | rsi_reversion | 4 | 25.0 | 0.18 |
| USD_CAD | rsi_reversion, weekend_gap | 0 | None | None |
| USD_JPY | rsi_reversion | 0 | None | None |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $9851.9 | $-54.68 (-0.55%) | 0 |
| 003 | rsi_reversion_nogate | $9343.09 | $0.0 (0.0%) | 0 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |

## GBP_USD forward-test (since 2026-08-07)
- trades 6 | win 50.0% | live PF 1.49 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 64, "logged": 71, "win_pct": 46.9, "pf": 0.48, "expectancy_R": -0.211, "verdict": "GATE EARNING ITS KEEP (skipped set is a loser)"}
