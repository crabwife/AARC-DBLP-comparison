# Comparable DBLP methods

The estimator, equations, stages, raw-lag definition, early-age nesting interactions, bootstrap, and geometric-shape summary are byte-identical to those documented in `SHL_aarc_modeling/METHODS.md`. The fit manifests record and compare the shared core-code SHA-256 checksum before cross-source plotting.

## DBLP panel reconstruction

The input is `df_trajs_all`. Duplicate person-age rows are summed, matching the legacy preparation. People must have age 0 and at least age 1. Between age 0 and a person's last observed source age, missing person-years are filled with zero productivity, reproducing the original DBLP `pivot(...).fillna(0)` policy. Every cohort is then cropped to ages 0–12.

## Cohorts

- `all_eligible_cropped13` is primary and uses all eligible trajectories.
- `complete13_cropped` requires source observation through age 12.
- `legacy_complete20_cropped13` requires source observation through age 20 and then crops to age 12, isolating the legacy complete-career selection effect from the horizon effect.
- `all_eligible_no_aarc_overlap` is created when AARC IDs are available and at least 50 DBLP people remain after overlap removal.

The AARC-selected ridge is frozen for every primary DBLP coefficient fit. DBLP-local validation optima are exported only as a sensitivity profile. T5 rho is selected separately within each cohort because it is a comparator parameter, not an unrestricted-feature transformation.

## Cross-source output

`f_compare` refuses to run unless the two manifests agree on the 13-year horizon, AR order, memory lags, fully identified stages, raw-lag policy, absence of lag preconditioning and duration averaging, presence of early-age nesting interactions, and exact shared core checksum. Combined figures label DBLP explicitly and keep selection cohorts separate.

Because AARC productivity is DBLP-linked, agreement is evidence of cross-domain and cross-sample generalization, not full independence of measurement source.
