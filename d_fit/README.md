# d_fit: Fit comparable DBLP models

Freezes the AARC-selected primary ridge, retains DBLP-local sensitivity profiles, and bootstraps cohort-specific raw weights.

## Inputs

Inputs are read only from the immediately upstream task (or the documented external source for import tasks).

## Outputs

The task writes tables, manifests, or model artifacts to `output/`. Existing source data are never modified. Read `../DECISIONS.md` for the estimand and inference rules.

## Run

Open `src/d_fit.ipynb` and run all cells. The notebook uses the explicit Desktop paths documented in the top-level README.
