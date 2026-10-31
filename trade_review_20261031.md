# Trade review — 2026-10-24 to 2026-10-31

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-03-05 .. 2026-10-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `d5f5b98aff95` · 1 closed (+2.48R) · 0 open

### #74 GBP_USD long · fade · time +2.48R

Opened Wed 28 Oct 09:01 UTC · closed Fri 30 Oct 09:05 · entry 1.32919 · stop 1.32427 · target 1.34394

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
| stop (×ATR) 2.5 → 2.0 | +2.46R → **+2.95R** | +0.0051R  [-0.071, +0.081] | helps this trade, no measurable effect on the book |

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| 12-bar clock closed it in profit | 1 | 19% |

## rsi_reversion_nogate — A/B CANDIDATE — volatility gate OFF

Account 101-001-39369941-003 · current params `d543f6e0abbe` · 0 closed (+0.00R) · 0 open

_No trades in the window._

## What the individual trades asked for

Each row is a change that would have improved at least one trade this week. The population column decides whether it deserves a proper test — a single week cannot.

| strategy | change | helped | hurt | net on this week's closed trades | 8.7-year verdict |
|---|---|---|---|---|---|
| rsi_reversion | stop (×ATR) → 2.0 | 1 (+0.49R) | 0 (+0.00R) | +0.49R | WITHIN NOISE |

**Supported by the population:** none. Every change a trade asked for this week is within noise or harmful across 8.7 years — keep the current parameters.

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
