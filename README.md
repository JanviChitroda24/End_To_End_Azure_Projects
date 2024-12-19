
# Azure End-to-End Data Engineering Project

## Project Overview
This project demonstrates the implementation of a modern end-to-end data pipeline leveraging Microsoft Azure's cloud ecosystem. It showcases how to efficiently manage data through its lifecycle, starting from ingestion to reporting, while ensuring scalability, security, and cost optimization.

The solution is designed for scenarios requiring large-scale data processing, transformation, and visualization, using a **lakehouse architecture** with **Bronze**, **Silver**, and **Gold** layers.

---

## Objectives
1. Automate data ingestion from an on-premises SQL Server database to the cloud.
2. Perform data transformations to clean, enrich, and prepare data for analysis.
3. Enable cost-effective, scalable querying and reporting using serverless solutions.
4. Provide actionable insights through interactive dashboards in Power BI.

---

## Architecture
The pipeline consists of the following key stages:

### 1. **Data Ingestion**
Data is extracted from an on-premises SQL Server database using **Azure Data Factory (ADF)** and loaded into the **Bronze Layer** of **Azure Data Lake Gen2**.

### 2. **Data Transformation**
Data flows through three distinct layers managed by **Azure Databricks**:
- **Bronze Layer:** Raw data ingested as-is from the source system.
- **Silver Layer:** Semi-cleaned data with minimal transformations (e.g., renaming columns, standardizing formats).
- **Gold Layer:** Fully enriched and analytics-ready data for reporting.

### 3. **Data Loading**
The Gold Layer is queried directly by **Azure Synapse Analytics** using a serverless SQL pool, enabling fast and cost-efficient analysis.

### 4. **Reporting**
**Power BI** connects to Azure Synapse Analytics to build interactive dashboards, providing visual insights into the data.

### 5. **Security and Governance**
**Azure Active Directory** and **Azure Key Vault** are used for secure access management and credential storage.

---

## Technology Stack
- **Azure Data Factory:** For Extract, Transform, Load (ETL) operations.
- **Azure Data Lake Gen2:** Cloud-based storage for the lakehouse architecture.
- **Azure Databricks:** High-performance data analytics and transformation.
- **Azure Synapse Analytics:** Serverless SQL for querying structured data.
- **Power BI:** Data visualization and interactive reporting.
- **Azure Active Directory & Azure Key Vault:** Security, authentication, and secret management.

---

## Pipeline Flow
The data pipeline follows this sequence:

1. **On-Premises SQL Server Database:** Source of truth for raw transactional data.
2. **Azure Data Factory:** Ingests raw data into the **Bronze Layer** in Azure Data Lake Gen2.
3. **Azure Databricks:**
   - Transforms Bronze data into the **Silver Layer** (cleaned).
   - Further enriches Silver data into the **Gold Layer** (analytics-ready).
4. **Azure Synapse Analytics:** Directly queries data from the Gold Layer for efficient analysis.
5. **Power BI:** Connects to Azure Synapse to build dashboards and reports.

---

## Highlights
- **Layered Approach:** Data is processed incrementally across **Bronze**, **Silver**, and **Gold** layers, ensuring clean and structured data.
- **Delta Lake Format:** Data is stored in Delta format, enabling versioning and ACID transactions.
- **Cost Efficiency:** Serverless SQL pools in Synapse reduce storage and compute costs.
- **Security:** Integration with Azure Active Directory and Key Vault ensures secure access to resources.

---

## Getting Started

### Prerequisites
1. Active Azure subscription with required permissions.
2. On-premises SQL Server database (e.g., AdventureWorksLT2017).
3. Power BI Desktop installed locally.


## Contact
For any questions or support, please contact [Janvi Chitroda](mailto:janvichitroda0824@gmail.com).

---
 