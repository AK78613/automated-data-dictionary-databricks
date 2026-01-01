# automated-data-dictionary-databricks
# Automated Data Dictionary using Databricks & PySpark

## Overview
This project demonstrates an automated approach to managing
table and column-level metadata in Databricks using PySpark.
The solution dynamically extracts table schemas and applies
documentation programmatically.

## Problem
Data documentation is often manual and quickly becomes outdated.
This project keeps documentation close to the data by embedding
metadata directly into Spark tables.

## Architecture
- Business tables: weather_raw, station_info
- Metadata source: metadata_definitions (managed Spark table)
- Automation engine: PySpark + Spark SQL

## Workflow
1. Create business tables
2. Extract schema metadata using DESCRIBE TABLE
3. Store metadata definitions centrally
4. Apply column-level documentation automatically

## Tech Stack
- Python
- Apache Spark (PySpark)
- Databricks
- Spark SQL

## End-to-End Testing
- Reset column comments
- Run metadata automation
- Verify via DESCRIBE EXTENDED
- Update metadata definitions and re-run automation

## Notes
Due to Databricks Free Edition constraints, metadata definitions
are stored as managed Spark tables.
