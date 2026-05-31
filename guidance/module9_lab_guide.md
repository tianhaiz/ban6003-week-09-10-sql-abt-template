# Module 9 Lab Guide: Database Setup and SQL Fundamentals

**BAN 6003: Data Management and Analytics Integration**

This module introduces Neon Postgres and basic SQL. You will connect to the shared course database, explore available tables, write single-table SQL queries, and compare SQL outputs with Pandas.

SQL joins and ABT construction come next. This module focuses on becoming comfortable with one table at a time.

## Lab File

Complete:

`module9_neon_sql_fundamentals_guided_lab.ipynb`

## Required Setup

The assignment repository includes a readonly course database connection in `.env.example`. In the notebook, run the setup cell under **Create your local `.env` file from the provided template**. It copies:

```bash
.env.example -> .env
```

Do not commit `.env` to GitHub. The repository is already configured to ignore it.

## GitHub Classroom Assignment Link

Canvas will provide the GitHub Classroom invitation link for this Module 9-10 assignment package:

**GitHub Classroom invitation link:** [to be added]

Click the invitation link, sign in to GitHub, and accept the assignment. If this is your first GitHub Classroom assignment for the course, GitHub may ask you to authorize GitHub Classroom and match your GitHub account to the course roster. Choose your own name or identifier carefully.

After you accept, wait for GitHub Classroom to create your personal assignment repository. Open the repository link shown on the confirmation page. If you see a repository access message, check the GitHub notifications inbox in the upper-right corner of GitHub, or go to `https://github.com/notifications`, and accept any pending repository or organization invitation from GitHub Classroom. You may also receive an email from GitHub with the same invitation.

Once you can see your personal assignment repository, open it in Codespaces with **Code > Codespaces > Create codespace on main**.

## What You Will Practice

You will practice connecting to Neon, listing tables, using `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`, aggregate functions, `GROUP BY`, reading SQL results into Pandas, and reviewing the project database workflow.

## Recommended Workflow

1. Open the notebook in GitHub Codespaces.
2. Run the setup cell that creates `.env`.
3. Run the package import and connection cells.
4. Work through each SQL section.
5. Complete all Your Turn tasks.
6. Complete the final practice query and reflection.
7. Save, commit, and push your work.

## Minimum Completion Checklist

Before submitting, make sure:

- Your database connection works.
- You listed available tables.
- You used `SELECT`, `WHERE`, `ORDER BY`, and `LIMIT`.
- You used aggregate functions and `GROUP BY`.
- You completed the Your Turn sections.
- You did not commit `.env`.
