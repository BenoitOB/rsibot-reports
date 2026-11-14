# Trade review — 2026-11-07 to 2026-11-14

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-03-05 .. 2026-10-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `d5f5b98aff95` · 1 closed (+3.00R) · 0 open

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
- **Did not behave as designed:** held 39 bars (156h) against a 12-bar rule — the position outlived its exit rules, so this result is NOT what the strategy would have earned.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| stop (×ATR) 2.5 → 1.5 | +1.30R → **+2.16R** | +0.0073R  [-0.080, +0.094] | helps this trade, no measurable effect on the book |

**This week's outcomes vs the population**

| outcome | this week | 8.7-year share |
|---|---|---|
| target hit | 1 | 1% |

## rsi_reversion_nogate — A/B CANDIDATE — volatility gate OFF

Account 101-001-39369941-003 · current params `d543f6e0abbe` · 0 closed (+0.00R) · 0 open

_No trades in the window._

## What the individual trades asked for

Each row is a change that would have improved at least one trade this week. The population column decides whether it deserves a proper test — a single week cannot.

| strategy | change | helped | hurt | net on this week's closed trades | 8.7-year verdict |
|---|---|---|---|---|---|
| rsi_reversion | stop (×ATR) → 1.5 | 1 (+0.87R) | 0 (+0.00R) | +0.87R | WITHIN NOISE |

**Supported by the population:** none. Every change a trade asked for this week is within noise or harmful across 8.7 years — keep the current parameters.

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
