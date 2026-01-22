# Banking Transactions Data Pipeline (Spark + Databricks)

## Overview
This project implements an end-to-end data pipeline using **Apache Spark on Databricks** to process banking transaction data.  
The pipeline follows an **enterprise-style Bronze–Silver–Gold architecture** and uses **Delta Lake** for reliable and scalable data storage.

The project focuses on **data quality, transformation, analytics, and governance**, reflecting real-world data engineering and data analytics workflows used in banking and financial services.

---

## Architecture
The pipeline is designed using the Bronze–Silver–Gold pattern:

- **Bronze Layer**  
  Stores raw, unmodified transaction data for auditability and traceability.

- **Silver Layer**  
  Stores cleaned and validated data after handling missing values, duplicates, and invalid records.  
  Data is persisted in **Delta format** to ensure reliability and ACID compliance.

- **Gold Layer**  
  Stores aggregated, analytics-ready datasets used for reporting and business insights.

- **Data Quality Summary**  
  Captures key data quality metrics to support governance and monitoring.

---

## Technologies Used
- Apache Spark (PySpark)
- Databricks
- Delta Lake
- Spark SQL
- Python

---

## Project Structure

```text
banking-transactions-spark-databricks/
│
├── notebook/
│   └── banking_transactions_spark_pipeline.ipynb
│
├── data/
│   └── raw/
│       └── transactions.csv
│
├── architecture/
│   └── bronze_silver_gold_architecture.png
│
└── requirements.txt
```


---

## Key Features
- Data ingestion with schema inference
- Data quality checks (null detection, duplicate detection, invalid value checks)
- Data cleaning and business rule validation
- Bronze–Silver–Gold data layering
- Delta Lake storage for reliable data management
- Analytics using Spark SQL
- Data quality summary for governance and controls

---

## Data Quality Rules Implemented
- Missing values handled with default values
- Duplicate transactions removed using transaction ID
- Negative transaction amounts corrected based on business rules
- Data quality metrics captured for monitoring

---

## Output Data (Generated in Databricks)
- **Bronze Data**: Raw transaction data (CSV)
- **Silver Data**: Cleaned and validated data (Delta format)
- **Gold Data**: Aggregated analytics-ready data (Delta format)
- **Data Quality Summary**: Governance metrics stored as Delta tables

> Note: Output data is generated dynamically in Databricks and is not committed to GitHub, following industry best practices.

---

## How to Run the Project
1. Upload the notebook to Databricks
2. Upload the raw dataset (`transactions.csv`) to DBFS
3. Run the notebook from top to bottom
4. Outputs will be created in Bronze, Silver, and Gold layers within Databricks

---

## Use Case
This project is designed to simulate real-world banking transaction processing, focusing on:
- Data reliability
- Reporting readiness
- Governance and controls
- Scalable analytics using Spark

---

## Key Learning Outcomes
- Hands-on experience with Apache Spark and Databricks
- Understanding of enterprise data architecture patterns
- Implementation of data quality and governance concepts
- Use of Delta Lake for reliable data pipelines
- Building analytics-ready datasets for business reporting
