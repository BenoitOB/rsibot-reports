# Trading Bots — weekly data (2026-09-05 → 2026-09-12)
_generated 2026-09-12 11:00 UTC_

- Balance **$10145.13** | NAV $10099.81 | open: [{'instrument': 'AUD_USD', 'units': '47386'}, {'instrument': 'USD_CAD', 'units': '-56438'}]
- Week P&L: **$-4.88 (-0.05%)** (start $10150.01)
- Uptime (7d): **100.0%** | last beat 4.0 min ago
- API health (7d): **4 failed poll cycles** (0.2% of polls, falling vs prior week) — {'auth_401': 4, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 0 | None | None |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | no | - | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, NZD_USD, EUR_JPY | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion, weekend_gap | 0 | None | None |
| GBP_JPY | rsi_reversion | 0 | None | None |
| GBP_USD | rsi_reversion, weekend_gap | 0 | None | None |
| NZD_USD | rsi_reversion, weekend_gap | 0 | None | None |
| USD_CAD | rsi_reversion, weekend_gap | 0 | None | None |
| USD_JPY | rsi_reversion | 0 | None | None |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $10145.13 | $-4.88 (-0.05%) | 2 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |
| 003 | weekend_gap | $9785.26 | $0.0 (0.0%) | 0 |

## GBP_USD forward-test (since 2026-08-07)
- trades 5 | win 40.0% | live PF 1.34 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 4, "logged": 9, "win_pct": 100.0, "pf": 99.9, "expectancy_R": 0.85, "verdict": "GATE IS COSTING US (skipped set is profitable) \u2014 revisit"}
