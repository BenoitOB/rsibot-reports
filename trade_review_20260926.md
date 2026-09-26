# Trade review — 2026-09-19 to 2026-09-26

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-02-04 .. 2026-09-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `3ad713814089` · 5 closed (+0.78R) · 0 open

### #57 USD_JPY short · pullback · time -0.27R

Opened Fri 18 Sep 05:01 UTC · closed Tue 22 Sep 05:07 · entry 157.132 · stop 158.430 · target 153.238

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_OPEN_HOUR_ET None→0; bot.WEEKLY_OPEN_WEEKDAY None→0; bot.WINDOW_END_INCLUSIVE None→True

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 71.4 while price was 0.6 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 74th percentile of its last 250 bars, expanding (×1.24 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.48R** at bar 1 (4h); worst **-0.71R** at bar 2 (8h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.27R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 469 trades in 8.7 years end this way.
- Gave back 0.76R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 4 | -0.27R → **+0.17R** | -0.0363R  [-0.093, +0.020] | helps this trade, no measurable effect on the book |

### #58 GBP_JPY short · pullback · time -0.49R

Opened Fri 18 Sep 05:01 UTC · closed Tue 22 Sep 05:07 · entry 210.096 · stop 211.586 · target 205.627

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_OPEN_HOUR_ET None→0; bot.WEEKLY_OPEN_WEEKDAY None→0; bot.WINDOW_END_INCLUSIVE None→True

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.9 while price was 4.0 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 77th percentile of its last 250 bars, expanding (×1.28 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.53R** at bar 1 (4h); worst **-0.80R** at bar 2 (8h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.49R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 469 trades in 8.7 years end this way.
- Gave back 1.03R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| target 3.0 → 0.5 | -0.49R → **+0.48R** | -0.0318R  [-0.079, +0.016] | helps this trade, no measurable effect on the book |
| hold (bars) 12 → 24 | -0.49R → **+0.66R** | -0.0203R  [-0.065, +0.024] | helps this trade, no measurable effect on the book |

### #59 GBP_JPY short · fade · time +0.62R

Opened Fri 18 Sep 09:02 UTC · closed Tue 22 Sep 09:07 · entry 211.010 · stop 212.741 · target 205.816

Traded under params `49c4958716b9` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_OPEN_HOUR_ET None→0; bot.WEEKLY_OPEN_WEEKDAY None→0; bot.WINDOW_END_INCLUSIVE None→True

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 72.2, 2.1 ATR from the EMA, with the trend.
- RSI depth 2.2 points past the threshold against a cap of 5.0 — passed with 2.8 to spare.
- Volatility: ATR at the 79th percentile of its last 250 bars, expanding (×1.50 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on GBP_JPY; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.86R** at bar 12 (48h); worst **-0.16R** at bar 1 (4h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised +0.62R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it in profit** — 20% of the 469 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| stop (×ATR) 2.5 → 1.5 | +0.60R → **+1.00R** | -0.0030R  [-0.132, +0.126] | helps this trade, no measurable effect on the book |

### #61 USD_JPY short · pullback · time -0.42R

Opened Mon 21 Sep 13:03 UTC · closed Wed 23 Sep 13:07 · entry 157.319 · stop 158.751 · target 153.021

Traded under params `3ad713814089` — **differs from current in:** bot.ENTRY_WINDOWS_ET.AUD_USD [[22, 6]]→((22, 6),); bot.ENTRY_WINDOWS_ET.EUR_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.GBP_JPY [[0, 9]]→((0, 9),); bot.ENTRY_WINDOWS_ET.GBP_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.NZD_USD [[22, 5]]→((22, 5),); bot.ENTRY_WINDOWS_ET.USD_CAD [[8, 17]]→((8, 17),)

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.1 while price was 0.1 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 75th percentile of its last 250 bars, expanding (×1.28 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on USD_JPY; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.
- Spread at entry 1.7 pips.

**What happened**

- Best point **+0.35R** at bar 6 (24h); worst **-0.47R** at bar 12 (48h), over 12 bar(s) held.
- Volatility contracted ×0.56 during the trade.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.42R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 469 trades in 8.7 years end this way.
- Gave back 0.77R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 6 | -0.41R → **-0.00R** | -0.0278R  [-0.072, +0.016] | helps this trade, no measurable effect on the book |

### #64 USD_JPY short · fade · friday +1.34R

Opened Thu 24 Sep 13:04 UTC · closed Fri 25 Sep 20:09 · entry 158.666 · stop 159.720 · target 155.505

Traded under params `3ad713814089` — **differs from current in:** bot.ENTRY_WINDOWS_ET.AUD_USD [[22, 6]]→((22, 6),); bot.ENTRY_WINDOWS_ET.EUR_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.GBP_JPY [[0, 9]]→((0, 9),); bot.ENTRY_WINDOWS_ET.GBP_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.NZD_USD [[22, 5]]→((22, 5),); bot.ENTRY_WINDOWS_ET.USD_CAD [[8, 17]]→((8, 17),)

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 70.8, 2.9 ATR from the EMA, against the trend.
- Counter-trend distance 2.9 ATR against a cap of 3.0 — passed with 0.1 ATR to spare.
- RSI depth 0.8 points past the threshold against a cap of 5.0 — passed with 4.2 to spare.
- Volatility: ATR at the 50th percentile of its last 250 bars, not expanding (×0.98 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.6 pips.

**What happened**

- Best point **+1.64R** at bar 7 (28h); worst **-0.35R** at bar 1 (4h), over 7 bar(s) held.

**Why we exited**

- **Friday 16:00 ET flatten** closed it after 7 bars, realised +1.34R — the weekly rule, not the 12-bar time stop, which it pre-empted.

**Expected?**

- Outcome: **closed by the Friday 16:00 ET flatten** — 43% of the 469 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| stop (×ATR) 2.5 → 1.5 | +1.28R → **+2.14R** | -0.0030R  [-0.132, +0.126] | helps this trade, no measurable effect on the book |

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| 12-bar clock closed it at a loss | 3 | 6% |
| 12-bar clock closed it in profit | 1 | 20% |
| closed by the Friday 16:00 ET flatten | 1 | 43% |

**One move, 2 positions:** #58, #59 (GBP_JPY short) all closed between Tue 05:07 and 09:07 UTC for +0.13R combined — one market event, so read these together rather than as 2 independent outcomes.

## rsi_reversion_nogate — A/B CANDIDATE — volatility gate OFF

Account 101-001-39369941-003 · current params `2cf53666b980` · 5 closed (+0.75R) · 0 open

### #55 USD_JPY short · pullback · time -0.26R

Opened Fri 18 Sep 05:01 UTC · closed Tue 22 Sep 05:08 · entry 157.132 · stop 158.430 · target 153.238

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_OPEN_HOUR_ET None→0; bot.WEEKLY_OPEN_WEEKDAY None→0; bot.WINDOW_END_INCLUSIVE None→True

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 71.4 while price was 0.6 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 74th percentile of its last 250 bars, expanding (×1.24 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.48R** at bar 1 (4h); worst **-0.71R** at bar 2 (8h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.26R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 469 trades in 8.7 years end this way.
- Gave back 0.75R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 4 | -0.27R → **+0.17R** | -0.0363R  [-0.093, +0.020] | helps this trade, no measurable effect on the book |

### #56 GBP_JPY short · pullback · time -0.48R

Opened Fri 18 Sep 05:01 UTC · closed Tue 22 Sep 05:08 · entry 210.096 · stop 211.586 · target 205.627

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_OPEN_HOUR_ET None→0; bot.WEEKLY_OPEN_WEEKDAY None→0; bot.WINDOW_END_INCLUSIVE None→True

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.9 while price was 4.0 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 77th percentile of its last 250 bars, expanding (×1.28 vs 10 bars earlier) — the gate allowed it.

**What happened**

- Best point **+0.53R** at bar 1 (4h); worst **-0.80R** at bar 2 (8h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.48R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 469 trades in 8.7 years end this way.
- Gave back 1.01R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| target 3.0 → 0.5 | -0.49R → **+0.48R** | -0.0318R  [-0.079, +0.016] | helps this trade, no measurable effect on the book |
| hold (bars) 12 → 24 | -0.49R → **+0.66R** | -0.0203R  [-0.065, +0.024] | helps this trade, no measurable effect on the book |

### #60 GBP_JPY short · fade · time +0.63R

Opened Fri 18 Sep 09:02 UTC · closed Tue 22 Sep 09:07 · entry 211.013 · stop 212.744 · target 205.819

Traded under params `17b2f25748d6` (reconstructed) — **differs from current in:** bot.ENTRY_WINDOWS_ET None→{'EUR_USD': ((8, 12),), 'GBP_USD': ((8, 12),), 'USD_JPY': ((0, 5), (8, 12)), 'AUD_USD': ((22, 6),), 'NZD_USD': ((22, 5),), 'USD_CAD': ((8, 17),), 'GBP_JPY': ((0, 9),)}; bot.FRIDAY_FLATTEN_HOUR_ET None→16; bot.FRIDAY_FLATTEN_WEEKDAY None→4; bot.WEEKLY_OPEN_HOUR_ET None→0; bot.WEEKLY_OPEN_WEEKDAY None→0; bot.WINDOW_END_INCLUSIVE None→True

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 72.2, 2.1 ATR from the EMA, with the trend.
- RSI depth 2.2 points past the threshold against a cap of 5.0 — passed with 2.8 to spare.
- Volatility: ATR at the 79th percentile of its last 250 bars, expanding (×1.50 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on GBP_JPY; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.

**What happened**

- Best point **+0.86R** at bar 12 (48h); worst **-0.16R** at bar 1 (4h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised +0.63R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it in profit** — 20% of the 469 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| stop (×ATR) 2.5 → 1.5 | +0.60R → **+1.00R** | -0.0030R  [-0.132, +0.126] | helps this trade, no measurable effect on the book |

### #62 USD_JPY short · pullback · time -0.43R

Opened Mon 21 Sep 13:04 UTC · closed Wed 23 Sep 13:07 · entry 157.315 · stop 158.748 · target 153.017

Traded under params `2cf53666b980` — **differs from current in:** bot.ENTRY_WINDOWS_ET.AUD_USD [[22, 6]]→((22, 6),); bot.ENTRY_WINDOWS_ET.EUR_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.GBP_JPY [[0, 9]]→((0, 9),); bot.ENTRY_WINDOWS_ET.GBP_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.NZD_USD [[22, 5]]→((22, 5),); bot.ENTRY_WINDOWS_ET.USD_CAD [[8, 17]]→((8, 17),)

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.1 while price was 0.1 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 75th percentile of its last 250 bars, expanding (×1.28 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on USD_JPY; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.
- Spread at entry 1.4 pips.

**What happened**

- Best point **+0.34R** at bar 6 (24h); worst **-0.47R** at bar 12 (48h), over 12 bar(s) held.
- Volatility contracted ×0.56 during the trade.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.43R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 6% of the 469 trades in 8.7 years end this way.
- Gave back 0.77R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 6 | -0.41R → **-0.00R** | -0.0278R  [-0.072, +0.016] | helps this trade, no measurable effect on the book |

### #63 USD_JPY short · fade · friday +1.30R

Opened Thu 24 Sep 13:02 UTC · closed Fri 25 Sep 20:08 · entry 158.608 · stop 159.662 · target 155.447

Traded under params `2cf53666b980` — **differs from current in:** bot.ENTRY_WINDOWS_ET.AUD_USD [[22, 6]]→((22, 6),); bot.ENTRY_WINDOWS_ET.EUR_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.GBP_JPY [[0, 9]]→((0, 9),); bot.ENTRY_WINDOWS_ET.GBP_USD [[8, 12]]→((8, 12),); bot.ENTRY_WINDOWS_ET.NZD_USD [[22, 5]]→((22, 5),); bot.ENTRY_WINDOWS_ET.USD_CAD [[8, 17]]→((8, 17),)

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 70.8, 2.9 ATR from the EMA, against the trend.
- Counter-trend distance 2.9 ATR against a cap of 3.0 — passed with 0.1 ATR to spare.
- RSI depth 0.8 points past the threshold against a cap of 5.0 — passed with 4.2 to spare.
- Volatility: ATR at the 50th percentile of its last 250 bars, not expanding (×0.98 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.5 pips.

**What happened**

- Best point **+1.58R** at bar 7 (28h); worst **-0.41R** at bar 1 (4h), over 7 bar(s) held.

**Why we exited**

- **Friday 16:00 ET flatten** closed it after 7 bars, realised +1.30R — the weekly rule, not the 12-bar time stop, which it pre-empted.

**Expected?**

- Outcome: **closed by the Friday 16:00 ET flatten** — 43% of the 469 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| target 3.0 → 1.5 | +1.23R → **+1.48R** | +0.0005R  [-0.022, +0.023] | helps this trade, no measurable effect on the book |
| stop (×ATR) 2.5 → 1.5 | +1.23R → **+2.05R** | -0.0030R  [-0.132, +0.126] | helps this trade, no measurable effect on the book |

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| 12-bar clock closed it at a loss | 3 | 6% |
| 12-bar clock closed it in profit | 1 | 20% |
| closed by the Friday 16:00 ET flatten | 1 | 43% |

**One move, 2 positions:** #56, #60 (GBP_JPY short) all closed between Tue 05:08 and 09:07 UTC for +0.15R combined — one market event, so read these together rather than as 2 independent outcomes.

## What the individual trades asked for

Each row is a change that would have improved at least one trade this week. The population column decides whether it deserves a proper test — a single week cannot.

| strategy | change | helped | hurt | net on this week's closed trades | 8.7-year verdict |
|---|---|---|---|---|---|
| rsi_reversion | stop (×ATR) → 1.5 | 2 (+1.25R) | 3 (-1.57R) | -0.32R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 24 | 1 (+1.16R) | 2 (-0.93R) | +0.31R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 4 | 3 (+1.18R) | 1 (-1.06R) | +0.07R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 6 | 3 (+1.24R) | 1 (-0.29R) | +0.75R | WITHIN NOISE |
| rsi_reversion | target → 0.5 | 1 (+0.97R) | 1 (-0.80R) | +0.05R | WITHIN NOISE |
| rsi_reversion_nogate | stop (×ATR) → 1.5 | 2 (+1.22R) | 3 (-1.57R) | -0.35R | WITHIN NOISE |
| rsi_reversion_nogate | hold (bars) → 24 | 1 (+1.16R) | 2 (-0.93R) | +0.31R | WITHIN NOISE |
| rsi_reversion_nogate | hold (bars) → 4 | 3 (+1.18R) | 1 (-1.06R) | +0.07R | WITHIN NOISE |
| rsi_reversion_nogate | hold (bars) → 6 | 3 (+1.24R) | 1 (-0.29R) | +0.75R | WITHIN NOISE |
| rsi_reversion_nogate | target → 0.5 | 1 (+0.97R) | 1 (-0.75R) | +0.11R | WITHIN NOISE |
| rsi_reversion_nogate | target → 1.5 | 1 (+0.25R) | 0 (+0.00R) | +0.25R | WITHIN NOISE |

**Supported by the population:** none. Every change a trade asked for this week is within noise or harmful across 8.7 years — keep the current parameters.

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
