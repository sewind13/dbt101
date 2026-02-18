# dbt101

A concise learning guide for dbt (data build tool). This repository contains notes,
exercises, and recommended next steps to learn dbt fundamentals and best practices.

## Overview

dbt helps analytics engineers transform data in the warehouse using SQL and
software engineering best practices. This guide walks through core concepts,
practical exercises, and resources to become productive with dbt.

## Prerequisites

- Basic SQL knowledge
- Git and GitHub familiarity
- A data warehouse (e.g., Postgres, BigQuery, Redshift, Snowflake)
- Python 3.8+ (for `dbt-core` installs)

## Quick setup (macOS)

Create and activate a virtual environment, then install dbt for your adapter:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
# Example for Postgres
pip install dbt-postgres
```

Initialize a new dbt project:

```bash
mkdir my_dbt_project && cd my_dbt_project
dbt init my_dbt_project
```

Configure your `profiles.yml` with connection details to your warehouse.

## Suggested learning path

1. Basics
	- Create simple models in `models/`
	- Run `dbt run` and `dbt test`
	- Use `ref()` and understand model compilation
2. Materializations
	- Learn `view`, `table`, and incremental strategies
3. Testing & Documentation
	- Add schema tests, custom tests, and document models with `docs` blocks
	- Run `dbt docs generate` and `dbt docs serve`
4. Macros & Jinja
	- Write reusable SQL with macros and Jinja templating
5. Sources, Seeds & Snapshots
	- Declare sources, use `seeds/`, and capture slowly changing data with snapshots
6. CI/CD & Packaging
	- Automate dbt runs in CI, publish docs, and use packages

## Exercises (practical)

- Exercise 1: Build a staging model that selects and casts raw columns
- Exercise 2: Add tests for nulls and uniqueness on key columns
- Exercise 3: Create a documented analytics model and generate docs

## Resources

- Official docs: https://docs.getdbt.com/
- dbt Learn: https://learn.getdbt.com/
- dbt Slack and community forums

## Contributing

Add exercises, sample queries, or example `profiles.yml` (without secrets).
Open issues or submit PRs for improvements.

---

If you'd like, I can add a sample `profiles.yml` template, example exercises,
or a small demo project inside this repo. Which would you prefer next?
