# Project Architecture Blueprint

## Goal

The eventual learning project will model basic operations and reporting for a
retail business. This is a blueprint, not a claim that cloud resources or
application components have already been built.

## High-level flow

1. Retail business data (for example, orders and products) is the source.
2. Small Python programs will validate and transform sample data.
3. PostgreSQL will provide a local relational database for SQL practice.
4. Simple queries and reports will make the processed data useful.
5. Later learning modules may map these concepts to Azure services after the
   local foundations are understood.

## Current boundary

Only the local workspace, editor settings, Python environment, and local Git
repository are in scope for the initial foundation. No application, database,
cloud resource, or data pipeline is created by this blueprint.

## Design principles

- Keep project files isolated under this directory.
- Keep credentials out of source control.
- Use a project-local Python virtual environment.
- Prefer small, testable steps and document what has actually been verified.
- Do not alter the existing PostgreSQL service or its port as part of this
  setup.
