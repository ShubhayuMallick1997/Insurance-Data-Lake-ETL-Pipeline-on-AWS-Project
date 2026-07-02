# 🏦 Insurance Data Lake ETL Pipeline on AWS

> **An End-to-End Enterprise Data Engineering Project using SQL Server, SSIS, AWS S3, PySpark, Athena, Power BI and REST API-ready Nested JSON**

![SQL Server](https://img.shields.io/badge/SQL%20Server-Database-red)
![SSIS](https://img.shields.io/badge/SSIS-ETL-blue)
![AWS S3](https://img.shields.io/badge/AWS-S3-orange)
![PySpark](https://img.shields.io/badge/PySpark-Big%20Data-yellow)
![Athena](https://img.shields.io/badge/Amazon-Athena-green)
![PowerBI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)
![Python](https://img.shields.io/badge/Python-3.x-blue)

---

# 📌 Project Overview

This project demonstrates an **enterprise-scale Data Engineering pipeline** for an Insurance Management System.

The objective is to simulate how insurance companies migrate operational data from a relational database into a cloud-based Data Lake, perform transformations using Apache Spark, create optimized analytical datasets, generate API-ready nested JSON documents, and prepare data for reporting and analytics.

The project follows a modern **Lakehouse architecture**, separating the pipeline into:

* Source Layer
* Raw Data Lake
* Curated Data Lake
* Analytics Layer
* Visualization Layer

The entire project was implemented using **Microsoft SQL Server, SSIS, AWS S3, Google Colab, PySpark, Athena and Power BI.**

---

# 🎯 Business Problem

Insurance companies store operational data across multiple normalized relational tables such as:

* Customer
* Policy
* Premium Payment
* Claims
* Products
* Agents
* Notifications
* Audit History

Business Intelligence tools, Machine Learning models and REST APIs cannot efficiently consume these normalized datasets directly.

Therefore, organizations typically build a Data Lake architecture to

* Centralize data
* Store multiple file formats
* Build optimized analytical datasets
* Generate API-ready JSON
* Support scalable analytics

This project simulates that complete workflow.

---

# 🏗 Solution Architecture

```text
                     SQL Server (InsuranceDB)
                               │
                               │
                         Initial Data Loading
                               │
                               ▼
                         SQL Server (SSMS)
                               │
                               ▼
                    SSIS ETL Data Extraction
                               │
                               ▼
                    Individual Excel Files
                               │
                               ▼
                         AWS CLI Upload
                               │
                               ▼
                 AWS S3 Raw Layer Storage
                               │
                               ▼
                      Google Colab Notebook
                               │
                               ▼
                 Pandas + Apache PySpark ETL
                               │
        ┌─────────────────────────────────────────┐
        │                                         │
        │   Data Validation                       │
        │   Data Transformation                   │
        │   DataFrame Creation                    │
        │   Multi-format Conversion               │
        │                                         │
        └─────────────────────────────────────────┘
                               │
        ┌──────────────┬─────────────┬────────────┬──────────────┐
        ▼              ▼             ▼            ▼
      CSV            JSON          ORC        PARQUET
        │              │             │            │
        └──────────────┴─────────────┴────────────┘
                               │
                      AWS CLI Upload
                               │
                               ▼
                    AWS S3 Curated Layer
                               │
             ┌─────────────────┴─────────────────┐
             ▼                                   ▼
       Amazon Athena                     Nested JSON APIs
             │                                   │
             ▼                                   ▼
        Power BI Dashboard                REST API / Postman
```

---

# 🚀 Technology Stack

| Category           | Technology                             |
| ------------------ | -------------------------------------- |
| Database           | Microsoft SQL Server                   |
| Database IDE       | SQL Server Management Studio (SSMS)    |
| ETL Tool           | SQL Server Integration Services (SSIS) |
| Programming        | Python                                 |
| Big Data           | Apache Spark (PySpark)                 |
| Notebook           | Google Colab                           |
| Cloud Storage      | AWS S3                                 |
| Cloud Query Engine | Amazon Athena                          |
| File Formats       | Excel, CSV, JSON, ORC, Parquet         |
| API Testing        | Postman                                |
| Data Visualization | Power BI                               |
| Version Control    | Git + GitHub                           |

---

# 📂 Database Schema

The Insurance database contains relational tables representing customers, policies, products, claims and premium payments.

```
Customer
│
├── Customer Policy
│      │
│      ├── Policy
│      │      │
│      │      └── Product Policy
│      │               │
│      │               └── Product
│      │
│      ├── Premium Payment
│      │
│      └── Claim
│              │
│              └── Claim Document
│
├── Agent Customer
│      │
│      └── Agent
│
├── Notification
│
└── Customer Audit

Employee
│
└── Branch

Users
```

---

# 📁 Project Repository Structure

```
Insurance-Data-Lake-ETL-Pipeline

│
├── SQL Scripts
│      ├── Database Creation
│      ├── Table Creation
│      ├── Insert Scripts
│      ├── Stored Procedures
│      └── Nested JSON Queries
│
├── SSIS Packages
│
├── Raw Excel Files
│
├── PySpark Notebooks
│
├── CSV Output
│
├── JSON Output
│
├── ORC Output
│
├── Parquet Output
│
├── Athena Queries
│
├── Power BI Dashboard
│
├── Images
│
└── README.md
```

---

# 📊 Project Workflow

```
SQL Server
      │
      ▼
SSMS
      │
      ▼
SSIS
      │
      ▼
Excel Files
      │
      ▼
AWS CLI
      │
      ▼
AWS S3 Raw Layer
      │
      ▼
Google Colab
      │
      ▼
PySpark
      │
      ▼
CSV
JSON
ORC
PARQUET
      │
      ▼
AWS CLI
      │
      ▼
AWS S3 Curated Layer
      │
      ▼
Amazon Athena
      │
      ▼
Power BI
```

---

# ⭐ Project Highlights

* Enterprise ETL Pipeline
* Cloud-based Data Lake Architecture
* SQL Server + SSIS Integration
* AWS S3 Raw & Curated Layers
* PySpark Data Processing
* Multi-format Data Conversion
* Amazon Athena Query Engine
* Nested JSON Generation using SQL Server
* Power BI Analytics
* REST API-ready Data Model

---

## 📌 Current Project Status

✅ Database Designed

✅ Tables Created

✅ Initial Data Loading Completed

✅ SSIS Data Extraction Completed

✅ Excel Generation Completed

✅ AWS S3 Raw Layer Completed

✅ Google Colab Integration Completed

✅ PySpark DataFrame Creation Completed

✅ CSV Generation Completed

✅ JSON Generation Completed

✅ ORC Generation Completed

✅ Parquet Generation Completed

✅ Curated Files Uploaded to AWS S3

⬜ Athena Analytics (In Progress)

⬜ Power BI Dashboard (Planned)

⬜ REST API Development (Planned)

⬜ Final Documentation (In Progress)
