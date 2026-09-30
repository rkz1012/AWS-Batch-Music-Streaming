# Batch Music Streaming Data Pipeline

An end-to-end batch data engineering pipeline for processing music streaming data using **Amazon S3, Apache Airflow, Python, SQL, and Amazon Redshift**.

The project demonstrates how raw music streaming data can be ingested, processed, transformed, and loaded into a cloud data warehouse for analytical workloads. Apache Airflow is used to orchestrate the pipeline and manage task dependencies.

---

## Architecture

```text
                    Music Streaming Data
                            |
                            v
                     +-------------+
                     |  Amazon S3  |
                     +------+------+
                            |
                            v
                     +-------------+
                     |   Airflow   |
                     |     DAG     |
                     +------+------+
                            |
                 +----------+----------+
                 |          |          |
                 v          v          v
              Extract   Transform   Validate
                 |          |          |
                 +----------+----------+
                            |
                            v
                     +-------------+
                     |  Redshift   |
                     | Data Warehouse|
                     +------+------+
                            |
                            v
                    Analytical Queries
