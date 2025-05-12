 📺 Netflix Azure Data Engineering Project
This project showcases the development of a scalable, end-to-end data pipeline using Azure and Databricks, designed to process and analyze Netflix data. Built on the Medallion Architecture (Bronze, Silver, Gold), it leverages modern data engineering tools to ensure automation, scalability, and governance across the pipeline.

🔍 Project Overview
This project demonstrates a robust data engineering pipeline using Azure Data Lake Storage (ADLS) and Azure Databricks, orchestrated through Azure Data Factory (ADF). The pipeline follows the Medallion Architecture, enabling a structured, incremental approach to data ingestion, transformation, and analytics:

Bronze Layer: Raw data ingestion using ADF and Databricks Autoloader

Silver Layer: Data cleaning and standardization with Delta Lake

Gold Layer: Business-level aggregates via Delta Live Tables for insights and reporting

🏗️ Solution Architecture


🔹 Bronze Layer – Raw Data Ingestion
Source: Public GitHub repository containing Netflix data

Tool: Azure Data Factory (ADF)

Storage: Azure Data Lake (Bronze Zone)

Features:

ADF pipelines fetch data from GitHub

Databricks Autoloader handles incremental, schema-aware ingestion

🔸 Silver Layer – Data Transformation
Tool: Azure Databricks with Delta Lake

Storage: ADLS Silver Zone

Features:

Data cleansing and transformation using PySpark

Data stored as optimized Delta Tables

Secure connectivity via Databricks Access Connector

🟡 Gold Layer – Analytics & Reporting
Tool: Delta Live Tables (DLT) on Azure Databricks

Storage: ADLS Gold Zone

Features:

Business-level aggregations and real-time transformations

Data governance with Unity Catalog

Workflow automation using Databricks Workflows

🧰 Technologies Used
Tool/Service	Purpose
Azure Data Lake (ADLS)	Storage for raw, refined, and aggregated data (Bronze/Silver/Gold)
Azure Data Factory (ADF)	Orchestrates ingestion from GitHub to ADLS
Azure Databricks	Performs transformation, analysis, and scheduling
Delta Lake	Enables ACID-compliant, scalable data storage
Delta Live Tables (DLT)	Simplifies real-time data transformation
Databricks Autoloader	Automatically ingests new data files incrementally
Unity Catalog	Centralized governance for data and access control
Databricks Workflows	Automates and schedules pipeline jobs

🚀 Key Features
✅ Fully automated ingestion using ADF and Autoloader
✅ Structured Medallion Architecture: Bronze, Silver, Gold
✅ Near real-time data processing with Delta Live Tables
✅ Job orchestration via Databricks Workflows
✅ Data governance with Unity Catalog

📁 Folder Structure
Folder	Description
Azure/	ADF pipelines and linked services (JSON templates)
Data/	Sample Netflix data files (CSV, JSON)
Databricks_notebooks/	Notebooks for data transformation and analysis (PySpark)
parameter_file/	Parameterization configs for dynamic ADF pipelines
pipelinescreenshots/	Visuals of pipeline architecture, ADF flows, and notebooks

📌 Conclusion
This project highlights best practices in modern data engineering using Azure-native services and Databricks. With scalable architecture, incremental ingestion, and real-time analytics, it serves as a solid reference for building production-grade pipelines in cloud environments.

