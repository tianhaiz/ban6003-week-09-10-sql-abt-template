# BAN 6003 Weeks 9-10: Neon SQL Fundamentals, Joins, and ABT Preparation

**BAN 6003: Data Management and Analytics Integration**  
**Weeks 9-10 GitHub Classroom Template**

This repository contains the notebooks and guidance for this assignment package. The grouping is designed to reduce setup overhead while keeping related skills together.

## Shared Course Database Setup

This assignment uses the BAN 6003 shared readonly Neon database for SQL practice. The notebooks include a setup cell that copies `.env.example` to `.env` for you. Do not commit `.env`.

```bash
# The notebook setup cell handles this for you.
# If needed, you can also run:
cp .env.example .env
```

If your instructor provides an updated readonly connection string, paste it into `.env` as `DATABASE_URL`.

## Required Notebooks

- `notebooks/module9_neon_sql_fundamentals_guided_lab.ipynb`
- `notebooks/module10_sql_joins_abt_guided_lab.ipynb`

## Required Files

- No local data files are required.

## How to Work

1. Open this repository in GitHub Codespaces.
2. Wait for the setup process to finish.
3. Open the notebooks in the order listed above.
4. Select the `base` kernel if prompted.
5. Run cells from top to bottom.
6. Complete all `Your Turn`, exercise, checkpoint, and reflection sections.
7. Save your notebooks.
8. Commit and push your work.

## Autograding / Completion Check

GitHub Actions runs a completion and reproducibility check. The check is designed to support the automatic portion of the lab grade. It verifies that required files exist, notebooks run when possible, marked code cells have real code, required output-producing cells have output after execution, and written response placeholders have been replaced.

The check does not evaluate the quality of your interpretation. Your instructor may grade the remaining portion manually using the assignment rubric.


## Database Note

This assignment uses Neon/Postgres. Create a `.env` file locally or in Codespaces with `DATABASE_URL=...`, but do not commit `.env`. The GitHub Actions check runs static SQL completeness checks unless a `DATABASE_URL` secret is configured.

## Submit

Commit and push your work before the deadline:

```bash
git add .
git commit -m "Complete Weeks 9-10 BAN 6003 assignment"
git push
```
