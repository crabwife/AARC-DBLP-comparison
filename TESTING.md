# Verification record

Verified on 2026-08-28 after the synthetic AARC run, using 420 synthetic DBLP people with 2–21 source years and 30 deliberately overlapping AARC identifiers.

- All eligible cropped to 13 years: 420 people
- Complete through 13 years: 252 people
- Legacy complete through 20 years, cropped to 13: 112 people
- All eligible excluding AARC overlap: 390 people
- Both project manifests reported the identical estimator checksum. After the notebook-native refactor, the shared notebook checksum is `2121c5f46d89628d9458f285ac8a0fb4f446f8a5ee128f63b0e633b95c623498`.
- T5 nesting error was zero in every DBLP cohort.
- All six PDP tasks, observation-matched simulations, cohort sensitivities, overlap accounting, and nine combined figures completed successfully.
- Representative combined raw-weight log, retention-forest, and DBLP cohort-sensitivity figures were visually inspected.
- The notebook-native refactor was rerun end to end. All task code executed from `src/*.ipynb`, the strict AARC–DBLP design match passed, and all nine combined figures regenerated.
- Static style checks found no Python files, no non-notebook files in any `src/`, no annotated function signatures, no semicolon statement separators, and no root-discovery or environment-fallback code.

These are mechanics tests on synthetic data. They do not report substantive AARC or DBLP findings.
