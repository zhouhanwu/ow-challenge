# Sausage Roll Promotion Challenge

**Question:** which sausage roll promotion should we use?

We answer it in three stages, each building on the last:

| Stage | Notebook prefix | Goal |
|---|---|---|
| 1. Exploration | `01_` | Understand the data: quality, distributions, how promotions differ |
| 2. Baseline | `02_` | Simplest honest answer, e.g. average sales per promotion. Any model must beat this |
| 3. Modelling | `03_` | Adjust for other factors (store, day, season...) and see if the answer changes |

The final recommendation goes in [`REPORT.md`](REPORT.md).

## Setup

```bash
uv sync                          # install dependencies
uv run nbstripout --install      # strip notebook outputs on commit (avoids merge conflicts)
uv run jupyter lab
```

Put the dataset in `data/` (git-ignored). Get it from the team drive; do not commit it.

## Working as a team of 4

- Notebooks live in `notebooks/` and are named `<stage>_<topic>_<initials>.ipynb`, e.g. `01_sales_trends_wz.ipynb`.
  One person per notebook means no merge conflicts.
- Work on a branch (`<initials>/<topic>`), open a PR into `main`, get one teammate to review.
- Suggested split: two people on exploration, then one on baseline and one on modelling once the data is understood.
  Everyone reviews the final `REPORT.md`.
- Keep it simple: prefer the explainable method. A model we can't explain to a shop manager is not an upgrade.
- Every notebook ends with a short "What I found" cell in plain English.
