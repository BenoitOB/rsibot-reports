# Trading Bots — weekly data (2026-11-14 → 2026-11-21)
_generated 2026-11-21 11:00 UTC_

- Balance **$10644.73** | NAV $10644.73 | open: flat
- Week P&L: **$-312.32 (-2.85%)** (start $10957.05)
- Uptime (7d): **96.6%** | last beat 4.0 min ago
- API health (7d): **117 failed poll cycles** (5.8% of polls, rising vs prior week) — {'auth_401': 60, 'network': 0, 'other': 57}

## Strategies running (note: weekend_gap uses its OWN sub-account)
| strategy | running | risk/trade | account | pairs | trades | win% | PF |
|---|---|---|---|---|---|---|---|
| rsi_reversion | yes | 2.0% | 001 | AUD_USD, GBP_USD, EUR_USD, NZD_USD, USD_JPY, USD_CAD, GBP_JPY | 2 | 0.0 | 0.0 |
| session_breakout | no | - | 004 | EUR_USD, EUR_GBP, GBP_JPY, USD_JPY, XAU_USD | 0 | None | None |
| weekend_gap | no | - | 003 | EUR_USD, GBP_USD, AUD_USD, USD_CAD, NZD_USD, EUR_JPY | 0 | None | None |

## Trades this week (per pair)
_(authoritative week total P&L is the balance delta above; per-trade journal pnl is unreliable for JPY pairs, so only counts/PF shown)_
| pair | strategy | trades | win% | PF |
|---|---|---|---|---|
| AUD_USD | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_JPY | rsi_reversion, weekend_gap | 0 | None | None |
| EUR_USD | rsi_reversion, weekend_gap | 0 | None | None |
| GBP_JPY | rsi_reversion | 1 | 0.0 | 0.0 |
| GBP_USD | rsi_reversion, weekend_gap | 0 | None | None |
| NZD_USD | rsi_reversion, weekend_gap | 0 | None | None |
| USD_CAD | rsi_reversion, weekend_gap | 0 | None | None |
| USD_JPY | rsi_reversion | 1 | 0.0 | 0.0 |

## Execution quality (weekend_gap forward test)
_the point of running this live: positive slippage = ADVERSE. Total cost = spread + slippage, vs the 4-9 pips assumed in the walk-forward._
- no data yet

## Accounts (balance delta is the reliable per-strategy P&L)
| account | strategies | balance | week P&L | open |
|---|---|---|---|---|
| 001 | rsi_reversion | $10644.73 | $-312.32 (-2.85%) | 0 |
| 003 | rsi_reversion_nogate | $9343.09 | $0.0 (0.0%) | 0 |
| 004 | session_breakout | $10284.92 | $0.0 (0.0%) | 0 |

## GBP_USD forward-test (since 2026-08-07)
- trades 7 | win 57.1% | live PF 2.93 vs backtest 1.46 | insufficient sample

## Entry filters — what each one BLOCKED, scored separately
_A blocked set that looks profitable is not a verdict: blocks arrive a few per week, so a month is ~30 trades against a per-trade sd of ~0.9R. No filter gets a verdict below the n printed in its row._

| filter | blocked (n) | exp/trade | 95% interval | PF | rate | status |
|---|---|---|---|---|---|---|
| counter_trend | 82 | -0.149R | [-0.306, +0.007] | 0.61 | 6.5/wk | ACCUMULATING — 82/139 needed to resolve 0.15R; this number carries no decision yet |
| vol_gate_high_not_expanding | 12 | -0.356R | [-0.810, +0.098] | 0.39 | 1.0/wk | ACCUMULATING — 12/139 needed to resolve 0.15R; this number carries no decision yet |
| rsi_too_deep | 2 | -0.717R | — | 0.0 | 0.2/wk | ACCUMULATING — 2/139 needed to resolve 0.15R; this number carries no decision yet |

_Needs n≥139 per filter to resolve a 0.15R difference. The 8.7-year population test is the authority on where each cap belongs; this is a live cross-check, not a second opinion._
