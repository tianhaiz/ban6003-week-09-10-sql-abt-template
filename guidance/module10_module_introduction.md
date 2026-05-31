# Module 10 Introduction: SQL Joins and ABT Preparation

Last week, you learned basic SQL for querying one table. This week, you use SQL joins, CTEs, and aggregation to begin preparing analysis-ready tables. The central concept is the Analytic Base Table, or ABT.

An ABT is not just a wide table with many columns. A good ABT has a clear unit of analysis, key columns that define one row, useful feature columns, and, when appropriate, a target variable. Before writing joins, you should be able to answer: what should one row mean?

## This Week You Will

- explain the purpose and structure of an ABT;
- use `INNER JOIN` and `LEFT JOIN`;
- use SQL aliases and simple CTEs with `WITH`;
- aggregate lower-level records before joining;
- build a preliminary one-row-per-entity ABT;
- read SQL results into Pandas;
- check duplicate keys, missing values, and possible leakage.

## Lab Focus

The lab connects to Neon and uses SQL to join flights with related lookup tables. You will build preliminary ABTs at levels such as carrier-month, route, or flight, then run basic checks to see whether the table matches its intended structure.

## Project Connection

Project Milestone 2 is due around this module and focuses on data integration and transformation. Use this week to make sure your project has a clear intended unit of analysis and a preliminary ABT or ABT design.

## Key Habit

Choose the unit of analysis first. Then aggregate, join, and check the data to match that unit.
