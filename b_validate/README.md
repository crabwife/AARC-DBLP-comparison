# b_validate: Validate and reconstruct DBLP panels

Aggregates duplicate person-age rows, restores interior zero years, crops to ages 0–12, and defines transparent selection cohorts.

## Inputs

Inputs are read only from the immediately upstream task (or the documented external source for import tasks).

## Outputs

The task writes tables, manifests, or model artifacts to `output/`. Existing source data are never modified. Read `../DECISIONS.md` for the estimand and inference rules.

## Run

Open `src/b_validate.ipynb` and run all cells. The notebook uses the explicit Desktop paths documented in the top-level README.
