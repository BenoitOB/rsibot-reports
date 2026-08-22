# Trading Bots — weekly data (2026-08-15 → 2026-08-22)
_generated 2026-08-22 11:00 UTC_

- Balance **$10206.01** | NAV $9966.5 | open: [{'instrument': 'AUD_USD', 'units': '-142627'}, {'instrument': 'GBP_USD', 'units': '-76806'}]
- Week P&L: **$-10.42 (-0.1%)** (start $10216.43)
- Uptime (7d): **97.5%** | last beat 1.0 min ago
- API health (7d): **0 failed poll cycles** (0.0% of polls, falling vs prior week) — {'auth_401': 0, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 5.0% | 001 | AUD_USD, EUR_JPY, GBP_USD | 7 | 14.3 | 4.15 |
| session_breakout | yes | 5.0% | 004 | EUR_USD, GBP_JPY, USD_JPY, XAU_USD | 11 | 36.4 | 0.27 |
| weekend_gap | yes | 5.0% | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, NZD_USD, EUR_JPY | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion | 2 | 0.0 | 0.0 |
| EUR_JPY | rsi_reversion | 3 | 33.3 | 4.26 |
| EUR_USD | session_breakout | 5 | 20.0 | 0.17 |
| GBP_JPY | session_breakout | 3 | 0.0 | 0.0 |
| GBP_USD | rsi_reversion | 2 | 0.0 | 0.0 |
| NZD_USD | weekend_gap | 0 | None | None |
| USD_CAD | weekend_gap | 0 | None | None |
| USD_JPY | session_breakout | 3 | 100.0 | 99.9 |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $10206.01 | $-10.42 (-0.1%) | 2 |
| 004 | session_breakout | $10284.92 | $84.18 (0.83%) | 0 |
| 003 | weekend_gap | $10000.0 | $0.0 (0.0%) | 0 |

## GBP_USD forward-test (since 2026-08-07)
- trades 3 | win 33.3% | live PF 15.5 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 0}
