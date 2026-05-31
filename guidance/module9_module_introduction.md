# Module 9 Introduction: Database Setup and SQL Fundamentals

Up to this point, most of our work has happened in notebooks with Pandas. This week, we begin working with databases and SQL. In real organizations, important data usually does not live only in one notebook. It often lives in shared, persistent database systems.

This module introduces Neon, an online Postgres database environment, and basic single-table SQL. The goal is to become comfortable connecting to a database, inspecting available tables, writing simple queries, and comparing SQL results with Pandas outputs.

## This Week You Will

- connect to the course Neon database from GitHub Codespaces;
- protect your database connection string using a `.env` file;
- list available database tables;
- use `SELECT`, `WHERE`, `ORDER BY`, and `LIMIT`;
- use aggregate functions such as `COUNT`, `AVG`, `SUM`, `MIN`, and `MAX`;
- use `GROUP BY` for grouped summaries;
- read SQL query results into Pandas.

## Important Boundary

This module focuses on single-table SQL. SQL joins and ABT construction come next. For now, build confidence with clear, readable queries that answer simple questions.

## Lab Focus

You will query course database tables, inspect the flights data, summarize records, compare SQL and Pandas approaches, and review a template for uploading or preparing project data in Neon.

## Project Connection

Neon will also serve as a project database environment. This week prepares you to store, query, and validate project data in a more realistic workflow. Do not commit your `.env` file to GitHub.
