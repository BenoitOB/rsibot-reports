# Trading Bots — weekly data (2026-08-08 → 2026-08-15)
_generated 2026-08-15 11:00 UTC_

- Balance **$10437.94** | NAV $10456.45 | open: [{'instrument': 'EUR_JPY', 'units': '-90280'}]
- Week P&L: **$78.46 (0.76%)** (start $10359.48)
- Uptime (7d): **99.9%** | last beat 0.0 min ago
- API health (7d): **4 failed poll cycles** (0.2% of polls, rising vs prior week) — {'auth_401': 4, 'network': 0, 'other': 0}

## Strategies running (both share this account)
| strategy | running | risk/trade | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|
| rsi_reversion | yes | 10.0% | AUD_USD, EUR_JPY, GBP_USD | 1 | 100.0 | 99.9 |
| session_breakout | yes | 1.0% | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 10 | 20.0 | 0.01 |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion | 0 | None | None |
| EUR_GBP | session_breakout | 4 | 0.0 | 0.0 |
| EUR_JPY | rsi_reversion | 0 | None | None |
| EUR_USD | session_breakout | 4 | 50.0 | 1.86 |
| GBP_JPY | session_breakout | 2 | 0.0 | 0.0 |
| GBP_USD | rsi_reversion | 1 | 100.0 | 99.9 |
| USD_JPY | session_breakout | 0 | None | None |
| XAU_USD | session_breakout | 0 | None | None |

## GBP_USD forward-test (since 2026-08-07)
- trades 1 | win 100.0% | live PF 99.9 vs backtest 1.46 | insufficient sample

## Volatility gate (Filter C) — performance of the SKIPPED trades
_gate is working if the skipped set has PF < 1.0 (it removed losers)_
- {"n": 0}
