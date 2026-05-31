# Neon Student Guide 1: Registration, Basic Navigation, and Shared Course Database

**BAN 6003: Data Management and Analytics Integration**

This guide explains what Neon is, how to create or access a Neon account, and how the course shared database works. For the Week 9-10 SQL labs, you do **not** need to create your own database or upload the NYC flights data. Your instructor has already prepared the course database.

## What Is Neon?

Neon is an online Postgres database platform. In this course, we use Neon so you can practice working with a real relational database instead of only local CSV files or Pandas DataFrames.

You will use Neon in two ways:

1. **Shared course database for SQL practice**: the instructor provides a readonly connection for tables such as `flights`, `airlines`, `airports`, `planes`, and `weather`.
2. **Project database workflow later**: you may choose to upload your own project data or ABT to a database after you prepare it.

## Do You Need a Neon Account for Week 9?

For the required Week 9-10 SQL labs, no. You will query the instructor's shared readonly database from the notebook.

Creating a Neon account is useful if you want to explore the web interface or later upload your own project data. If your instructor has not asked you to create your own project database, do not create or upload course practice tables yourself.

## Optional: Create or Access a Neon Account

Go to:

`https://neon.com`

Click **Sign Up** or **Log In**. You may sign up with GitHub, Google, or an email address. Use an account you can access throughout the semester.

After signing in, you should see the Neon Console. This is the web interface where projects, databases, branches, SQL editor tools, and connection details are managed.

## Basic Terms

- **Project**: a workspace that contains database resources.
- **Database**: where tables are stored.
- **Branch**: a database branch. For this course, use the default branch unless told otherwise.
- **SQL Editor**: a browser-based place to run SQL queries.
- **Connection string**: a credential string used by Python, notebooks, or SQL tools to connect to a database.

## How the Shared Course Database Works

The Week 9-10 assignment repository includes a file named:

`.env.example`

The notebook setup cell copies it to:

`.env`

The `.env` file stores `DATABASE_URL`, which points to the shared readonly course database. Do not print the full connection string, post it publicly, or commit `.env` to GitHub.

The readonly database lets you run SQL queries such as:

```sql
SELECT *
FROM flights
LIMIT 5;
```

It does not let you create, replace, or delete tables. That is intentional. The shared course database is for practice queries.

## If the Connection Does Not Work

Check the following:

- Did you run the notebook setup cell that creates `.env` from `.env.example`?
- Are you working in your assignment repository, not the template repository?
- Did you avoid editing or deleting `DATABASE_URL`?
- Did you restart the notebook kernel after changing `.env`?
- Did GitHub Codespaces finish installing the required packages?

If the problem continues, share the error message with your instructor, but do not share the full connection string publicly.
