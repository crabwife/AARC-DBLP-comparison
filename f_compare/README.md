# f_compare: Compare DBLP with AARC

Verifies design manifests and creates combined raw-weight, retention, selection, sample-size, overlap, and dynamic diagnostics.

## Inputs

Inputs are read only from the immediately upstream task (or the documented external source for import tasks).

## Outputs

The task writes tables, manifests, or model artifacts to `output/`. Existing source data are never modified. Read `../DECISIONS.md` for the estimand and inference rules.

## Run

Open `src/f_compare.ipynb` and run all cells. The notebook uses the explicit Desktop paths documented in the top-level README.
