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

## 📷 Screenshots

### Bronze Layer

![Bronze Layer](screenshots/bronze_layer.png)

<img width="1787" height="612" alt="bronze_layer1" src="https://github.com/user-attachments/assets/40bbe2cf-9ec1-4ef1-8062-0e73fa6540b5" />


### Silver Layer

![Silver Layer](screenshots/silver_layer.png)

<img width="2036" height="549" alt="silver_layer2" src="https://github.com/user-attachments/assets/79ce07f6-f8cf-42f7-870c-dfd44e1a91e5" />


### Gold Regulatory Reporting

![Gold Regulatory Reporting](screenshots/gold_reporting.png)

<img width="2014" height="419" alt="gold_reporting3" src="https://github.com/user-attachments/assets/3160f238-84b3-4f5e-9038-35a345bf498a" />


### Customer Summary

![Customer Summary](screenshots/customer_summary.png)

<img width="2036" height="385" alt="customer_summary4" src="https://github.com/user-attachments/assets/b165dd83-418c-47d2-8e6b-d16a0dc0ee12" />


### Data Quality Metrics

![Data Quality Metrics](screenshots/data_quality_metrics.png)

<img width="619" height="390" alt="data_quality_metrics5" src="https://github.com/user-attachments/assets/40960182-66ee-4018-b521-ce514188a61c" />


## 🚀 Future Enhancements

- Real-time transaction processing with Apache Kafka.
- Pipeline orchestration using Apache Airflow or Databricks Workflows.
- Machine learning-based fraud and AML detection.
- Interactive Power BI dashboards.
- Production deployment on AWS or Azure.
