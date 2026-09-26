# Trade review — 2026-09-12 to 2026-09-19

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-02-04 .. 2026-09-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `5cd41c2d7795` · 6 closed (-4.41R) · 3 open

### #44 AUD_USD long · pullback · stop -1.00R

Opened Thu 10 Sep 13:02 UTC · closed Mon 14 Sep 09:16 · entry 0.71674 · stop 0.71246 · target 0.72959

Traded under params `43ae93644557` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.EXCLUDED_ENTRY_HOURS_UTC [21]→[21, 22]; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.ROLLOVER_LOCAL_HOUR None→17; bot.WEEKLY_REOPEN_HOUR_ET None→17

**Why we entered**

- **Pullback leg, long.** RSI crossed 35 (down) to 30.4 while price was 2.4 ATR above the EMA200 — buying the dip in an uptrend.
- Volatility: ATR at the 72nd percentile of its last 250 bars, expanding (×1.29 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.47R** at bar 7 (28h); worst **-1.27R** at bar 12 (48h), over 12 bar(s) held.

**Why we exited**

- **Stop loss** hit on bar 12 (48h), realised -1.00R.
- It was in profit first (best +0.47R at bar 7) before reversing into the stop.

**Expected?**

- Outcome: **stopped out after being in profit** — 8% of the 367 trades in 8.7 years end this way.
- Gave back 1.47R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 6 | -1.03R → **+0.40R** | -0.0228R  [-0.073, +0.027] | helps this trade, no measurable effect on the book |

### #45 USD_CAD short · pullback · stop -1.08R

Opened Fri 11 Sep 13:04 UTC · closed Mon 14 Sep 12:31 · entry 1.38611 · stop 1.39110 · target 1.37115

Traded under params `43ae93644557` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.EXCLUDED_ENTRY_HOURS_UTC [21]→[21, 22]; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.ROLLOVER_LOCAL_HOUR None→17; bot.WEEKLY_REOPEN_HOUR_ET None→17

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 67.9 while price was 1.6 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 54th percentile of its last 250 bars, not expanding (×1.04 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.03R** at bar 1 (4h); worst **-1.12R** at bar 6 (24h), over 6 bar(s) held.

**Why we exited**

- **Stop loss** hit on bar 6 (24h), realised -1.08R.

**Expected?**

- Outcome: **stopped out, never meaningfully in profit** — 11% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 4 | -1.04R → **-0.31R** | -0.0246R  [-0.088, +0.039] | helps this trade, no measurable effect on the book |

### #46 AUD_USD long · pullback · time -0.39R

Opened Mon 14 Sep 01:04 UTC · closed Wed 16 Sep 01:06 · entry 0.71459 · stop 0.70987 · target 0.72875

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, long.** RSI crossed 35 (down) to 33.7 while price was 1.0 ATR above the EMA200 — buying the dip in an uptrend.
- Volatility: ATR at the 86th percentile of its last 250 bars, expanding (×1.35 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 long trade(s) were already open on AUD_USD; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.23R** at bar 1 (4h); worst **-0.80R** at bar 4 (16h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.39R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 4 | -0.42R → **-0.01R** | -0.0246R  [-0.088, +0.039] | helps this trade, no measurable effect on the book |

### #50 AUD_USD long · pullback · time +0.07R

Opened Mon 14 Sep 09:16 UTC · closed Wed 16 Sep 09:08 · entry 0.71258 · stop 0.70747 · target 0.72792

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, long.** RSI crossed 35 (down) to 29.9 while price was 0.1 ATR above the EMA200 — buying the dip in an uptrend.
- Volatility: ATR at the 93rd percentile of its last 250 bars, expanding (×1.19 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 long trade(s) were already open on AUD_USD; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.45R** at bar 2 (8h); worst **-0.34R** at bar 2 (8h), over 12 bar(s) held.
- Volatility contracted ×0.74 during the trade.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised +0.07R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it near flat** — 11% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

No tested parameter change would have moved this trade by 0.25R or more.

### #52 USD_CAD short · fade · stop -1.01R

Opened Tue 15 Sep 13:02 UTC · closed Wed 16 Sep 18:26 · entry 1.39242 · stop 1.39721 · target 1.37805

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 72.8, 1.7 ATR from the EMA, against the trend.
- Counter-trend distance 1.7 ATR against a cap of 3.0 — passed with 1.3 ATR to spare.
- RSI depth 2.8 points past the threshold against a cap of 5.0 — passed with 2.2 to spare.
- Volatility: ATR at the 44th percentile of its last 250 bars, not expanding (×0.95 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.36R** at bar 1 (4h); worst **-1.48R** at bar 8 (32h), over 8 bar(s) held.

**Why we exited**

- **Stop loss** hit on bar 8 (32h), realised -1.01R.
- It was in profit first (best +0.36R at bar 1) before reversing into the stop.

**Expected?**

- Outcome: **stopped out after being in profit** — 8% of the 367 trades in 8.7 years end this way.
- Gave back 1.37R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 4 | -1.04R → **-0.14R** | -0.0246R  [-0.088, +0.039] | helps this trade, no measurable effect on the book |
| counter-trend cap (ATR) 3.0 → 1.0 | -1.04R → **+0.00R** (entry would have been blocked) | +0.0074R  [-0.122, +0.137] | helps this trade, no measurable effect on the book |
| RSI depth cap 5.0 → 2.0 | -1.04R → **+0.00R** (entry would have been blocked) | +0.0283R  [-0.095, +0.151] | helps this trade, no measurable effect on the book |

### #54 USD_CAD short · fade · stop -1.01R

Opened Wed 16 Sep 13:04 UTC · closed Wed 16 Sep 18:41 · entry 1.39396 · stop 1.39861 · target 1.38002

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 71.4, 2.2 ATR from the EMA, against the trend.
- Counter-trend distance 2.2 ATR against a cap of 3.0 — passed with 0.8 ATR to spare.
- RSI depth 1.4 points past the threshold against a cap of 5.0 — passed with 3.6 to spare.
- Volatility: ATR at the 38th percentile of its last 250 bars, not expanding (×0.93 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on USD_CAD; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.22R** at bar 1 (4h); worst **-1.19R** at bar 2 (8h), over 2 bar(s) held.

**Why we exited**

- **Stop loss** hit on bar 2 (8h), realised -1.01R.

**Expected?**

- Outcome: **stopped out, never meaningfully in profit** — 11% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| counter-trend cap (ATR) 3.0 → 2.0 | -1.04R → **+0.00R** (entry would have been blocked) | -0.0180R  [-0.140, +0.104] | helps this trade, no measurable effect on the book |

### #57 USD_JPY short · pullback · OPEN

Opened Fri 18 Sep 05:01 UTC · entry 157.132 · stop 158.430 · target 153.238

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 71.4 while price was 0.6 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 74th percentile of its last 250 bars, expanding (×1.24 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.48R** at bar 1 (4h); worst **-0.71R** at bar 2 (8h), over 4 bar(s) so far.
- Volatility **expanded ×1.26** during the trade — the market repriced rather than reverted.

**Why we exited**

- Still open after 4 of 12 bars; unrealised result not scored.

**Expected?**

- Open — judged when it closes.

### #58 GBP_JPY short · pullback · OPEN

Opened Fri 18 Sep 05:01 UTC · entry 210.096 · stop 211.586 · target 205.627

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.9 while price was 4.0 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 77th percentile of its last 250 bars, expanding (×1.28 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.53R** at bar 1 (4h); worst **-0.80R** at bar 2 (8h), over 4 bar(s) so far.
- Volatility **expanded ×1.27** during the trade — the market repriced rather than reverted.

**Why we exited**

- Still open after 4 of 12 bars; unrealised result not scored.

**Expected?**

- Open — judged when it closes.

### #59 GBP_JPY short · fade · OPEN

Opened Fri 18 Sep 09:02 UTC · entry 211.010 · stop 212.741 · target 205.816

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 72.2, 2.1 ATR from the EMA, with the trend.
- RSI depth 2.2 points past the threshold against a cap of 5.0 — passed with 2.8 to spare.
- Volatility: ATR at the 79th percentile of its last 250 bars, expanding (×1.50 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on GBP_JPY; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.81R** at bar 2 (8h); worst **-0.16R** at bar 1 (4h), over 3 bar(s) so far.

**Why we exited**

- Still open after 3 of 12 bars; unrealised result not scored.

**Expected?**

- Open — judged when it closes.

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| stopped out after being in profit | 2 | 8% |
| stopped out, never meaningfully in profit | 2 | 11% |
| 12-bar clock closed it at a loss | 1 | 6% |
| 12-bar clock closed it near flat | 1 | 11% |

**Unusual week:** 4 of 6 closed trades hit the stop against 19% expected — about a 1% chance under these rules. Worth understanding; on its own, not a reason to change a parameter (see the clusters below and SECTION B of the weekly review).
**One move, 2 positions:** #52, #54 (USD_CAD short) all closed between Wed 18:26 and 18:41 UTC for -2.02R combined — one market event, so read these together rather than as 2 independent outcomes.

## rsi_reversion_nogate — A/B CANDIDATE — volatility gate OFF

Account 101-001-39369941-003 · current params `28ae28835d3f` · 5 closed (-2.90R) · 3 open

### #47 AUD_USD long · pullback · time -0.39R

Opened Mon 14 Sep 01:04 UTC · closed Wed 16 Sep 01:06 · entry 0.71459 · stop 0.70987 · target 0.72875

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, long.** RSI crossed 35 (down) to 33.7 while price was 1.0 ATR above the EMA200 — buying the dip in an uptrend.
- Volatility: ATR at the 86th percentile of its last 250 bars, expanding (×1.35 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.23R** at bar 1 (4h); worst **-0.80R** at bar 4 (16h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.39R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 4 | -0.42R → **-0.01R** | -0.0246R  [-0.088, +0.039] | helps this trade, no measurable effect on the book |

### #48 EUR_USD long · fade · time -0.46R

Opened Mon 14 Sep 05:04 UTC · closed Wed 16 Sep 05:07 · entry 1.15657 · stop 1.15175 · target 1.17104

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Fade leg, long.** RSI crossed 30 to 29.4, 1.0 ATR from the EMA, against the trend.
- Counter-trend distance 1.0 ATR against a cap of 3.0 — passed with 2.0 ATR to spare.
- RSI depth 0.6 points past the threshold against a cap of 5.0 — passed with 4.4 to spare.
- Volatility: ATR at the 78th percentile of its last 250 bars, not expanding (×1.07 vs 10 bars earlier) — the gate WOULD have blocked this — it traded only because this arm runs with the gate OFF, so this is an INCREMENTAL A/B trade.

**What happened**

- Best point **+0.10R** at bar 1 (4h); worst **-0.88R** at bar 3 (12h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.46R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| volatility gate OFF → ON | -0.47R → **+0.00R** (the control's gate would have blocked it) | -0.0063R  [-0.118, +0.105] | helps this trade, no measurable effect on the book |

### #49 AUD_USD long · pullback · time -0.03R

Opened Mon 14 Sep 09:00 UTC · closed Wed 16 Sep 09:07 · entry 0.71310 · stop 0.70799 · target 0.72844

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, long.** RSI crossed 35 (down) to 29.9 while price was 0.1 ATR above the EMA200 — buying the dip in an uptrend.
- Volatility: ATR at the 93rd percentile of its last 250 bars, expanding (×1.19 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 long trade(s) were already open on AUD_USD; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.35R** at bar 2 (8h); worst **-0.44R** at bar 2 (8h), over 12 bar(s) held.
- Volatility contracted ×0.74 during the trade.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.03R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it near flat** — 11% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

No tested parameter change would have moved this trade by 0.25R or more.

### #51 USD_CAD short · fade · stop -1.01R

Opened Tue 15 Sep 13:02 UTC · closed Wed 16 Sep 18:31 · entry 1.39247 · stop 1.39731 · target 1.37815

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 72.8, 1.7 ATR from the EMA, against the trend.
- Counter-trend distance 1.7 ATR against a cap of 3.0 — passed with 1.3 ATR to spare.
- RSI depth 2.8 points past the threshold against a cap of 5.0 — passed with 2.2 to spare.
- Volatility: ATR at the 44th percentile of its last 250 bars, not expanding (×0.95 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.37R** at bar 1 (4h); worst **-1.45R** at bar 8 (32h), over 8 bar(s) held.

**Why we exited**

- **Stop loss** hit on bar 8 (32h), realised -1.01R.
- It was in profit first (best +0.37R at bar 1) before reversing into the stop.

**Expected?**

- Outcome: **stopped out after being in profit** — 8% of the 367 trades in 8.7 years end this way.
- Gave back 1.38R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 4 | -1.04R → **-0.13R** | -0.0246R  [-0.088, +0.039] | helps this trade, no measurable effect on the book |
| counter-trend cap (ATR) 3.0 → 1.0 | -1.04R → **+0.00R** (entry would have been blocked) | +0.0074R  [-0.122, +0.137] | helps this trade, no measurable effect on the book |
| RSI depth cap 5.0 → 2.0 | -1.04R → **+0.00R** (entry would have been blocked) | +0.0283R  [-0.095, +0.151] | helps this trade, no measurable effect on the book |

### #53 USD_CAD short · fade · stop -1.01R

Opened Wed 16 Sep 13:03 UTC · closed Wed 16 Sep 18:41 · entry 1.39398 · stop 1.39863 · target 1.38004

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 71.4, 2.2 ATR from the EMA, against the trend.
- Counter-trend distance 2.2 ATR against a cap of 3.0 — passed with 0.8 ATR to spare.
- RSI depth 1.4 points past the threshold against a cap of 5.0 — passed with 3.6 to spare.
- Volatility: ATR at the 38th percentile of its last 250 bars, not expanding (×0.93 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on USD_CAD; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.22R** at bar 1 (4h); worst **-1.19R** at bar 2 (8h), over 2 bar(s) held.

**Why we exited**

- **Stop loss** hit on bar 2 (8h), realised -1.01R.

**Expected?**

- Outcome: **stopped out, never meaningfully in profit** — 11% of the 367 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| counter-trend cap (ATR) 3.0 → 2.0 | -1.04R → **+0.00R** (entry would have been blocked) | -0.0180R  [-0.140, +0.104] | helps this trade, no measurable effect on the book |

### #55 USD_JPY short · pullback · OPEN

Opened Fri 18 Sep 05:01 UTC · entry 157.132 · stop 158.430 · target 153.238

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 71.4 while price was 0.6 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 74th percentile of its last 250 bars, expanding (×1.24 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.48R** at bar 1 (4h); worst **-0.71R** at bar 2 (8h), over 4 bar(s) so far.
- Volatility **expanded ×1.26** during the trade — the market repriced rather than reverted.

**Why we exited**

- Still open after 4 of 12 bars; unrealised result not scored.

**Expected?**

- Open — judged when it closes.

### #56 GBP_JPY short · pullback · OPEN

Opened Fri 18 Sep 05:01 UTC · entry 210.096 · stop 211.586 · target 205.627

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.9 while price was 4.0 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 77th percentile of its last 250 bars, expanding (×1.28 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.53R** at bar 1 (4h); worst **-0.80R** at bar 2 (8h), over 4 bar(s) so far.
- Volatility **expanded ×1.27** during the trade — the market repriced rather than reverted.

**Why we exited**

- Still open after 4 of 12 bars; unrealised result not scored.

**Expected?**

- Open — judged when it closes.

### #60 GBP_JPY short · fade · OPEN

Opened Fri 18 Sep 09:02 UTC · entry 211.013 · stop 212.744 · target 205.819

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_REOPEN_HOUR_ET None→17; bot.WINDOW_END_INCLUSIVE None→False; risk.max_positions_per_pair 2→0

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 72.2, 2.1 ATR from the EMA, with the trend.
- RSI depth 2.2 points past the threshold against a cap of 5.0 — passed with 2.8 to spare.
- Volatility: ATR at the 79th percentile of its last 250 bars, expanding (×1.50 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on GBP_JPY; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.81R** at bar 2 (8h); worst **-0.16R** at bar 1 (4h), over 3 bar(s) so far.

**Why we exited**

- Still open after 3 of 12 bars; unrealised result not scored.

**Expected?**

- Open — judged when it closes.

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| 12-bar clock closed it at a loss | 2 | 6% |
| 12-bar clock closed it near flat | 1 | 11% |
| stopped out after being in profit | 1 | 8% |
| stopped out, never meaningfully in profit | 1 | 11% |

**One move, 2 positions:** #51, #53 (USD_CAD short) all closed between Wed 18:31 and 18:41 UTC for -2.03R combined — one market event, so read these together rather than as 2 independent outcomes.

## What the individual trades asked for

Each row is a change that would have improved at least one trade this week. The population column decides whether it deserves a proper test — a single week cannot.

| strategy | change | helped | hurt | net on this week's closed trades | 8.7-year verdict |
|---|---|---|---|---|---|
| rsi_reversion | counter-trend cap (ATR) → 1.0 | 2 (+2.08R) | 0 (+0.00R) | +2.08R | WITHIN NOISE |
| rsi_reversion | counter-trend cap (ATR) → 2.0 | 1 (+1.04R) | 0 (+0.00R) | +1.04R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 4 | 4 (+2.89R) | 0 (+0.00R) | +2.95R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 6 | 2 (+2.18R) | 0 (+0.00R) | +2.23R | WITHIN NOISE |
| rsi_reversion | RSI depth cap → 2.0 | 1 (+1.04R) | 0 (+0.00R) | +1.04R | WITHIN NOISE |
| rsi_reversion_nogate | counter-trend cap (ATR) → 1.0 | 2 (+2.08R) | 0 (+0.00R) | +2.08R | WITHIN NOISE |
| rsi_reversion_nogate | counter-trend cap (ATR) → 2.0 | 1 (+1.04R) | 0 (+0.00R) | +1.04R | WITHIN NOISE |
| rsi_reversion_nogate | hold (bars) → 4 | 2 (+1.32R) | 0 (+0.00R) | +1.50R | WITHIN NOISE |
| rsi_reversion_nogate | RSI depth cap → 2.0 | 1 (+1.04R) | 0 (+0.00R) | +1.04R | WITHIN NOISE |
| rsi_reversion_nogate | volatility gate → ON | 1 (+0.47R) | 0 (+0.00R) | +0.47R | WITHIN NOISE |

**Supported by the population:** none. Every change a trade asked for this week is within noise or harmful across 8.7 years — keep the current parameters.

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
