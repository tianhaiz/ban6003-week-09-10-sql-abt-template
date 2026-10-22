# BAN 6003 Weeks 9-10: Neon SQL Fundamentals, Joins, and ABT Preparation

**BAN 6003: Data Management and Analytics Integration**  
**Weeks 9-10 GitHub Template**

This repository contains the notebooks, environment files, and output folders for this assignment package. Detailed lab instructions are provided in Canvas/LMS.

## Shared Course Database Setup

This assignment uses the BAN 6003 shared read-only Neon database for SQL practice. Your instructor posts the connection string on the Canvas page **"Module 9 Database Connection"**.

1. Open the Module 9 notebook and run the cells from the top. The connection cell creates a file named `.env` in the top folder of this repository (next to `README.md`) and stops with a message. This is expected.
2. Open `.env` and paste the connection string from Canvas right after `DATABASE_URL=`. Save the file and run the connection cell again.
3. Never commit `.env`. It is listed in `.gitignore`, so Git ignores it.

## Canvas / LMS Lab Guide

Read the Canvas/LMS lab guide before working in this repository. The LMS page contains the detailed workflow, submission instructions, and any module-specific notes. This README is only a quick repository checklist.

## Required Notebooks

- `notebooks/module9_neon_sql_fundamentals_guided_lab.ipynb`
- `notebooks/module10_sql_joins_abt_guided_lab.ipynb`

Module 10 also introduces DuckDB, which runs SQL on your own data (Pandas DataFrames and CSV files) without a database server.

## Project SQL Guide (Not Graded)

- `notebooks/module10_part2_project_sql_options.ipynb`

The project requires at least one SQL query on your own project data. This notebook shows the two paths: **Path A**, your own free Neon database (upload your tables and query them), and **Path B**, DuckDB on your DataFrames and CSV files. Cells marked `# COPY` can be copied into your project notebook.

## Data and Outputs

- No local data files are required.

Completed outputs belong in `data/processed` and are not included in the template.

Expected outputs:

- `data/processed/destination_delay_summary_module9.csv`
- `data/processed/jfk_destination_reliability_module9.csv`
- `data/processed/preliminary_abt_module10.csv`
- `data/processed/route_month_abt_module10.csv`
- `data/processed/carrier_month_abt_module10.csv` (DuckDB practice file)

## How to Work

1. Create your own GitHub repository from this template.
2. You can work in GitHub Codespaces or in local VS Code. On the UTSA campus network Codespaces may not connect; use the local setup there (see the Canvas page on local setup).
3. Install dependencies with `python -m pip install -r requirements.txt` if working locally.
4. Open the notebooks in the order listed above.
5. Run cells from top to bottom.
6. Complete all `Your Turn`, exercise, checkpoint, and reflection sections.
7. Save your notebooks and required outputs.
8. Submit your GitHub repository link through Canvas.

## Database Note

This assignment uses Neon/Postgres. Use these variable names in `.env`:

- `DATABASE_URL`: the course read-only database. Paste the connection string from the Canvas page "Module 9 Database Connection".
- `PROJECT_DATABASE_URL`: only if you choose Path A for your project. Your own Neon database. See `notebooks/module10_part2_project_sql_options.ipynb`.

`.env` stays on your computer or in your Codespace. It is not saved to GitHub. If you open a new Codespace or clone the repository again, the notebook creates an empty `.env` again; paste the string again. Do not commit `.env`.

## Submit

Submit your GitHub repository link through Canvas before the deadline. Your repository should be public. If your GitHub repository is private, invite the instructor account `zzz1990771` or `zzz1990771@gmail.com` before submitting the link.

If you are using GitHub, a typical commit workflow is:

```bash
git add .
git commit -m "Complete Weeks 9-10 BAN 6003 assignment"
git push
```
