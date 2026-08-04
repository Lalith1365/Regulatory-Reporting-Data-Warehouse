------------------------------------------------------
🚀 Regulatory Reporting & Core Banking Data Warehouse
------------------------------------------------------

[Python] [PySpark] [Databricks] [Delta Lake] [Spark SQL]

## 📌 Overview

This project demonstrates an end-to-end **Regulatory Reporting & Core Banking Data Warehouse** built using **Databricks, PySpark, Delta Lake, and Spark SQL**.

The solution follows the **Medallion Architecture (Bronze, Silver, Gold)** to simulate how financial institutions process banking transactions for regulatory reporting and analytics.

The pipeline ingests raw banking transactions, validates and cleans the data, quarantines invalid records, enriches transactions with AML (Anti-Money Laundering) risk classifications, detects suspicious and high-value transactions, and generates business-ready reporting tables.

### Key Features

- 🥉 Bronze Layer for raw transaction ingestion
- 🥈 Silver Layer for data validation, cleansing, and enrichment
- 🛑 Quarantine table for invalid transactions
- 🛡️ AML risk classification based on counterparty country
- 💰 Large transaction and suspicious transaction detection
- 🔄 Incremental data loading using Delta Lake
- 🔀 MERGE (UPSERT) for efficient updates
- 🥇 Gold Layer for regulatory reporting, customer summaries, and data quality metrics
- 📊 Analytics-ready tables for dashboards and reporting

🏗 Architecture
Core Banking System
        │
        ▼
 Bronze Layer
        │
        ▼
 Silver Layer
 ├── Validation
 ├── AML
 ├── Large Transactions
 ├── Suspicious Transactions
        │
        ▼
 Gold Layer
 ├── Reporting
 ├── Customer Summary
 └── Metrics
        │
        ▼
 Dashboard

### Technologies Used

- 🐍 Python
- ⚡ Apache Spark (PySpark)
- 🗄️ Spark SQL
- 🔺 Delta Lake
- 🧱 Databricks
- 🌿 Git
- 📂 GitHub

## ✨ Core Concepts Demonstrated

- ETL Pipeline Development
- Medallion Architecture
- Delta Lake Tables
- Data Validation
- Quarantine Handling
- AML Risk Classification
- Suspicious Transaction Detection
- Incremental Data Loading
- Delta Lake MERGE (UPSERT)
- Regulatory Reporting
- Data Quality Monitoring

## 📂 Project Workflow

The project follows the **Medallion Architecture (Bronze → Silver → Gold)** to process core banking transactions.

### Step 1: Data Ingestion (Bronze Layer)
- Simulated raw banking transaction data using PySpark.
- Stored raw records in a Delta table without modifications.
- Preserved all incoming data for traceability and auditing.

⬇️

### Step 2: Data Validation & Cleansing (Silver Layer)
- Read transactions from the Bronze layer.
- Validated mandatory fields (e.g., Account ID and Transaction Amount).
- Moved invalid or corrupted records to a Quarantine table.
- Cast data types and standardized timestamps.

⬇️

### Step 3: Data Enrichment
- Classified transactions into **HIGH** or **LOW** AML risk tiers based on counterparty country.
- Flagged transactions greater than or equal to **$1,000,000**.
- Detected suspicious transactions using business rules.

⬇️

### Step 4: Incremental Processing
- Simulated arrival of new banking transactions.
- Appended new data to the Bronze layer.
- Processed only new records.
- Used **Delta Lake MERGE (UPSERT)** to update the Silver layer efficiently.

⬇️

### Step 5: Gold Layer Reporting
Generated business-ready reporting tables:

- 📊 Regulatory Reporting
- 👤 Customer Summary
- ✅ Data Quality Metrics

⬇️

### Step 6: Analytics
The Gold layer serves as the source for dashboards and business reporting.

## 🥉 Bronze Layer

- Ingested raw core banking transactions into a Delta table.
- Preserved original data without transformations.
- Served as the source for downstream processing.

## 🥈 Silver Layer

- Validated mandatory fields.
- Quarantined invalid records.
- Added AML risk classification.
- Flagged large and suspicious transactions.

## 🥇 Gold Layer

Generated analytics-ready tables:

- Regulatory Reporting
- Customer Summary
- Data Quality Metrics

## 📊 Results

The project successfully demonstrates an end-to-end regulatory reporting data warehouse using the Medallion Architecture.

### Achievements

- ✅ Built a complete **Bronze → Silver → Gold** data pipeline using Databricks and Delta Lake.
- ✅ Ingested and processed simulated core banking transaction data.
- ✅ Implemented data quality validation with quarantine handling for invalid records.
- ✅ Enriched transactions with **AML risk classification** based on counterparty country.
- ✅ Flagged **large-value** and **suspicious** transactions using business rules.
- ✅ Implemented **incremental data loading** and **Delta Lake MERGE (UPSERT)** operations.
- ✅ Generated Gold-layer business tables for:
  - Regulatory Reporting
  - Customer Summary
  - Data Quality Metrics
- ✅ Produced analytics-ready datasets for dashboards and reporting.

📷 Screenshots

🚀 Future Improvements
