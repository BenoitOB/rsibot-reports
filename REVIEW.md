```
==============================================================================
WEEKLY REVIEW — 2026-10-17 11:00 UTC
baseline: 2026-09-19 rev no-git | 328 sim trades / 5.49y | exp +0.100R sd 0.80
scoring trades opened on/after 2026-09-19 21:40 UTC (the rules this baseline describes)
==============================================================================

A. EXECUTION INTEGRITY  — bugs; one occurrence is enough to act
  [OK  ] stop exits worse than -1.35R: 0
  [OK  ] days since last entry: 0.7 (expected 0.1 at 1.15/wk, P(zero)=0.884) — within normal quiet
  [OK  ] broker close/order rejections (7d): 0
  [OK  ] failed poll cycles in TRADEABLE hours (7d): 4  [auth-401: 59]  ~0.20% of polls  (+20 while the market was shut — ignored)
  [OK  ] journal rows open but closed at broker: 0
  [OK  ] exit-mix check deferred (n=5, needs 15)

B. EDGE TRACKING  — observe; act ONLY on a band breach
  closed under current rules: n=5  sumR=+3.58  mean=+0.716R
  expected +0.100R, 95% band at n~5: [-0.598, +0.799]  (cum [-3.0, +4.0]R)
  [OK  ] inside the band — this week carries NO information about the edge. Change nothing.
  progress to significance: 5/242 trades (~4.0 more years at 1.15/wk)

  kill switch: trailing 50 closed trades sum < -5.0R -> take the strategy off risk
  [warm-up] 5/50 trades under current rules — not armed yet (~9.1 months to arm)
  interim backstop remains the account drawdown halt (note: enforce_halts is False on this practice account)

C. PAIR WATCH  — informational ONLY. Do not prune on these numbers.
  pair      live n   live R   exp R  yrs+  note
  GBP_USD        0        -  -0.089  0/1   lowest-ranked (NOT a drop signal — see note above)
  USD_CAD        1   -0.342  +0.018  4/6   inconsistent across years
  GBP_JPY        0        -  +0.027  4/6   inconsistent across years
  USD_JPY        2   +0.460  +0.086  3/5   inconsistent across years
  EUR_USD        0        -  +0.211  1/1   
  NZD_USD        1   -0.009  +0.221  4/6   inconsistent across years
  AUD_USD        1   +3.013  +0.238  4/6   inconsistent across years

D. RESEARCH QUEUE  — one falsifiable test per week, bar set in advance
  pass bar (fixed before any test runs): pooled_pf >= 1.30 net of measured spreads; year_consistency positive in >= 2/3 of full years tested; breadth positive on >= 5 of 8 instruments; tuning none — parameters fixed before the test, no post-hoc sweeps; sample >= 200 trades or the result is 'insufficient', not 'fail'; _calibration_2026_09_13 A 26-week-shifted placebo on ~200-trade terciles produced a 0.14R gap from noise (cftc-positioning-conditioning). The 0.10R pooled-gap bar is below that floor. Raise the bar above ~0.15R for tercile comparisons at this sample size, or require a placebo arm to establish the floor for that specific test.
  (queue empty — add a hypothesis before next week)
  0 open / 26 resolved

  DO NOT RE-PROPOSE (tested and failed):
    - subgroup_slicing: Improvement by re-ranking or re-weighting the EXISTING trade population is exhausted. Per-pair pruning (p=0.61), leg weighting (p=0.32), correlation c...
    - trailing_stops: Do not re-propose for any fade strategy here — ATR trail lost with paired t=-3.68 and a mechanism (it harvests the noise a mean-reversion trade must s...
    - price_based_regime_forecasting: Variance ratio, efficiency ratio and realised vol all failed to separate the eras. A reactive kill switch is the accepted answer.
    - implied_vol_substitutes: EVZ risk-scaling PASSED but CBOE retired the series (2025-03). Two free substitutes have now FAILED stage 1 with the opposite sign: VIX (percentile co...
    - event_calendar_conditioning: Two framings tested and failed — holding-window SPANNING and entry PROXIMITY. In both the PLACEBO (a weekday with no release) produced a gap as large ...

==============================================================================
NO ACTION REQUIRED. The correct move this week is to change nothing
and run the queued research test.
==============================================================================
```
