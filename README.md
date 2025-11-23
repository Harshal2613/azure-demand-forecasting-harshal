# Azure-Demand-Forecasting-Capacity-Optimization-System-Harshal-Mahajan

📊 Azure Demand Forecasting & Capacity Optimization System

Infosys Springboard 6.0 – Internship Project

Azure Cloud • Databricks • Medallion Architecture • Machine Learning • Power BI Dashboards

Demo Video :
<video src="sandbox:/mnt/data/demovideo.mp4" width="600" controls></video>




🚀 Project Overview

This project demonstrates a complete end-to-end Cloud Demand Forecasting & Capacity Optimization system built using Azure Data Factory, Azure Databricks, Azure Data Lake Gen2, and Power BI.

It shows how large-scale enterprise data — coming from Snowflake, Amazon S3, and REST APIs — can be collected, unified, cleaned, modeled, and visualized using a fully scalable cloud architecture.

The system helps cloud service providers or internal cloud teams to:

  Analyze compute & storage usage

  Forecast next-month and next-year cloud demand

  Compare ML model performance (MAPE-based)

  Identify region-wise growth patterns

  Optimize resource allocation across Azure regions

🗂️ Architecture Overview

![WhatsApp Image 2025-11-23 at 19 24 32_720ca87d](https://github.com/user-attachments/assets/82421743-0e5e-4bd2-8323-5933ee2ae698)





🧱 Medallion Architecture
  🔶 Bronze Layer – Raw Data

    Direct ingestion from Snowflake, GCP, and API

    No transformations

    Schema-aligned storage

    Files stored as received for auditing

  Raw Datasets Used:

    demand_data.csv

    external_factors.csv

    feature_engineering_data.csv

  🔷 Silver Layer – Cleaned/Structured Data

    cleaning & handling missing values

    Standardizing column formats

    Joining compute + storage + external datasets

     Time-series feature creation (Day, Month, Region, Season)

  Calculating KPI fields like:
    ✔ usage_units
    ✔ peak_usage_units
    ✔ cloud_demand_index
    ✔ week-over-week growth

  🟡 Gold Layer – Analytics & Modeling

    Aggregated demand tables

    Region-level and service-level summaries

    Feature-engineered datasets for ML

    Final tables exported to Power BI

🤖 Machine Learning Pipeline

  A dedicated forecasting notebook in Databricks trains multiple models for each Azure region and service (Compute & Storage).

  ML Workflow Includes:

    Loop through each region (West Europe, East US, Central India)

  Train multiple models:

    1.Prophet

    2.XGBoost

    3.Random Forest

    4.Holt-Winters

    5.ARIMA

  Calculate MAPE for every model

  Select the best-performing model per region

  Generate daily forecast for next month

  Generate 12-month forecast for next year

  Store results in Gold Layer

  Export outputs for Power BI dashboards

📊 Power BI Dashboards

  The final results are visualized using interactive dashboards with drill-through navigation.

  1️⃣ Azure Cloud Summary Dashboard

  ![WhatsApp Image 2025-11-23 at 18 54 15_715f3cfd](https://github.com/user-attachments/assets/b9b3289b-b282-43ee-a95c-bf95a21c1e77)


  ✔ Shows overall cloud usage patterns and capacity trends.

  2️⃣ Regional Analysis Dashboard

  ![WhatsApp Image 2025-11-23 at 18 54 41_07791542](https://github.com/user-attachments/assets/cc7f558f-4a1f-49b8-b3a8-b926c1565fd0)



  ✔ Helps identify which region requires resource optimization.

  3️⃣ Compute Forecast Dashboard

  ![WhatsApp Image 2025-11-23 at 18 55 02_a75dce4b](https://github.com/user-attachments/assets/a4389da4-e6d7-40c4-817d-9b607da56912)


  ✔ Used to plan VM capacity & scaling strategies.

  4️⃣ Storage Forecast Dashboard

  ![WhatsApp Image 2025-11-23 at 18 57 48_67924785](https://github.com/user-attachments/assets/16afa1a5-3049-47ab-9dbb-49c03b164c4e)

  ✔ Helps plan storage expansion & cost optimization.
  
  The dashboard is visible in this link: 
  https://app.powerbi.com/view?r=eyJrIjoiOGRhOTVmZDItNThhZC00MWJmLTkxNzUtYWVkYTZkNGM4NzRkIiwidCI6IjI5MTk2MTM0LTRiNzktNDY1NS1hYTZjLTAyNTc2MzQ5NGI2NCJ9 
  
🔧 Technologies Used

  1.Azure Data Factory

  2.Azure Databricks (PySpark + ML)

  3.Azure Data Lake Gen2

  4.Snowflake

  5.GCP

  6.REST APIs

  7.Power BI

  8.Machine Learning Models: Prophet, XGBoost, Random Forest, Holt-Winters, ARIMA

🎯 Key Outcomes

  1.Unified multi-source Azure usage dataset

  2.Fully automated ETL pipeline using Medallion architecture

  3.Accurate forecasting for compute & storage usage

  4.Region-wise ML model selection based on MAPE

  5.Production-ready Power BI dashboards

End-to-end workflow replicating enterprise cloud demand systems
