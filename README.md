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

⚙ Technologies

📂 Project Workflow

🥉 Bronze Layer

🥈 Silver Layer

🥇 Gold Layer

📊 Results

📷 Screenshots

🚀 Future Improvements
