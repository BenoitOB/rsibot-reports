# Trade review — 2026-10-11 to 2026-10-18

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-02-04 .. 2026-09-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `3ad713814089` · 3 closed (+2.66R) · 0 open

### #65 AUD_USD short · pullback · target +3.01R

Opened Wed 14 Oct 05:02 UTC · closed Thu 15 Oct 12:32 · entry 0.70013 · stop 0.70328 · target 0.69068

Traded under params `3ad713814089` — same as current.

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 66.0 while price was 2.8 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 4th percentile of its last 250 bars, not expanding (×0.79 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.3 pips.

**What happened**

- Best point **+3.23R** at bar 8 (32h); worst **-0.38R** at bar 2 (8h), over 8 bar(s) held.
- Volatility **expanded ×1.58** during the trade — the market repriced rather than reverted.

**Why we exited**

- **Target** hit on bar 8, realised +3.01R.

**Expected?**

- Outcome: **target hit** — 1% of the 469 trades in 8.7 years end this way.
- **Unusual** for these rules — worth a look, but one trade.

**What would have changed it**

No tested parameter change would have moved this trade by 0.25R or more.

### #66 NZD_USD short · pullback · friday -0.01R

Opened Fri 16 Oct 05:02 UTC · closed Fri 16 Oct 20:09 · entry 0.56534 · stop 0.57063 · target 0.54948

Traded under params `3ad713814089` — same as current.

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 66.3 while price was 1.8 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 92nd percentile of its last 250 bars, expanding (×1.67 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 2.4 pips.

**What happened**

- Best point **+0.22R** at bar 3 (12h); worst **-0.42R** at bar 2 (8h), over 3 bar(s) held.

**Why we exited**

- **Friday 16:00 ET flatten** closed it after 3 bars, realised -0.01R — the weekly rule, not the 12-bar time stop, which it pre-empted.

**Expected?**

- Outcome: **closed by the Friday 16:00 ET flatten** — 43% of the 469 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

No tested parameter change would have moved this trade by 0.25R or more.

### #67 USD_CAD long · pullback · friday -0.34R

Opened Fri 16 Oct 17:03 UTC · closed Fri 16 Oct 20:09 · entry 1.41648 · stop 1.40872 · target 1.43977

Traded under params `3ad713814089` — same as current.

**Why we entered**

- **Pullback leg, long.** RSI crossed 35 (down) to 34.1 while price was 1.3 ATR above the EMA200 — buying the dip in an uptrend.
- Volatility: ATR at the 100th percentile of its last 250 bars, expanding (×1.32 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.8 pips.

**What happened**

- Best point **+0.00R** at bar 0 (0h); worst **-0.37R** at bar 1 (4h), over 1 bar(s) held.

**Why we exited**

- **Friday 16:00 ET flatten** closed it after 1 bars, realised -0.34R — the weekly rule, not the 12-bar time stop, which it pre-empted.

**Expected?**

- Outcome: **closed by the Friday 16:00 ET flatten** — 43% of the 469 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

No tested parameter change would have moved this trade by 0.25R or more.

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| closed by the Friday 16:00 ET flatten | 2 | 43% |
| target hit | 1 | 1% |

## rsi_reversion_nogate — A/B CANDIDATE — volatility gate OFF

Account 101-001-39369941-003 · current params `f4f939f2082e` · 0 closed (+0.00R) · 0 open

_No trades in the window._

## What the individual trades asked for

Each row is a change that would have improved at least one trade this week. The population column decides whether it deserves a proper test — a single week cannot.

_No trade this week would have been moved by a tested parameter._

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
