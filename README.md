# SHL DBLP comparable: 13-year cross-source replication

This PDP pipeline reconstructs the DBLP computer-science analysis under the exact 13-year, variable-follow-up, raw-lag design used by `SHL_aarc_modeling`, then produces combined AARC–DBLP diagnostics.

Place this folder at `~/Desktop/SHL_dblp_comparable`. The DBLP input path is explicitly `~/Desktop/SHL_SPAARW2/prepare/output/df_trajs_all`; the code does not search for alternate directories or extensions. Run `SHL_aarc_modeling` first, then run these notebooks in order:

1. `a_import/src/a_import.ipynb`
2. `b_validate/src/b_validate.ipynb`
3. `c_prepare/src/c_prepare.ipynb`
4. `d_fit/src/d_fit.ipynb`
5. `e_simulate/src/e_simulate.ipynb`
6. `f_compare/src/f_compare.ipynb`

Each task notebook loads `common/core.ipynb` directly. The combined analysis reads AARC results explicitly from `~/Desktop/SHL_aarc_modeling`.

## Tasks

1. `a_import`: byte-for-byte resolution/import of `df_trajs_all`.
2. `b_validate`: canonical identifiers, duplicate aggregation, exact age-0 origin, 13-year crop, and explicit zero-year reconstruction matching the legacy DBLP pivot/fill policy.
3. `c_prepare`: raw AR lags and four transparent cohorts when possible: all eligible, complete 13-year, legacy complete 20-year cropped to 13, and all eligible excluding AARC-ID overlap.
4. `d_fit`: exact T5 and unrestricted AR(6,6) estimators. The primary coefficient comparison freezes the ridge selected in AARC; DBLP-local ridge optima are sensitivity results only.
5. `e_simulate`: recursive, observation-matched simulations.
6. `f_compare`: combined AARC/DBLP raw slopes, retention summaries, sample-size views, DBLP selection sensitivity, overlap accounting, and dynamic diagnostics.

All run settings are in `config.json`. Production results should use its defaults or more bootstrap replicates.

## Primary comparison

`all_eligible_cropped13` is the primary DBLP cohort. It uses every person with age 0 and at least one transition, crops at age 12, and never requires a 20-year career. `complete13_cropped` and `legacy_complete20_cropped13` reveal how the old complete-career restriction changes the recovered shape. If the AARC person crosswalk is available, the no-overlap cohort directly diagnoses sample overlap.

The combined result is a cross-domain and cross-sample replication. It is not a completely independent data-source replication because AARC productivity is DBLP-linked.
