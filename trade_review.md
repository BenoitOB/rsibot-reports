# Trade review — 2026-11-14 to 2026-11-21

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-03-05 .. 2026-10-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `d5f5b98aff95` · 2 closed (-1.45R) · 0 open

### #76 GBP_JPY long · fade · stop -1.01R

Opened Mon 16 Nov 10:02 UTC · closed Wed 18 Nov 09:08 · entry 210.430 · stop 209.284 · target 213.867

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Fade leg, long.** RSI crossed 30 to 28.8, 1.5 ATR from the EMA, against the trend.
- Counter-trend distance 1.5 ATR against a cap of 3.0 — passed with 1.5 ATR to spare.
- RSI depth 1.2 points past the threshold against a cap of 5.0 — passed with 3.8 to spare.
- Volatility: ATR at the 31st percentile of its last 250 bars, not expanding (×0.97 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 4.1 pips.

**What happened**

- Best point **+0.31R** at bar 10 (40h); worst **-1.01R** at bar 12 (48h), over 12 bar(s) held.

**Why we exited**

- **Stop loss** hit on bar 12 (48h), realised -1.01R.
- It was in profit first (best +0.31R at bar 10) before reversing into the stop.

**Expected?**

- Outcome: **stopped out after being in profit** — 6% of the 1024 trades in 8.7 years end this way.
- Gave back 1.32R from its peak. That alone is not a signal: across the population the peak falls anywhere in the hold, and capping winners costs more than it saves.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| hold (bars) 12 → 8 | -1.03R → **+0.13R** | -0.0227R  [-0.046, +0.000] | helps this trade, no measurable effect on the book |
| stop (×ATR) 2.5 → 3.5 | -1.03R → **-0.45R** | -0.0243R  [-0.084, +0.036] | helps this trade, no measurable effect on the book |
| counter-trend cap (ATR) 3.0 → 1.0 | -1.03R → **+0.00R** (entry would have been blocked) | +0.0107R  [-0.065, +0.087] | helps this trade, no measurable effect on the book |

### #77 USD_JPY long · pullback · friday -0.44R

Opened Fri 20 Nov 10:03 UTC · closed Fri 20 Nov 21:07 · entry 158.828 · stop 158.064 · target 161.119

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Pullback leg, long.** RSI crossed 35 (down) to 34.2 while price was 0.8 ATR above the EMA200 — buying the dip in an uptrend.
- Volatility: ATR at the 21st percentile of its last 250 bars, not expanding (×0.97 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.7 pips.

**What happened**

- Best point **+0.21R** at bar 1 (4h); worst **-0.36R** at bar 1 (4h), over 2 bar(s) held.

**Why we exited**

- **Friday 16:00 ET flatten** closed it after 2 bars, realised -0.44R — the weekly rule, not the 12-bar time stop, which it pre-empted.

**Expected?**

- Outcome: **closed by the Friday 16:00 ET flatten** — 45% of the 1024 trades in 8.7 years end this way.
- **Did not behave as designed:** live result -0.44R differs from the path replay -0.07R by 0.36R — check the fill and the P&L record.

**What would have changed it**

No tested parameter change would have moved this trade by 0.25R or more.

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| stopped out after being in profit | 1 | 6% |
| closed by the Friday 16:00 ET flatten | 1 | 45% |

## rsi_reversion_nogate — A/B CANDIDATE — volatility gate OFF

Account 101-001-39369941-003 · current params `d543f6e0abbe` · 0 closed (+0.00R) · 0 open

_No trades in the window._

## What the individual trades asked for

Each row is a change that would have improved at least one trade this week. The population column decides whether it deserves a proper test — a single week cannot.

| strategy | change | helped | hurt | net on this week's closed trades | 8.7-year verdict |
|---|---|---|---|---|---|
| rsi_reversion | stop (×ATR) → 3.5 | 1 (+0.58R) | 0 (+0.00R) | +0.69R | WITHIN NOISE |
| rsi_reversion | counter-trend cap (ATR) → 1.0 | 1 (+1.03R) | 0 (+0.00R) | +1.03R | WITHIN NOISE |
| rsi_reversion | hold (bars) → 8 | 1 (+1.16R) | 0 (+0.00R) | +1.16R | WITHIN NOISE |

**Supported by the population:** none. Every change a trade asked for this week is within noise or harmful across 8.7 years — keep the current parameters.

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
