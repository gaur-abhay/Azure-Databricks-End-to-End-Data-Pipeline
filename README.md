# Azure Databricks End-to-End Data Pipeline

## Overview

This project demonstrates an **end-to-end data pipeline** built using **Azure Databricks**, following the **Medallion Architecture (Bronze, Silver, Gold)**.
The goal of this project is to showcase how raw data can be incrementally ingested, transformed, governed, and prepared for analytics using modern data engineering practices.

The implementation focuses on **clarity, structure, and governance**, rather than large-scale data volumes.

---

## Architecture

The pipeline is designed using the **Medallion Architecture** pattern:

* **Bronze Layer** – Raw data ingestion
* **Silver Layer** – Cleansed and transformed data
* **Gold Layer** – Analytics-ready data

Data flows from ingestion to consumption in a structured and layered manner.

---

## Key Components

### Azure Databricks

* Used as the core processing platform
* Handles data ingestion, transformation, and pipeline execution

### Azure Data Lake Storage

* Serves as the central storage layer
* Stores data in **Parquet format**

### Auto Loader (Bronze Layer)

* Enables **incremental data ingestion**
* Automatically detects and processes new files
* Ensures efficient ingestion without reprocessing existing data

### PySpark Transformations

* Applied basic transformations to clean and prepare data
* Used across Silver and Gold layers

### Unity Catalog

* Used for **data organization and governance**
* Data structured using:

  * Metastore (top-level container)
  * Catalogs
  * Schemas (databases)
  * Tables and views

---

## Data Flow

1. Raw data is ingested incrementally into the **Bronze layer** using Auto Loader
2. Data is transformed and cleaned in the **Silver layer** using PySpark
3. Curated datasets are produced in the **Gold layer** for analytics
4. Unity Catalog manages metadata, structure, and access across all layers

---

## Technologies Used

* Azure Databricks
* Apache Spark (PySpark)
* Medallion Architecture
* Databricks Auto Loader
* Unity Catalog
* Azure Data Lake Storage
* Parquet

---

## Project Scope

* Small dataset with simple transformations
* Focused on understanding:

  * End-to-end pipeline design
  * Incremental ingestion
  * Layered data architecture
  * Basic data governance concepts

This project is intended for **learning and demonstration purposes**.

---

## Key Learnings

* Designing layered data pipelines using Medallion Architecture
* Implementing incremental ingestion using Auto Loader
* Applying basic transformations with PySpark
* Organizing and governing data using Unity Catalog



