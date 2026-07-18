# Swiggy End-to-End Data Analytics using Microsoft Fabric

## Project Overview

This project demonstrates an end-to-end data analytics solution built using Microsoft Fabric. It covers the complete analytics pipeline—from ingesting raw CSV files into a Lakehouse, transforming the data with Dataflow Gen2, storing curated data in a Warehouse, building a Semantic Model, and preparing the data for Power BI reporting.  
Note: The Power BI dashboard is currently under development and will be added soon.

---

## Project Architecture

```text
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
```

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Microsoft Fabric | Unified Analytics Platform |
| OneLake | Centralized Data Storage |
| Lakehouse | Raw Data Storage |
| Dataflow Gen2 | Data Cleaning & Transformation |
| Pipeline | Data Orchestration |
| Warehouse | Analytical Data Storage |
| Semantic Model | Data Modeling |
| Power BI | Business Intelligence & Reporting |

---

# Implementation Workflow

## Step 1: Create Workspace

A Microsoft Fabric workspace was created to manage all project assets in a single environment.

<img width="841" height="500" alt="Screenshot 2026-07-17 121945" src="https://github.com/user-attachments/assets/798bfa71-c1ca-47bc-b811-cf9126a0e146" />

---

## Step 2: Create Lakehouse

A Lakehouse was created to act as the centralized storage layer in OneLake.

### Activities Performed

- Uploaded all source CSV files into the **Files** section.
- Used the Files area because it supports multiple file formats.
- Stored raw source files before ingestion.

### Supported File Types

- CSV
- Excel
- JSON
- Parquet
- Images
- Text Files

<img width="1838" height="875" alt="Screenshot 2026-07-17 122328" src="https://github.com/user-attachments/assets/a0823a76-6fc6-4f27-92ca-8c5af776fc63" />

---

## Step 3: Data Ingestion Pipeline

A Microsoft Fabric Pipeline was created to ingest the raw CSV files into Lakehouse Delta Tables.

### Bronze Layer

The Bronze Layer stores raw data exactly as received from the source system.

**Key Characteristics**

- Raw source data
- No transformations
- Centralized storage in OneLake
- Single source of truth

<img width="1779" height="666" alt="Screenshot 2026-07-17 123712" src="https://github.com/user-attachments/assets/7d4c5803-1d15-4be3-9a5c-c35f4c002967" />

---

## Step 4: Data Cleaning with Dataflow Gen2

Dataflow Gen2 was used to clean and transform the Bronze Layer data using Power Query.

### Transformations Performed

- Data type conversion
- Data formatting
- Data validation
- Basic data cleaning
- Power Query transformations

The transformed data is prepared for analytical processing.

<img width="1831" height="613" alt="Screenshot 2026-07-17 191859" src="https://github.com/user-attachments/assets/13416d2f-b80e-4f95-965b-d867c3e3eb59" />

---

## Step 5: Warehouse (Gold Layer)

A Warehouse was created to store curated and analytics-ready data.

### Activities Performed

- Loaded transformed tables into the Warehouse.
- Stored clean and structured datasets.
- Prepared data for reporting and business analysis.

---

## Step 6: Semantic Model

A Semantic Model was created to establish relationships between fact and dimension tables.

### Relationships

- Fact Orders
- Date Dimension
- Dish Dimension
- Restaurant Dimension
- Location Dimension

The Semantic Model serves as the reporting layer for Power BI.

<img width="1201" height="550" alt="Screenshot 2026-07-17 203313" src="https://github.com/user-attachments/assets/b0d7ee01-31a2-4d04-b13b-9a7f0841c274" />

---

## Step 7: Power BI Report

The Semantic Model is connected to Power BI to build interactive dashboards and business reports.

---

## Microsoft Fabric Components Used

- Workspace
- OneLake
- Lakehouse
- Pipeline
- Delta Tables
- Dataflow Gen2
- Warehouse
- Semantic Model
- Power BI

---

## Medallion Architecture

### Bronze Layer
- Raw data ingested from source systems.

### Silver Layer
- Cleaned and transformed data using Dataflow Gen2.

### Gold Layer
- Curated, structured, and analytics-ready data stored in the Warehouse.

---

## Future Enhancements

- Interactive Power BI Dashboard
- Business KPIs
- Executive Dashboard
- Business Insights
- Advanced DAX Measures

---

## Repository Structure

```text
Dataset/
Images/
SQL/
Report/
README.md
```
