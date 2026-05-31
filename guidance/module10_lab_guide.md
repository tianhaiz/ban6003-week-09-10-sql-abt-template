# Module 10 Lab Guide: SQL Joins and ABT Preparation

**BAN 6003: Data Management and Analytics Integration**

This module moves from basic SQL to SQL-based integration and preliminary ABT construction.

The key question is:

> What should one row mean in the table we prepare for analysis or modeling?

## Lab File

Complete:

`module10_sql_joins_abt_guided_lab.ipynb`

## Required Setup

Use the same shared readonly Neon connection from Module 9. The notebook includes a setup cell that copies `.env.example` to `.env` if needed. Do not commit `.env`.

## GitHub Classroom Assignment Link

This module is part of the Module 9-10 assignment package. Canvas will provide the GitHub Classroom invitation link if you have not already accepted this package:

**GitHub Classroom invitation link:** [to be added]

If you already accepted the Module 9-10 assignment, return to the same personal assignment repository and reopen your Codespace. If the repository does not open or GitHub says you do not have access, check the GitHub notifications inbox in the upper-right corner of GitHub, or go to `https://github.com/notifications`, and accept any pending repository or organization invitation from GitHub Classroom.

## What You Will Practice

You will practice `INNER JOIN`, `LEFT JOIN`, joining the same lookup table more than once, SQL aliases, CTEs with `WITH`, aggregation before joining, route-level or carrier-month ABT construction, and checks for duplicate keys and missing values.

## Recommended Workflow

1. Open the notebook in GitHub Codespaces.
2. Run or confirm the `.env` setup cell.
3. Run the connection setup cells.
4. Complete the SQL join examples.
5. Complete all Your Turn sections.
6. Build a preliminary ABT in the final practice section.
7. Complete the reflection.
8. Save, commit, and push your work.

## What to Pay Attention To

Keep asking what one row means, which keys define one row, whether aggregation should happen before joining, and whether a join could duplicate records.

## Minimum Completion Checklist

Before submitting, make sure:

- Your notebook connects to Neon.
- You ran an inner join and a left join.
- You used at least one CTE.
- You created an aggregated summary before joining.
- You built a preliminary ABT.
- You checked duplicate keys and missing values.
- You completed the data leakage and final reflections.
