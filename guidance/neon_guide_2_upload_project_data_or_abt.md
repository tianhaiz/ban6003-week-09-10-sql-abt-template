# Neon Student Guide 2: Uploading Project Data or an ABT

**BAN 6003: Data Management and Analytics Integration**

This guide is for later project work, not the required Week 9-10 shared SQL practice. The shared course database is readonly. If you want to upload your own project data or final ABT, use your own database environment unless your instructor gives different instructions.

## Goal

Take a prepared Pandas DataFrame and write it to a Postgres table in your own Neon database.

Good candidates for upload include:

- cleaned project data
- integrated project data
- final ABT
- model-ready table

Do not upload raw or sensitive data unless you have permission and a clear reason.

## Step 1: Prepare Your DataFrame

Load or create the project DataFrame you want to upload:

```python
import pandas as pd

abt = pd.read_csv("../data/processed/final_abt.csv")
abt.head()
```

Check the structure before uploading:

```python
abt.shape
abt.info()
abt.isna().sum()
```

Make sure you can explain what one row represents.

## Step 2: Use Your Own Database Connection

Store your own Neon connection string in `.env`:

```text
DATABASE_URL="postgresql://USER:PASSWORD@HOST/DATABASE?sslmode=require&channel_binding=require"
```

Do not use the shared course readonly connection for project uploads. The shared course connection is for SQL practice only.

Make sure `.env` is listed in `.gitignore`.

## Step 3: Connect from Python

```python
import os
from dotenv import load_dotenv
from sqlalchemy import create_engine, text

load_dotenv()
engine = create_engine(os.getenv("DATABASE_URL"))

with engine.connect() as conn:
    result = conn.execute(text("SELECT 1 AS connection_test;"))
    print(result.fetchall())
```

## Step 4: Choose a Clear Table Name

Use lowercase, snake_case, and a descriptive name.

Examples:

```text
project_cleaned_data
project_integrated_data
project_final_abt
```

Avoid vague names such as `data`, `final`, or `table1`.

## Step 5: Upload the DataFrame

```python
abt.to_sql(
    name="project_final_abt",
    con=engine,
    schema="public",
    if_exists="replace",
    index=False,
    chunksize=5000
)
```

For most project checkpoints, `if_exists="replace"` is easiest because it overwrites an older version of the same table.

## Step 6: Verify the Upload

Check row count:

```python
pd.read_sql_query("""
SELECT COUNT(*) AS row_count
FROM project_final_abt;
""", engine)
```

Preview rows:

```python
pd.read_sql_query("""
SELECT *
FROM project_final_abt
LIMIT 5;
""", engine)
```

Check columns and database data types:

```python
pd.read_sql_query("""
SELECT column_name, data_type
FROM information_schema.columns
WHERE table_name = 'project_final_abt'
ORDER BY ordinal_position;
""", engine)
```

## Step 7: Document the Upload

In your project notebook or report, write a short note:

- What table did you upload?
- What does one row represent?
- How many rows and columns were uploaded?
- Did the database row count match the local DataFrame?
- What assumptions or limitations should the instructor know?

Example:

> I uploaded my final ABT to Neon as `project_final_abt`. One row represents one customer. The local DataFrame had 2,431 rows and 38 columns, and the Neon table row count matched after upload.

## Common Mistakes

- Trying to upload to the shared readonly course database.
- Uploading raw data instead of prepared project data.
- Forgetting what one row means.
- Committing `.env` to GitHub.
- Not verifying row counts after upload.
