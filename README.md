# `dbt-test-project`

Following [StartDataEngineering tutorial](https://www.startdataengineering.com/post/dbt-data-build-tool-tutorial/), this project contains the code needed to run dbt using poetry as dependency manager.

## Pre requisites

Tools you need to have installed in order to use the code in this repo:
1. Docker
1. Docker compose
1. Poetry

## Installation

To use the code in this repo, you'll need to:
1. Install the dependencies needed with `poetry install` 
1. Build and run the containers with `docker-compose up --build` or `docker compose up --build` (this will depend on your docker's version).
1. Run `dbt snapshot`
1. Run `dbt run`.

And there you go! 🟢

## What is dbt?

dbt enables data practitioners to adopt software engineering best practices and deploy modular, reliable analytics code. Basically it's a transformation workflow, that uses SQL statements. It allows to create complex models, use variables and macros (similar to functions), run tests, generate documentation, and many more features.

dbt does not extract or load data, but it's powerful at transforming data that's already available in the database. 

## Basics 

There are three main things to know about in order to use the dbt tool:
1. dbt project
1. database connection
1. dbt commands

### dbt project

A dbt project is a directory containing `.sql` and `.yml` files. The minimun required files are:
* A project file named `dbt_project.yml`: this file contains configurations of a dbt project.
* Model(s) which are `.sql` files: a model in dbt is simple a single `.sql` file containing a single select statement.

Every dbt project needs a `dbt_project.yml` file since this is how dbt will know a directory is a dbt project. It also contains important information that tells dbt how to operate on the project.

More information about dbt projects can be found at: [dbt project](https://docs.getdbt.com/docs/introduction#dbt-projects)

### dbt commands

All dbt commands start with `dbt` and can be executed using the CLI. Some commands are:
* `dbt init`
* `dbt run`
* `dbt test`
* `dbt docs generate`
