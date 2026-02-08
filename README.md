# 🏥 End-to-End Hospital Admission Data Pipeline (Azure) Project Overview

 Project Overview
This project demonstrates an end-to-end Data Engineering pipeline built on Microsoft Azure, focusing on COVID-19 hospital and ICU admission data.
The main objective is to ingest raw data from multiple sources, transform and model it efficiently, and deliver analytics-ready datasets that can be directly used for reporting, advanced analytics, or BI tools.
This project is designed to simulate real-world data engineering scenarios, emphasizing scalability, automation, and data quality.

# 🏗️ Solution Architecture

The architecture follows a modern cloud-based data engineering design using layered storage and automated pipelines.

 # Architecture Diagram
![covid -19](https://github.com/user-attachments/assets/31228fb7-ccb8-483f-bd0f-e9e4c530d83e)
High-level flow:
External data sources (API & Blob Storage)
Azure Data Factory for ingestion & orchestration
Azure Data Lake Gen2 (Raw & Curated layers)
Azure SQL Database as a serving layer
Data ready for analytics & dashboarding

 
 # Data Sources
COVID-19 Hospital Admission Data
Source: ECDC (via HTTP API)

Population Data
Source: Azure Blob Storage

#  Data Ingestion

Data ingestion is handled using Azure Data Factory (ADF).
HTTP Connector is used to pull COVID-19 data from ECDC
Population data is ingested from Azure Blob Storage
Pipelines are designed to support automated and repeatable loads


# 🧹 Data Transformation (Processing)

All transformations are implemented using Azure Data Factory – Mapping Data Flows.
Key transformation steps include:
Data cleansing and standardization
Schema mapping
Handling daily vs weekly datasets
Date transformations (Year–Week logic)
Lookup transformations:
Country codes (ISO)
Population data

# 📷 Mapping Data Flow

![hospital admission](https://github.com/user-attachments/assets/8db7499c-bd93-4347-b619-90fced4c7ba2)
![cases and deaths](https://github.com/user-attachments/assets/26535321-8a5e-4324-a9ba-bf657bf22ec4)

# 🧱 Data Modeling

The transformed data is modeled into analytics-ready tables optimized for querying and reporting.
Final datasets include:
Daily Hospital & ICU Occupancy
Weekly New Hospital & ICU Admissions
The data model supports:
Fast analytical queries
Easy integration with BI tools
Downstream advanced analytics or ML use cases

# 🗄️ Serving Layer

Final curated datasets are loaded into Azure SQL Database
Schemas are optimized for analytical workloads
Data is fully prepared for:
Power BI dashboards
Ad-hoc SQL analysis
Further data science workloads

# 🛠️ Tech Stack
Azure Data Factory (Pipelines & Mapping Data Flows)
Azure Data Lake Storage Gen2
Azure Blob Storage
Azure SQL Database
HTTP API Integration
SQL

# 👤 Author

Dina
Data Analyst
Feel free to connect or provide feedback 🙌

 
