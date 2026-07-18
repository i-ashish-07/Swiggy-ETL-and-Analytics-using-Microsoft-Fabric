# Swiggy End-to-End Data Analytics using Microsoft Fabric
Project Overview
This project demonstrates an end-to-end data analytics solution built using Microsoft Fabric. It covers the complete analytics pipeline—from ingesting raw CSV files into a Lakehouse, transforming the data with Dataflow Gen2, storing curated data in a Warehouse, building a Semantic Model, and preparing the data for Power BI reporting.

Note: The Power BI dashboard is currently under development and will be added soon.

CSV Files
   │
   ▼
Lakehouse (Files)
   │
   ▼
Pipeline
   │
   ▼
Bronze Layer
   │
   ▼
Dataflow Gen2
(Data Cleaning & Transformation)
   │
   ▼
Warehouse (Gold Layer)
   │
   ▼
Semantic Model
   │
   ▼
Power BI Dashboard


## Technologies Used
Microsoft Fabric:-	Unified Analytics Platform
OneLake:-	Centralized Data Storage
Lakehouse:-	Store Raw Data
Dataflow Gen2:-	Data Cleaning
Pipeline:-	Data Orchestration
Warehouse:-	Analytical Storage
Semantic Model:-	Data Modeling
Power BI:-	Dashboard

## Workflow
### Step 1 — Create Workspace
Created a Microsoft Fabric Workspace.
All analytics assets were developed inside the same workspace.

<img width="841" height="500" alt="Screenshot 2026-07-17 121945" src="https://github.com/user-attachments/assets/798bfa71-c1ca-47bc-b811-cf9126a0e146" />

Step 2 — Create Lakehouse

Created a Lakehouse to serve as the centralized storage layer.

Uploaded all CSV files into the Files section.

The Files section can store multiple file formats including:

CSV
Excel
JSON
Parquet
Images
Text files

This data acts as the raw source for the analytics pipeline.

<img width="1838" height="875" alt="Screenshot 2026-07-17 122328" src="https://github.com/user-attachments/assets/a0823a76-6fc6-4f27-92ca-8c5af776fc63" />

Step 3 — Data Ingestion Pipeline

Created a Microsoft Fabric Pipeline to ingest raw CSV files into Lakehouse tables.

The pipeline loads raw files into Delta Tables, which represent the Bronze Layer of the Medallion Architecture.

Bronze Layer characteristics:

Raw source data
No transformations
Centralized storage in OneLake
Single source of truth

<img width="1779" height="666" alt="Screenshot 2026-07-17 123712" src="https://github.com/user-attachments/assets/7d4c5803-1d15-4be3-9a5c-c35f4c002967" />

Step 4 — Data Cleaning using Dataflow Gen2

Created a Dataflow Gen2 for data preparation.

Performed:

Data type corrections
Formatting
Validation
Basic data cleaning
Power Query transformations

The transformed data becomes ready for analytics.

<img width="1831" height="613" alt="Screenshot 2026-07-17 191859" src="https://github.com/user-attachments/assets/13416d2f-b80e-4f95-965b-d867c3e3eb59" />

Step 5 — Warehouse (Gold Layer)

Created a Warehouse for storing curated analytical data.

Using the pipeline, each transformed table was loaded into the Warehouse.

The Warehouse represents the Gold Layer, which contains:

Clean data
Structured tables
Analytics-ready datasets

Step 6 — Semantic Model

Created a Semantic Model.

Configured relationships between:

Fact Orders
Date Dimension
Dish Dimension
Restaurant Dimension
Location Dimension

This model is used by Power BI for reporting.

<img width="1201" height="550" alt="Screenshot 2026-07-17 203313" src="https://github.com/user-attachments/assets/b0d7ee01-31a2-4d04-b13b-9a7f0841c274" />

Step 7 — Power BI Dashboard

The Semantic Model will be connected to Power BI to build interactive dashboards.

Status: 🚧 Under Development



