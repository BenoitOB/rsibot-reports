# Trading Bots — weekly data (2026-11-07 → 2026-11-14)
_generated 2026-11-14 11:00 UTC_

- Balance **$10957.05** | NAV $10957.05 | open: flat
- Week P&L: **$621.87 (6.02%)** (start $10335.18)
- Uptime (7d): **99.6%** | last beat 1.0 min ago
- API health (7d): **18 failed poll cycles** (0.89% of polls, falling vs prior week) — {'auth_401': 18, 'network': 0, 'other': 0}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 1 | 100.0 | 99.9 |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | no | - | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, NZD_USD, EUR_JPY | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion | 1 | 100.0 | 99.9 |
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
| 001 | rsi_reversion | $10957.05 | $621.87 (6.02%) | 0 |
| 003 | rsi_reversion_nogate | $9343.09 | $0.0 (0.0%) | 0 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |

## GBP_USD forward-test (since 2026-08-07)
- trades 7 | win 57.1% | live PF 2.93 vs backtest 1.46 | insufficient sample

## Entry filters — what each one BLOCKED, scored separately
_A blocked set that looks profitable is not a verdict: blocks arrive a few per week, so a month is ~30 trades against a per-trade sd of ~0.9R. No filter gets a verdict below the n printed in its row._

| filter | blocked (n) | exp/trade | 95% interval | PF | rate | status |
|---|---|---|---|---|---|---|
| counter_trend | 70 | -0.086R | [-0.260, +0.088] | 0.75 | 6.0/wk | ACCUMULATING — 70/139 needed to resolve 0.15R; this number carries no decision yet |
| vol_gate_high_not_expanding | 11 | -0.324R | [-0.815, +0.167] | 0.43 | 0.9/wk | ACCUMULATING — 11/139 needed to resolve 0.15R; this number carries no decision yet |
| rsi_too_deep | 2 | -0.717R | — | 0.0 | 0.2/wk | ACCUMULATING — 2/139 needed to resolve 0.15R; this number carries no decision yet |

_Needs n≥139 per filter to resolve a 0.15R difference. The 8.7-year population test is the authority on where each cap belongs; this is a live cross-check, not a second opinion._
