# 🚀 Production-Ready E-Commerce ETL Pipeline | PySpark & Databricks

An end-to-end cloud data engineering pipeline built using **PySpark** and **Databricks Serverless** architectures. This project processes raw, messy transnational retail data, implements data quality filters, and surfaces critical business intelligence metrics into high-performance analytical tables.

## 📐 Data Architecture (Medallion Workflow)
* **Bronze Layer:** Ingested raw e-commerce CSV transactional data (~48MB logs) containing formatting anomalies and broken strings into the Unity Catalog database workspace.
* **Silver Layer:** Cleansed data quality anomalies by eliminating record blocks missing primary keys (`CustomerID`), removing structural inventory noise (negative transaction quantities), and engineering a new transaction-level metrics matrix (`TotalSpending`).
* **Gold Layer:** Executed high-performance data aggregations to calculate total lifetime consumer valuation, ordering patterns, and sorting the top revenue-driving clusters. Output layers are fully saved into production-ready **Delta Lake Tables**.

## 🛠️ Tech Stack & Skills Demonstrated
* **Engine Framework:** Apache Spark (PySpark Core API)
* **Environment:** Databricks Serverless Compute / Unity Catalog
* **Storage Optimization:** Delta Lake Tables (ACID transactions, schema enforcement)
* **Key Operations:** Data Transformation, Schema Cleaning, Complex Aggregations, Missing Value Treatment.

## 📊 Sample Output Schema Surface
The pipeline outputs an optimized data layer (`gold_customer_metrics`) ready for streaming analytical dashboards:
* `CustomerID` (Unique identifier string)
* `TotalAmountSpent` (Aggregated continuous consumer financial scale)
* `TotalItemsBought` (Sum total scalar transaction counts)
