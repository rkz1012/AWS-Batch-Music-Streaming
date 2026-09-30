# Batch Music Streaming Data Pipeline

## Overview

An end-to-end batch data engineering pipeline for processing music streaming data using Apache Airflow, Amazon S3, Python, SQL, and Amazon Redshift.

The pipeline automates data ingestion, transformation, validation, and loading into Amazon Redshift for analytical workloads.

## Architecture

```text
Music Streaming Data
        |
        v
    Amazon S3
        |
        v
 Apache Airflow
        |
        +-- Extract
        |
        +-- Transform
        |
        +-- Validate
        |
        +-- Load
        |
        v
  Amazon Redshift
        |
        v
 Analytical Queries
