# Trading Bots — weekly data (2026-08-22 → 2026-08-29)
_generated 2026-08-29 11:00 UTC_

- Balance **$10420.59** | NAV $10304.26 | open: [{'instrument': 'NZD_USD', 'units': '56718'}, {'instrument': 'USD_JPY', 'units': '-55879'}, {'instrument': 'GBP_USD', 'units': '42170'}, {'instrument': 'USD_CAD', 'units': '-62708'}, {'instrument': 'EUR_USD', 'units': '54050'}]
- Week P&L: **$214.58 (2.1%)** (start $10206.01)
- Uptime (7d): **98.8%** | last beat 0.0 min ago
- API health (7d): **0 failed poll cycles** (0.0% of polls, flat vs prior week) — {'auth_401': 0, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 2 | 100.0 | 99.9 |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | yes | 2.0% | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, EUR_JPY, USD_JPY, EUR_GBP | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion | 1 | 100.0 | 99.9 |
| EUR_GBP | weekend_gap | 0 | None | None |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion, weekend_gap | 0 | None | None |
| GBP_JPY | rsi_reversion | 0 | None | None |
| GBP_USD | rsi_reversion | 1 | 100.0 | 99.9 |
| NZD_USD | rsi_reversion, weekend_gap | 0 | None | None |
| USD_CAD | rsi_reversion, weekend_gap | 0 | None | None |
| USD_JPY | rsi_reversion, weekend_gap | 0 | None | None |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $10420.59 | $214.58 (2.1%) | 5 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |
| 003 | weekend_gap | $9985.89 | $-14.11 (-0.14%) | 1 |

## GBP_USD forward-test (since 2026-08-07)
- trades 3 | win 66.7% | live PF 1.82 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 0, "logged": 3}
