# 🏅 Olympic Azure Data Engineering Project

This project demonstrates a modern **end-to-end Data Engineering pipeline** built on **Azure Cloud** using the Tokyo 2020 Olympics dataset. It showcases real-world data ingestion, transformation, and analytics using industry-standard tools like **Azure Data Factory**, **Databricks**, **Azure Data Lake Storage Gen2**, and **Azure Synapse Analytics**.

---

## 🏗️ Architecture

```mermaid
<img width="638" alt="project" src="https://github.com/user-attachments/assets/571d3641-8262-428e-87b6-9af5de2fab76" />
```


## 🛠️ Tech Stack

Service / Tool	Purpose
Azure Data Factory	Ingest data into ADLS Gen2
Azure Data Lake Gen2	Store raw & processed datasets
Azure Databricks	Clean, transform, and process data
PySpark	Transformation logic in notebooks
Azure Synapse	SQL-based analytics on transformed data
Power BI	Optional dashboard visualizations

## 📂 Folder Structure
olympic-azure-data-engineering-project/
│
├── data/                          # Sample datasets
│   └── tokyo_olympics_2020.csv
│
├── notebooks/                    # Databricks notebooks
│   └── data_transformation.ipynb
│
├── adf_pipeline/                # Data Factory pipeline export (JSON)
│   └── olympic_ingestion_pipeline.json
│
├── powerbi/                     # Power BI report file (if available)
│   └── olympic_dashboard.pbix
│
├── synapse_queries/            # SQL scripts for Synapse Analytics
│   └── queries.sql
│
└── README.md

## 🔄 Pipeline Overview

1. Data Ingestion with Azure Data Factory
Ingests raw Olympic dataset from local or web source

Loads into ADLS Gen2 → /raw/olympics_2020/

2. Data Transformation using Azure Databricks
Reads raw data using PySpark

Cleans nulls, formats columns, derives insights

Writes cleaned data to /processed/olympics_2020/

3. Analytics with Azure Synapse
Connects to Processed Zone via SQL-on-demand or linked service

Performs queries to extract country-wise stats, medal rankings, sport trends, etc.

4. (Optional) Dashboard with Power BI
Connects to Synapse tables

Visualizes medals by country, athletes’ performance, sport-wise trends, etc.

## 🚀 How to Run

Prerequisites
Azure Subscription

Permissions to use Data Factory, Data Lake Gen2, Databricks, Synapse

Python (for local PySpark testing, optional)

Power BI Desktop (optional)

Steps
Clone this repo
```bash
git clone https://github.com/YasithaNV2001/olympic-azure-data-engineering-project.git
```

Import olympic_ingestion_pipeline.json into Azure Data Factory

Upload tokyo_olympics_2020.csv to ADLS Gen2 /raw/ container

Run the notebook data_transformation.ipynb in Azure Databricks

Connect Synapse to ADLS Processed Zone and run queries.sql

(Optional) Open olympic_dashboard.pbix in Power BI Desktop

