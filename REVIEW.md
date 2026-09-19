```
==============================================================================
WEEKLY REVIEW — 2026-09-19 20:26 UTC
baseline: 2026-09-18 rev no-git | 731 sim trades / 5.49y | exp +0.135R sd 0.89
==============================================================================

A. EXECUTION INTEGRITY  — bugs; one occurrence is enough to act
  [OK  ] stop exits worse than -1.35R: 0
  [OK  ] days since last entry: 1.5 (expected 0.5 at 2.56/wk, P(zero)=0.583) — within normal quiet
  [OK  ] broker close/order rejections (7d): 0
  [OK  ] failed poll cycles (7d): 1  [auth-401: 25]  ~0.05% of polls
  [OK  ] journal rows open but closed at broker: 0
  [OK  ] known bug artefacts excluded from scoring: #41, #42, #43
  [OK  ] exit-mix check deferred (n=11, needs 15)

B. EDGE TRACKING  — observe; act ONLY on a band breach
  closed under current rules: n=11  sumR=-5.61  mean=-0.510R
  expected +0.135R, 95% band at n~10: [-0.419, +0.689]  (cum [-4.2, +6.9]R)
  [ACT ] BELOW the 95% band — investigate before it compounds
  progress to significance: 11/169 trades (~1.2 more years at 2.56/wk)

  kill switch: trailing 50 closed trades sum < -5.0R -> take the strategy off risk
  [warm-up] 11/50 trades under current rules — not armed yet (~3.5 months to arm)
  interim backstop remains the account drawdown halt (note: enforce_halts is False on this practice account)

C. PAIR WATCH  — informational ONLY. Do not prune on these numbers.
  pair      live n   live R   exp R  yrs+  note
  USD_CAD        4   -0.847  -0.017  3/6   lowest-ranked (NOT a drop signal — see note above)
  GBP_JPY        0        -  +0.077  4/6   inconsistent across years
  EUR_USD        1   -0.029  +0.126  5/6   
  AUD_USD        3   -0.438  +0.143  5/6   
  USD_JPY        1   +0.018  +0.162  5/6   
  GBP_USD        1   -0.414  +0.176  5/6   
  NZD_USD        1   -0.484  +0.265  6/6   

D. RESEARCH QUEUE  — one falsifiable test per week, bar set in advance
  pass bar (fixed before any test runs): pooled_pf >= 1.30 net of measured spreads; year_consistency positive in >= 2/3 of full years tested; breadth positive on >= 5 of 8 instruments; tuning none — parameters fixed before the test, no post-hoc sweeps; sample >= 200 trades or the result is 'insufficient', not 'fail'; _calibration_2026_09_13 A 26-week-shifted placebo on ~200-trade terciles produced a 0.14R gap from noise (cftc-positioning-conditioning). The 0.10R pooled-gap bar is below that floor. Raise the bar above ~0.15R for tercile comparisons at this sample size, or require a placebo arm to establish the floor for that specific test.
  (queue empty — add a hypothesis before next week)
  0 open / 25 resolved

  DO NOT RE-PROPOSE (tested and failed):
    - subgroup_slicing: Improvement by re-ranking or re-weighting the EXISTING trade population is exhausted. Per-pair pruning (p=0.61), leg weighting (p=0.32), correlation c...
    - trailing_stops: Do not re-propose for any fade strategy here — ATR trail lost with paired t=-3.68 and a mechanism (it harvests the noise a mean-reversion trade must s...
    - price_based_regime_forecasting: Variance ratio, efficiency ratio and realised vol all failed to separate the eras. A reactive kill switch is the accepted answer.
    - implied_vol_substitutes: EVZ risk-scaling PASSED but CBOE retired the series (2025-03). Two free substitutes have now FAILED stage 1 with the opposite sign: VIX (percentile co...
    - event_calendar_conditioning: Two framings tested and failed — holding-window SPANNING and entry PROXIMITY. In both the PLACEBO (a weekday with no release) produced a gap as large ...

==============================================================================
ACTION REQUIRED — 1 item(s):
  * live expectancy below the 95% band
==============================================================================
```
