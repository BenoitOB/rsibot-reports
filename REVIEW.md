```
==============================================================================
WEEKLY REVIEW — 2026-10-24 11:00 UTC
baseline: 2026-10-19 rev no-git | 701 sim trades / 5.46y | exp +0.133R sd 0.78
scoring trades opened on/after 2026-09-19 21:40 UTC (the rules this baseline describes)
==============================================================================

A. EXECUTION INTEGRITY  — bugs; one occurrence is enough to act
  [OK  ] stop exits worse than -1.35R: 0
  [OK  ] days since last entry: 2.4 (expected 0.9 at 2.47/wk, P(zero)=0.427) — within normal quiet
  [OK  ] would-be halts (7d): none — no safety limit came close to firing
  [OK  ] broker close/order rejections (7d): 0
  [OK  ] failed poll cycles in TRADEABLE hours (7d): 1  [auth-401: 71]  ~0.05% of polls
  [OK  ] live account: 101-001-39369941-001 = "Primary" in the OANDA UI | last broker FILL 2026-10-23 20:03:08 UTC (102 lifetime)
  [OK  ] journal rows open but closed at broker: 0
  [OK  ] exit-mix check deferred (n=11, needs 15)

B. EDGE TRACKING  — observe; act ONLY on a band breach
  closed under current rules: n=11  sumR=+3.34  mean=+0.304R
  expected +0.133R, 95% band at n~10: [-0.352, +0.618]  (cum [-3.5, +6.2]R)
  [OK  ] inside the band — this week carries NO information about the edge. Change nothing.
  progress to significance: 11/133 trades (~1.0 more years at 2.47/wk)

  kill switch: trailing 50 closed trades sum < -5.0R -> take the strategy off risk
  [warm-up] 11/50 trades under current rules — not armed yet (~3.7 months to arm)
  interim backstop remains the account drawdown halt (note: enforce_halts is False on this practice account)

C. PAIR WATCH  — informational ONLY. Do not prune on these numbers.
  pair      live n   live R   exp R  yrs+  note
  USD_CAD        1   -0.342  +0.012  4/6   inconsistent across years
  GBP_JPY        0        -  +0.038  4/6   inconsistent across years
  GBP_USD        1   +0.280  +0.075  3/5   inconsistent across years
  USD_JPY        2   +0.460  +0.176  6/6   
  NZD_USD        5   -0.156  +0.194  4/6   inconsistent across years
  AUD_USD        2   +1.633  +0.211  4/6   inconsistent across years
  EUR_USD        0        -  +0.224  6/6   

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
