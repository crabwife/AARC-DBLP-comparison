# a_import: Import DBLP trajectories

Resolves and copies df_trajs_all without mutation.

## Inputs

Inputs are read only from the immediately upstream task (or the documented external source for import tasks).

## Outputs

The task writes tables, manifests, or model artifacts to `output/`. Existing source data are never modified. Read `../DECISIONS.md` for the estimand and inference rules.

## Run

Open `src/a_import.ipynb` and run all cells. The notebook uses the explicit Desktop paths documented in the top-level README.
