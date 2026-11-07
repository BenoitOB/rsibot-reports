# Trade review — 2026-10-31 to 2026-11-07

Every trade closed in the window, plus every trade still open, for the active demo strategies. Paths are replayed on H4 **mid** candles — a description of what the market did, not a fill simulation. Each proposed change is shown with its effect on the whole 8.7-year population (2018-03-05 .. 2026-10-18), because hindsight on one trade always finds a better parameter.

## rsi_reversion — CONTROL — volatility gate ON

Account 101-001-39369941-001 · current params `d5f5b98aff95` · 1 closed (+0.83R) · 0 open

### #75 EUR_USD short · pullback · time +0.83R

Opened Thu 05 Nov 06:03 UTC · closed Fri 06 Nov 05:46 · entry 1.12611 · stop 1.13381 · target 1.10300

Traded under params `d5f5b98aff95` — same as current.

**Why we entered**

- **Pullback leg, short.** RSI crossed 65 up to 65.0 while price was 0.2 ATR below the EMA200 — selling the rally in a downtrend.
- Volatility: ATR at the 87th percentile of its last 250 bars, expanding (×1.13 vs 10 bars earlier) — the gate allowed it.
- Spread at entry 1.7 pips.

**What happened**

- Best point **+0.91R** at bar 6 (24h); worst **-0.07R** at bar 1 (4h), over 6 bar(s) held.

**Why we exited**

- **12-bar time stop** closed it after 6 bars, realised +0.83R — the exit this strategy makes most of its money on.

**Expected?**

- Outcome: **12-bar clock closed it in profit** — 19% of the 1024 trades in 8.7 years end this way.
- **Expected** — a normal outcome for these rules.

**What would have changed it**

| change | this trade | across 8.7 years (Δ exp/trade, 95% CI) | verdict |
|---|---|---|---|
| stop (×ATR) 2.5 → 1.5 | +1.54R → **+2.57R** | +0.0073R  [-0.080, +0.094] | helps this trade, no measurable effect on the book |

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
| rsi_reversion | stop (×ATR) → 1.5 | 1 (+1.03R) | 0 (+0.00R) | +1.03R | WITHIN NOISE |

**Supported by the population:** none. Every change a trade asked for this week is within noise or harmful across 8.7 years — keep the current parameters.

---

_This review proposes; it never changes a parameter. The per-trade numbers are hindsight on one path. Only a change marked SUPPORTED — better across the whole population, outside the noise, in both eras — is worth a research-queue test, and the decision is yours._
