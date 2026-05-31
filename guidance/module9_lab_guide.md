# Module 9 Lab Guide: Database Setup and SQL Fundamentals

**BAN 6003: Data Management and Analytics Integration**

This module introduces Neon Postgres and basic SQL. You will connect to the shared course database, explore available tables, write single-table SQL queries, and compare SQL outputs with Pandas.

SQL joins and ABT construction come next. This module focuses on becoming comfortable with one table at a time.

## Lab File

Complete:

`module9_neon_sql_fundamentals_guided_lab.ipynb`

## GitHub Repository and Running Environment

Start from this public template repository:

https://github.com/tianhaiz/ban6003-week-09-10-sql-abt-template

Create your own GitHub repository from the template with **Use this template > Create a new repository**. I recommend making your repository public so the instructor can inspect your submission. If you use a private repository, invite the instructor GitHub account `zzz1990771` or the email `zzz1990771@gmail.com` as a collaborator.

You may run the lab in either environment:

- **Main path, recommended for beginners:** GitHub Codespaces from your own repository.
- **Optional path for technically experienced students:** clone your own repository, activate the `ban6003` conda environment, install `requirements.txt`, and run JupyterLab locally.

Submit your GitHub repository link through Canvas.

## Required Setup

The assignment repository includes a readonly course database connection in `.env.example`. In the notebook, run the setup cell under **Create your local `.env` file from the provided template**. It copies:

```bash
.env.example -> .env
```

Do not commit `.env` to GitHub. The repository is already configured to ignore it.


## What You Will Practice

You will practice connecting to Neon, listing tables, using `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`, aggregate functions, `GROUP BY`, reading SQL results into Pandas, and reviewing the project database workflow.

## Recommended Workflow

1. Open the notebook in Codespaces, or in local Jupyter if you are using the optional local path.
2. Run the setup cell that creates `.env`.
3. Run the package import and connection cells.
4. Work through each SQL section.
5. Complete all Your Turn tasks.
6. Complete the final practice query and reflection.
7. Save your work, then commit and push if using GitHub.

## Minimum Completion Checklist

Before submitting, make sure:

- Your database connection works.
- You listed available tables.
- You used `SELECT`, `WHERE`, `ORDER BY`, and `LIMIT`.
- You used aggregate functions and `GROUP BY`.
- You completed the Your Turn sections.
- You did not commit `.env`.
