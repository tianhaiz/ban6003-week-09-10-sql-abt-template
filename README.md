# BAN 6003 Weeks 9-10: Neon SQL Fundamentals, Joins, and ABT Preparation

**BAN 6003: Data Management and Analytics Integration**  
**Weeks 9-10 GitHub Template**

This repository contains the notebooks, data files, environment files, and local check scripts for this assignment package. Detailed lab instructions are provided in Canvas/LMS.

## Shared Course Database Setup

This assignment uses the BAN 6003 shared readonly Neon database for SQL practice. The notebooks include a setup cell that copies `.env.example` to `.env` for you. Do not commit `.env`.

```bash
# The notebook setup cell handles this for you.
# If needed, you can also run:
cp .env.example .env
```

If your instructor provides an updated readonly connection string, paste it into `.env` as `DATABASE_URL`.

## Canvas / LMS Lab Guide

Read the Canvas/LMS lab guide before working in this repository. The LMS page contains the detailed workflow, submission instructions, and any module-specific notes. This README is only a quick repository checklist.

## Required Notebooks

- `notebooks/module9_neon_sql_fundamentals_guided_lab.ipynb`
- `notebooks/module10_sql_joins_abt_guided_lab.ipynb`

## Required Files

- No local data files are required.

## How to Work

1. Create your own GitHub repository from this template.
2. Use GitHub Codespaces as the main working environment. If you are technically experienced, you may use local Jupyter/conda instead.
3. Install dependencies with `python -m pip install -r requirements.txt` if working locally.
4. Open the notebooks in the order listed above.
5. Run cells from top to bottom.
6. Complete all `Your Turn`, exercise, checkpoint, and reflection sections.
7. Save your notebooks and required outputs.
8. Submit your GitHub repository link through Canvas.

## Completion Check

Your instructor may run a local completion and reproducibility check after submission. The check is designed to support the automatic portion of the lab grade. It verifies that required files exist, notebooks run when possible, marked code cells have real code, required output-producing cells have output after execution, and written response placeholders have been replaced.

The check does not evaluate the quality of your interpretation. Your instructor may grade the remaining portion manually using the assignment rubric.


## Database Note

This assignment uses Neon/Postgres. Create a `.env` file locally or in Codespaces with `DATABASE_URL=...`, but do not commit `.env`. For instructor-side checks, SQL notebooks can run when the local environment has a valid readonly `DATABASE_URL`.

## Submit

Submit your GitHub repository link through Canvas before the deadline. Your repository should be public. If your GitHub repository is private, invite the instructor account `zzz1990771` or `zzz1990771@gmail.com` before submitting the link.

If you are using GitHub, a typical commit workflow is:

```bash
git add .
git commit -m "Complete Weeks 9-10 BAN 6003 assignment"
git push
```
