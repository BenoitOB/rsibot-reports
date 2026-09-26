```
==============================================================================
WEEKLY REVIEW — 2026-09-26 11:00 UTC
baseline: 2026-09-19 rev no-git | 328 sim trades / 5.49y | exp +0.100R sd 0.80
==============================================================================

A. EXECUTION INTEGRITY  — bugs; one occurrence is enough to act
  [OK  ] stop exits worse than -1.35R: 0
  [OK  ] days since last entry: 1.9 (expected 0.3 at 1.15/wk, P(zero)=0.730) — within normal quiet
  [OK  ] broker close/order rejections (7d): 0
  [OK  ] failed poll cycles (7d): 1  [auth-401: 25]  ~0.05% of polls
  [OK  ] journal rows open but closed at broker: 0
  [OK  ] known bug artefacts excluded from scoring: #41, #42, #43
  [WARN] exit mix live vs expected: stop 25%/18%  time 75%/39%  target 0%/1%

B. EDGE TRACKING  — observe; act ONLY on a band breach
  closed under current rules: n=16  sumR=-4.83  mean=-0.302R
  expected +0.100R, 95% band at n~20: [-0.249, +0.450]  (cum [-5.0, +9.0]R)
  [ACT ] BELOW the 95% band — investigate before it compounds
  progress to significance: 16/242 trades (~3.8 more years at 1.15/wk)

  kill switch: trailing 50 closed trades sum < -5.0R -> take the strategy off risk
  [warm-up] 16/50 trades under current rules — not armed yet (~6.9 months to arm)
  interim backstop remains the account drawdown halt (note: enforce_halts is False on this practice account)

C. PAIR WATCH  — informational ONLY. Do not prune on these numbers.
  pair      live n   live R   exp R  yrs+  note
  GBP_USD        1   -0.414  -0.089  0/1   lowest-ranked (NOT a drop signal — see note above)
  USD_CAD        4   -0.847  +0.018  4/6   inconsistent across years
  GBP_JPY        2   +0.066  +0.027  4/6   inconsistent across years
  USD_JPY        4   +0.166  +0.086  3/5   inconsistent across years
  EUR_USD        1   -0.029  +0.211  1/1   
  NZD_USD        1   -0.484  +0.221  4/6   inconsistent across years
  AUD_USD        3   -0.438  +0.238  4/6   inconsistent across years

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
