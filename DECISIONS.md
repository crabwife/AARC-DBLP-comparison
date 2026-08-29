# Visible decision log

1. DBLP is cropped to the same ages 0–12 as AARC before any model fitting.
2. The primary cohort uses all eligible trajectories, not only the approximately 591 careers observable for 20 years.
3. Two selection sensitivities are mandatory: complete through age 12, and the legacy complete-through-age-20 people cropped back to age 12.
4. DBLP gaps between age 0 and the last observed age are filled with zero productivity because that reproduces the original `pivot(...).fillna(0)` policy. AARC already has explicit person-year grids.
5. People without career age 0 and people with no transition beyond age 0 are excluded and counted; the model does not infer their origin.
6. The split seed and stage convention are identical to AARC. Person IDs are canonicalized before splitting.
7. The primary unrestricted DBLP fit freezes the ridge selected by domain-balanced AARC validation. This prevents a source-specific tuning choice from masquerading as a source difference in coefficient shape.
8. DBLP-local ridge selection remains available only as a sensitivity profile.
9. T5 rho is selected within each DBLP cohort, but it never enters the unrestricted lag features.
10. Cross-source plotting refuses to run unless the AARC manifest confirms 13 years, AR(6,6), raw lags, no lag preconditioning, and no stage-duration averaging.
11. The same early-age nuisance interactions and machine-precision T5 nesting assertion used in AARC are required in DBLP; they are excluded from the reported decay curves.
12. The primary combined plots distinguish DBLP using black, heavier, diamond-marked dashed lines; AARC domains retain redundant color, marker, and line-style encodings.
13. Code is notebook-native: each task has one runnable notebook in `src/`, shared estimators live in `common/core.ipynb`, paths are explicit Desktop paths, functions have no type annotations, and code uses one statement per line with minimal comments.
13. If AARC source IDs are available, overlap is counted and a no-overlap DBLP cohort is fitted. Apparent replication in overlapping people is not described as independent evidence.
14. The causal and latent-state interpretation boundaries in the AARC decision log apply unchanged.
