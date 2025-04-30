# Azure Data Warehouse Integration Framework

## 🚀 Project Overview
This project demonstrates a real-world Azure-based data warehouse integration scenario. It connects on-premise systems (SITS, iTrent) to Azure using Azure Data Factory and a metadata-driven control database, structured in a Medallion architecture (Staging → Enterprise → Presentation). Power BI connects to the Presentation layer for reporting.

## 🎯 Objectives
- Integrate hybrid (on-premise and cloud) data sources securely.
- Build a scalable and metadata-driven ETL framework using ADF.
- Design a modular Medallion architecture for clarity and maintainability.
- Enable robust monitoring and logging.
- Deliver actionable insights in Power BI.

## 🧱 Architecture Overview
![architecture](architecture/medallion_architecture.png)

## 🧩 Layers Description
1. **Staging Layer**: Raw import from source systems.
2. **Enterprise Layer**: Cleaned, joined, business logic applied via stored procedures.
3. **Presentation Layer**: Optimized for reporting with dimensions and facts.

## 🗂️ Control Database
- Manages metadata for all ETL processes.
- Tables:
  - `SourceSystems`
  - `StagingMapping`
  - `EnterpriseMapping`
  - `PresentationMapping`
  - `ETL_Log`

## ⚙️ Tools & Tech
- **Azure Data Factory** (ETL orchestration)
- **Azure SQL Database / Synapse** (Warehouse)
- **Azure Key Vault** (Credential management)
- **Power BI** (Reporting)

## 🧪 Logging & Monitoring
The `ETL_Log` table tracks each load's status, timestamps, and errors for auditability and retry logic.

## 📊 Power BI Model
![powerbi_model](powerbi/data_model_description.md)

## 👷 Contributor
- **Deepak** – Data Warehouse Specialist & Consultant
