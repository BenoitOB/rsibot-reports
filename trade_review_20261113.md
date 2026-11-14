# Trade review — 2026-10-19 to 2026-11-13

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-03-05 .. 2026-10-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `d5f5b98aff95` · 8 closed (+5.24R) · 0 open

### #68 NZD_USD short · pullback · time -0.53R

Opened Mon 19 Oct 13:04 UTC · closed Wed 21 Oct 13:01 · entry 0.56722 · stop 0.57182 · target 0.55343

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.9 while price was 1.0 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 59th percentile of its last 250 bars, not expanding (×0.94 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 2.4 pips.

**What happened**

- Best point **+0.29R** at bar 1 (4h); worst **-0.58R** at bar 7 (28h), over 12 bar(s) held.
- Volatility contracted ×0.70 during the trade.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.53R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 7% of the 1024 trades in 8.7 years end this way.
- Gave back 0.83R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 10 | -0.51R → **-0.05R** | -0.0131R  [-0.029, +0.003] | helps this trade, no measurable effect on the book |

### #69 NZD_USD short · pullback · time -0.37R

Opened Tue 20 Oct 05:01 UTC · closed Thu 22 Oct 05:04 · entry 0.56751 · stop 0.57148 · target 0.55558

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 66.2 while price was 0.8 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 35th percentile of its last 250 bars, not expanding (×0.70 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 1 short trade(s) were already open on NZD_USD; this is position 2 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.
- Spread at entry 2.3 pips.

**What happened**

- Best point **+0.08R** at bar 6 (24h); worst **-0.89R** at bar 11 (44h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.37R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it at a loss** — 7% of the 1024 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 6 | -0.39R → **+0.02R** | -0.0255R  [-0.056, +0.005] | helps this trade, no measurable effect on the book |

### #70 AUD_USD short · fade · time +0.25R

Opened Wed 21 Oct 09:01 UTC · closed Fri 23 Oct 09:00 · entry 0.70246 · stop 0.70640 · target 0.69063

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 70.9, 0.5 ATR from the EMA, against the trend.
- Counter-trend distance 0.5 ATR against a cap of 3.0 — passed with 2.5 ATR to spare.
- RSI depth 0.9 points past the threshold against a cap of 5.0 — passed with 4.1 to spare.
- Volatility: ATR at the 40th percentile of its last 250 bars, not expanding (×0.81 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.3 pips.

**What happened**

- Best point **+0.77R** at bar 7 (28h); worst **-0.31R** at bar 4 (16h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised +0.25R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it in profit** — 19% of the 1024 trades in 8.7 years end this way.
- Gave back 0.52R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

No tested parameter change would have moved this trade by 0.25R or more.

### #71 GBP_USD short · fade · time +0.28R

Opened Wed 21 Oct 09:01 UTC · closed Fri 23 Oct 09:00 · entry 1.33949 · stop 1.34571 · target 1.32083

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 73.9, 3.0 ATR from the EMA, against the trend.
- Counter-trend distance 3.0 ATR against a cap of 3.0 — passed with 0.0 ATR to spare.
- RSI depth 3.9 points past the threshold against a cap of 5.0 — passed with 1.1 to spare.
- Volatility: ATR at the 53rd percentile of its last 250 bars, not expanding (×0.82 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.9 pips.

**What happened**

- Best point **+0.64R** at bar 8 (32h); worst **-0.39R** at bar 6 (24h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised +0.28R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it in profit** — 19% of the 1024 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 24 | +0.27R → **+1.11R** | -0.0415R  [-0.070, -0.013] | helps this trade, **hurts the book** |

### #72 NZD_USD short · pullback · time -0.04R

Opened Wed 21 Oct 09:01 UTC · closed Fri 23 Oct 09:00 · entry 0.56844 · stop 0.57158 · target 0.55902

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.2 while price was 0.1 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 5th percentile of its last 250 bars, not expanding (×0.68 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 2 short trade(s) were already open on NZD_USD; this is position 3 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.
- Spread at entry 2.4 pips.

**What happened**

- Best point **+0.52R** at bar 8 (32h); worst **-0.82R** at bar 4 (16h), over 12 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised -0.04R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it near flat** — 11% of the 1024 trades in 8.7 years end this way.
- Gave back 0.56R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| target 3.0 → 0.5 | -0.04R → **+0.45R** | -0.0290R  [-0.062, +0.004] | helps this trade, no measurable effect on the book |

### #73 NZD_USD short · fade · friday +0.17R

Opened Thu 22 Oct 01:02 UTC · closed Fri 23 Oct 20:03 · entry 0.57069 · stop 0.57402 · target 0.56071

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Fade leg, short.** RSI crossed 70 to 72.1, 1.4 ATR from the EMA, against the trend.
- Counter-trend distance 1.4 ATR against a cap of 3.0 — passed with 1.6 ATR to spare.
- RSI depth 2.1 points past the threshold against a cap of 5.0 — passed with 2.9 to spare.
- Volatility: ATR at the 12th percentile of its last 250 bars, not expanding (×0.81 vs 10 bars earlier) — the gate allowed it.
- **Stacked:** 2 short trade(s) were already open on NZD_USD; this is position 3 on the pair — a fresh valid signal, which the strategy takes regardless of open positions.
- Spread at entry 2.3 pips.

**What happened**

- Best point **+1.17R** at bar 4 (16h); worst **-0.07R** at bar 1 (4h), over 10 bar(s) held.

**Why we exited**

- **Friday 16:00 ET flatten** closed it after 10 bars, realised +0.17R — the weekly rule, not the 12-bar time stop, which it pre-empted.

**Expected?**

- Outcome: **closed by the Friday 16:00 ET flatten** — 45% of the 1024 trades in 8.7 years end this way.
- Gave back 1.00R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| target 3.0 → 1.0 | +0.09R → **+0.95R** | -0.0027R  [-0.026, +0.021] | helps this trade, no measurable effect on the book |
| hold (bars) 12 → 24 | +0.09R → **+0.89R** | -0.0415R  [-0.070, -0.013] | helps this trade, **hurts the book** |

### #74 GBP_USD long · fade · time +2.48R

Opened Wed 28 Oct 09:01 UTC · closed Fri 30 Oct 09:00 · entry 1.32919 · stop 1.32427 · target 1.34394

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Fade leg, long.** RSI crossed 30 to 29.7, 2.2 ATR from the EMA, against the trend.
- Counter-trend distance 2.2 ATR against a cap of 3.0 — passed with 0.8 ATR to spare.
- RSI depth 0.3 points past the threshold against a cap of 5.0 — passed with 4.7 to spare.
- Volatility: ATR at the 9th percentile of its last 250 bars, not expanding (×0.78 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.9 pips.

**What happened**

- Best point **+2.57R** at bar 12 (48h); worst **-0.35R** at bar 1 (4h), over 12 bar(s) held.
- Volatility **expanded ×1.63** during the trade — the market repriced rather than reverted.

**Why we exited**

- **12-bar time stop** closed it after 12 bars, realised +2.48R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it in profit** — 19% of the 1024 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 20 | +2.46R → **+2.96R** | -0.0328R  [-0.059, -0.006] | helps this trade, **hurts the book** |
| stop (×ATR) 2.5 → 2.0 | +2.46R → **+2.95R** | +0.0051R  [-0.071, +0.081] | helps this trade, no measurable effect on the book |

### #75 EUR_USD short · pullback · target +3.00R

Opened Thu 05 Nov 06:03 UTC · closed Fri 13 Nov 15:49 · entry 1.12611 · stop 1.13381 · target 1.10300

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.0 while price was 0.2 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 87th percentile of its last 250 bars, expanding (×1.13 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.7 pips.

**What happened**

- Best point **+3.05R** at bar 39 (156h); worst **-0.07R** at bar 1 (4h), over 39 bar(s) held.
- Volatility contracted ×0.77 during the trade.

**Why we exited**

- **Target** hit on bar 39, realised +3.00R.

**Expected?**

- Outcome: **target hit** — 1% of the 1024 trades in 8.7 years end this way.
- **Unusual** for these rules — worth a look, but one trade.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| stop (×ATR) 2.5 → 1.5 | +1.30R → **+2.16R** | +0.0073R  [-0.080, +0.094] | helps this trade, no measurable effect on the book |

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| 12-bar clock closed it in profit | 3 | 19% |
| 12-bar clock closed it at a loss | 2 | 7% |
| 12-bar clock closed it near flat | 1 | 11% |
| closed by the Friday 16:00 ET flatten | 1 | 45% |
| target hit | 1 | 1% |

## rsi_reversion_nogate — A/B CANDIDATE — volatility gate OFF

Account 101-001-39369941-003 · current params `d543f6e0abbe` · 0 closed (+0.00R) · 0 open

_No trades in the window._

## What the individual trades asked for

Each row is a change that would have improved at least one trade this week. The population column decides whether it deserves a proper test — a single week cannot.

| strategy | change | helped | hurt | net on this week's closed trades | 8.7-year verdict |
|---|---|---|---|---|---|
| rsi_reversion | stop (×ATR) → 1.5 | 2 (+1.34R) | 3 (-2.05R) | -0.30R | WITHIN NOISE |
| rsi_reversion | stop (×ATR) → 2.0 | 2 (+0.81R) | 2 (-1.67R) | -0.83R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 10 | 1 (+0.46R) | 3 (-1.11R) | -0.58R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 20 | 2 (+0.97R) | 1 (-0.35R) | +0.85R | HURTS |
| rsi_reversion | hold (bars) → 24 | 3 (+2.14R) | 3 (-0.90R) | +1.21R | HURTS |
| rsi_reversion | hold (bars) → 6 | 3 (+1.08R) | 3 (-3.06R) | -2.05R | WITHIN NOISE |
| rsi_reversion | target → 0.5 | 2 (+0.86R) | 2 (-2.82R) | -1.54R | WITHIN NOISE |
| rsi_reversion | target → 1.0 | 1 (+0.86R) | 2 (-1.82R) | -0.95R | WITHIN NOISE |

**Supported by the population:** none. Every change a trade asked for this week is within noise or harmful across 8.7 years — keep the current parameters.

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
