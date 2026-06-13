# End-to-End Data Engineering Pipeline using Snowflake, dbt and Apache Airflow

## Project Overview

This project demonstrates the development of an end-to-end ELT (Extract, Load, Transform) pipeline using Snowflake, dbt, and Apache Airflow.

Raw TPCH sample data is transformed through staging, intermediate, and fact layers using dbt. Data quality tests are implemented to ensure reliability, and Apache Airflow orchestrates the entire workflow.

---

## Architecture

TPCH Source Data

↓

Staging Models

↓

Intermediate Models

↓

Fact Table (fct_orders)

↓

Data Quality Tests

↓

Airflow Orchestration

---

## Tech Stack

* Snowflake
* dbt (Data Build Tool)
* Apache Airflow
* Astronomer Astro
* SQL
* Python
* Git & GitHub

---

## Project Structure

```text
airflow_project/
│
├── dags/
│   ├── dbt_dag.py
│   └── data_pipeline/
│
├── screenshots/
│
├── tests/
│
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## Data Models

### Staging Models

* stg_tpch_orders
* stg_tpch_line_items

Purpose:

* Clean raw source data
* Standardize column names
* Prepare data for transformations

### Intermediate Models

* int_order_items
* int_order_items_summary

Purpose:

* Join and aggregate staging data
* Apply business logic

### Fact Model

* fct_orders

Purpose:

* Create analytics-ready datasets for reporting and business analysis

---

## Data Quality Tests

Implemented dbt tests:

### Generic Tests

* not_null
* unique
* relationships
* accepted_values

### Custom Tests

* fct_orders_date_valid
* fct_orders_discount

These tests ensure data accuracy, consistency, and reliability.

---

## Workflow Orchestration

Apache Airflow is used to automate the pipeline execution.

Workflow:

1. Run dbt models
2. Execute data quality tests
3. Monitor pipeline execution

---

## Screenshots

### Airflow DAG Success

See:

`screenshots/airflow_success.png`

### Successful dbt Run

See:

`screenshots/dbt_run_success.png`

### Successful dbt Test

See:

`screenshots/dbt_test_success.png`

### dbt Lineage Graph

See:

`screenshots/dbt_lineage_graph.png`

### Snowflake Tables

See:

`screenshots/snowflake_tables.png`

---

## Key Learnings

* Data Warehousing with Snowflake
* Data Transformation using dbt
* Data Modeling
* Data Quality Testing
* Workflow Orchestration with Airflow
* ELT Pipeline Development
* Git and GitHub Version Control

---

## Author

Naveed Shaikh

GitHub:
https://github.com/naveedshaikh061003-coder
