```
==============================================================================
WEEKLY REVIEW — 2026-09-12 11:00 UTC
baseline: 2026-09-09 rev no-git | 515 sim trades / 5.45y | exp +0.161R sd 0.94
==============================================================================

A. EXECUTION INTEGRITY  — bugs; one occurrence is enough to act
  [OK  ] stop exits worse than -1.35R: 0
  [OK  ] days since last entry: 0.9 (expected 0.2 at 1.82/wk, P(zero)=0.789) — within normal quiet
  [OK  ] broker close/order rejections (7d): 0
  [OK  ] failed poll cycles (7d): 2  [auth-401: 21]  ~0.10% of polls
  [OK  ] journal rows open but closed at broker: 0
  [OK  ] known bug artefacts excluded from scoring: #41, #42, #43
  [OK  ] exit-mix check deferred (n=6, needs 15)

B. EDGE TRACKING  — observe; act ONLY on a band breach
  closed under current rules: n=6  sumR=-2.20  mean=-0.367R
  expected +0.161R, 95% band at n~5: [-0.665, +0.988]  (cum [-3.3, +4.9]R)
  [OK  ] inside the band — this week carries NO information about the edge. Change nothing.
  progress to significance: 6/131 trades (~1.3 more years at 1.82/wk)

  kill switch: trailing 50 closed trades sum < -5.0R -> take the strategy off risk
  [warm-up] 6/50 trades under current rules — not armed yet (~5.6 months to arm)
  interim backstop remains the account drawdown halt (note: enforce_halts is False on this practice account)

C. PAIR WATCH  — informational ONLY. Do not prune on these numbers.
  pair      live n   live R   exp R  yrs+  note
  GBP_JPY        0        -  +0.002  3/6   inconsistent across years
  USD_CAD        2   -0.645  +0.078  5/6   
  USD_JPY        1   +0.018  +0.156  4/6   inconsistent across years
  EUR_USD        1   -0.029  +0.174  5/6   
  NZD_USD        1   -0.484  +0.181  4/6   inconsistent across years
  GBP_USD        1   -0.414  +0.270  5/5   
  AUD_USD        0        -  +0.300  5/6   

D. RESEARCH QUEUE  — one falsifiable test per week, bar set in advance
  pass bar (fixed before any test runs): pooled_pf >= 1.30 net of measured spreads; year_consistency positive in >= 2/3 of full years tested; breadth positive on >= 5 of 8 instruments; tuning none — parameters fixed before the test, no post-hoc sweeps; sample >= 200 trades or the result is 'insufficient', not 'fail'
  (queue empty — add a hypothesis before next week)
  0 open / 15 resolved

  DO NOT RE-PROPOSE (tested and failed):
    - subgroup_slicing: Improvement by re-ranking or re-weighting the EXISTING trade population is exhausted. Per-pair pruning (p=0.61), leg weighting (p=0.32), correlation c...
    - trailing_stops: Do not re-propose for any fade strategy here — ATR trail lost with paired t=-3.68 and a mechanism (it harvests the noise a mean-reversion trade must s...
    - price_based_regime_forecasting: Variance ratio, efficiency ratio and realised vol all failed to separate the eras. A reactive kill switch is the accepted answer.

==============================================================================
NO ACTION REQUIRED. The correct move this week is to change nothing
and run the queued research test.
==============================================================================
```
