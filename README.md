# 🏦 Insurance Data Lake ETL Pipeline on AWS

> **An End-to-End Enterprise Data Engineering Project using SQL Server, SSIS, AWS S3, PySpark, Athena, Power BI and REST API-ready Nested JSON**

![SQL Server](https://img.shields.io/badge/SQL%20Server-Database-red)
![SSIS](https://img.shields.io/badge/SSIS-ETL-blue)
![AWS S3](https://img.shields.io/badge/AWS-S3-orange)
![PySpark](https://img.shields.io/badge/PySpark-Big%20Data-yellow)
![Athena](https://img.shields.io/badge/Amazon-Athena-green)
![PowerBI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)
![Python](https://img.shields.io/badge/Python-3.x-blue)



![SQL Server](https://github.com/ShubhayuMallick1997/Insurance-Data-Lake-ETL-Pipeline-on-AWS-Project/blob/main/Insurance%20End%20to%20End%20Pyspark%20SSIS%20AWS%20Project%20Architecture.png)
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


# ⚙️ ETL Implementation

This section explains the complete ETL workflow implemented during the project.

---

# Phase 1 — Database Design (SQL Server)

The project begins with the design of an Insurance Management relational database using Microsoft SQL Server.

### Database Created

```
InsuranceDB
```

### Tables Implemented

```
Customer
Policy
Customer_Policy
Premium_Payment
Claim
Claim_Document
Products
Product_Policy
Agent
Agent_Customer
Employee
Branch
Notification
Customer_Audit
Users
```

### Features

* Primary Keys
* Foreign Keys
* One-to-Many Relationships
* Many-to-Many Relationships
* Junction Tables
* Master & Transaction Tables

---

# Entity Relationship Diagram

```
Customer
│
├── Customer_Policy
│      │
│      ├── Policy
│      │      │
│      │      └── Product_Policy
│      │               │
│      │               └── Products
│      │
│      ├── Premium_Payment
│      │
│      └── Claim
│              │
│              └── Claim_Document
│
├── Notification
│
├── Customer_Audit
│
└── Agent_Customer
        │
        └── Agent

Employee
│
└── Branch

Users
```

---

# Phase 2 — Initial Data Loading (SSMS)

After creating all database tables, sample insurance data was inserted into every table.

Data includes

* Customers
* Policies
* Claims
* Premium Payments
* Products
* Agents
* Notifications
* Audit Records

The objective was to simulate an operational insurance database.

---

# Phase 3 — ETL using SSIS

SQL Server Integration Services (SSIS) was used to extract data from SQL Server.

## Source

```
SQL Server
```

↓

## Data Flow Tasks

Each table was connected individually using an OLE DB Source.

```
Customer

Policy

Claim

Premium Payment

Products

...

15 Tables
```

↓

## Data Conversion

Unicode and Non-Unicode datatype mismatches were handled using the **Data Conversion Transformation**.

Examples:

```
DT_STR

↓

DT_WSTR
```

```
TEXT

↓

Unicode String
```

This ensured successful export to Excel.

---

# Phase 4 — Excel Generation

Each SQL Server table was exported as an independent Excel file.

Generated files include:

```
Customer.xlsx

Policy.xlsx

Customer_Policy.xlsx

Premium_Payment.xlsx

Claim.xlsx

Claim_Document.xlsx

Products.xlsx

Product_Policy.xlsx

Agent.xlsx

Agent_Customer.xlsx

Branch.xlsx

Employee.xlsx

Notification.xlsx

Customer_Audit.xlsx

Users.xlsx
```

These Excel files represent the Raw Dataset extracted from the operational database.

---

# SSIS Workflow

```
SQL Server

↓

OLE DB Source

↓

Data Conversion

↓

Excel Destination
```

---

# SSIS Control Flow

```
Customer

↓

Policy

↓

Customer Policy

↓

Premium Payment

↓

Claim

↓

Claim Document

↓

Products

↓

Product Policy

↓

Agent

↓

Agent Customer

↓

Employee

↓

Branch

↓

Notification

↓

Customer Audit

↓

Users
```

All ETL tasks were executed within a single SSIS package.

---

# Phase 5 — AWS S3 Integration

AWS CLI was configured on the local system.

Configuration included:

```
IAM User

↓

Access Key

↓

Secret Access Key

↓

AWS CLI Configure
```

Connection verification

```
aws s3 ls
```

---

# Raw Layer Upload

Each generated Excel file was uploaded into the Raw Layer bucket.

```
Raw Layer

│

├── Customer.xlsx

├── Policy.xlsx

├── Customer_Policy.xlsx

├── Premium_Payment.xlsx

├── Claim.xlsx

├── Products.xlsx

├── Notification.xlsx

...

15 Excel Files
```

Purpose

* Preserve original source data
* Immutable raw storage
* Recovery point
* Data lineage

---

# AWS Data Lake Architecture

```
SQL Server

↓

SSIS

↓

Excel

↓

AWS CLI

↓

S3 Raw Layer
```

---

# Phase 6 — Google Colab

Google Colab was selected because Amazon EMR was intentionally avoided to keep the project within the AWS Free Tier.

Libraries installed:

```
boto3

pandas

pyspark

openpyxl
```

---

# Connecting Google Colab to AWS S3

AWS credentials were configured inside the notebook.

Workflow

```
Google Colab

↓

boto3

↓

AWS S3

↓

Download Excel Files
```

---

# Reading Excel Files

Using pandas

```python
pdf = pd.read_excel(...)
```

↓

Converted into Spark DataFrame

```python
customer_df = spark.createDataFrame(pdf)
```

---

# Spark Data Processing

Each dataset was validated using

```
show()

printSchema()

head()

count()
```

before conversion.

---

# Multi-format Data Generation

Each Spark DataFrame was converted into

```
CSV

JSON

ORC

PARQUET
```

using

```python
DataFrameWriter
```

Example

```
Spark DataFrame

↓

CSV

↓

JSON

↓

ORC

↓

PARQUET
```

---

# Generated File Structure

```
Customer_csv

Customer_json

Customer_orc

Customer_parquet

Policy_csv

Policy_json

...

15 Tables
×
4 Formats
```

Total output datasets

```
15 Tables

×

4 Formats

=

60 Output Datasets
```

---

# File Renaming

Since Apache Spark generates random

```
part-0000....
```

files,

Python automation was used to rename every output file into meaningful names.

Example

```
Customer_Data.parquet

Policy_Data.parquet

Claim_Data.json

Notification_Data.csv
```

---

# Phase 7 — Curated Layer Upload

After local verification, each generated dataset was uploaded to dedicated AWS S3 curated storage.

```
CSV Bucket

JSON Bucket

ORC Bucket

PARQUET Bucket
```

using AWS CLI.

---

# Curated Layer Architecture

```
Google Colab

↓

PySpark

↓

CSV

↓

AWS S3 CSV Bucket


Google Colab

↓

PySpark

↓

JSON

↓

AWS S3 JSON Bucket


Google Colab

↓

PySpark

↓

ORC

↓

AWS S3 ORC Bucket


Google Colab

↓

PySpark

↓

PARQUET

↓

AWS S3 Parquet Bucket
```

---

# ETL Pipeline Summary

```
SQL Server

↓

SSMS

↓

SSIS

↓

Excel Files

↓

AWS CLI

↓

S3 Raw Layer

↓

Google Colab

↓

PySpark

↓

Spark DataFrame

↓

CSV

JSON

ORC

PARQUET

↓

AWS CLI

↓

AWS S3 Curated Layer
```

---

# Deliverables Completed

✔ Database Design

✔ Relational Schema

✔ Sample Data Generation

✔ SQL Server Implementation

✔ SSIS ETL Package

✔ Excel Export

✔ AWS CLI Configuration

✔ Raw Layer Upload

✔ Google Colab Integration

✔ AWS S3 Integration

✔ Pandas Data Processing

✔ Spark DataFrame Creation

✔ CSV Conversion

✔ JSON Conversion

✔ ORC Conversion

✔ Parquet Conversion

✔ Spark File Renaming Automation

✔ Curated Layer Upload


# 📊 Analytics Layer

After the ETL pipeline successfully migrated the data into AWS S3 Curated Storage, the next objective was to build an analytical layer capable of serving Business Intelligence reports and API-ready datasets.

---

# Amazon Athena

Amazon Athena was selected as the serverless SQL query engine to analyze data stored in Amazon S3 without provisioning any servers.

Athena enables SQL queries directly on cloud storage and is ideal for data lake analytics.

---

## Athena Workflow

```text
AWS S3 Curated Layer
        │
        ▼
AWS Glue Data Catalog
        │
        ▼
Amazon Athena
        │
        ▼
SQL Analytics
```

---

# Athena Database

Example

```sql
CREATE DATABASE insurance_curated;
```

---

# External Tables

External tables were created on top of the Parquet datasets stored inside the Curated Layer.

Example tables

```text
Customer

Policy

Customer_Policy

Premium_Payment

Claim

Products

Notification

Customer_Audit
```

---

# Why Parquet?

Parquet was selected as the primary analytical format because it provides

* Columnar Storage
* Compression
* Predicate Pushdown
* Faster Scan Performance
* Reduced Storage Cost

Compared to CSV

| CSV          | Parquet         |
| ------------ | --------------- |
| Row Based    | Column Based    |
| Large Size   | Compressed      |
| Slow Queries | Fast Queries    |
| No Schema    | Embedded Schema |

---

# File Format Strategy

| Format  | Purpose            |
| ------- | ------------------ |
| Excel   | Raw Extraction     |
| CSV     | Data Exchange      |
| JSON    | REST APIs          |
| ORC     | Hadoop Ecosystem   |
| Parquet | Analytics / Athena |

---

# Multi-format Data Lake

```text
Raw Layer

│

├── Excel



Curated Layer

│

├── CSV

├── JSON

├── ORC

└── PARQUET
```

---

# SQL Analytics Examples

Example 1

Total Customers

```sql
SELECT COUNT(*)
FROM customer;
```

---

Example 2

Total Premium Collected

```sql
SELECT SUM(amount)
FROM premium_payment;
```

---

Example 3

Claims by Status

```sql
SELECT
claim_status,
COUNT(*)
FROM claim
GROUP BY claim_status;
```

---

Example 4

Products Under Each Policy

```sql
SELECT
pol_id,
COUNT(prod_id)
FROM product_policy
GROUP BY pol_id;
```

---

# Nested JSON Generation

One of the major objectives of this project was generating hierarchical JSON directly from SQL Server.

Instead of returning flat relational datasets, SQL Server's

```text
FOR JSON PATH
```

feature was used to build enterprise API responses.

---

# Nested JSON Hierarchy

```text
Customers
│
├── Customer
│
├── Agent Customer
│      │
│      └── Agent
│
├── Customer Policies
│      │
│      ├── Policy
│      │      │
│      │      └── Products
│      │               │
│      │               └── Product
│      │
│      ├── Claims
│      │      │
│      │      └── Claim Documents
│      │
│      └── Premium Payments
│
├── Notifications
│
└── Customer Audit
```

---

# REST API Ready JSON

The generated JSON structure closely resembles production REST APIs used by Insurance and Banking platforms.

Example

```json
{
  "cust_id": 1,
  "cust_name": "John",

  "Customer_Policies":[

      {

        "Policy":{

            "Products":[...]

        },

        "Claims":[...]

      }

  ],

  "Notifications":[...]

}
```

---

# Data Quality Validation

During the ETL process, several validations can be applied before writing curated datasets.

Examples

* Duplicate Customer Removal

* Email Standardization

* Mobile Number Validation

* Null Customer Removal

* Date Validation

* Invalid Premium Detection

* Invalid Claim Detection

---

# Curated Layer Objectives

The Curated Layer is optimized for

* Business Intelligence

* Machine Learning

* Data Science

* REST APIs

* SQL Analytics

* Dashboarding

---

# Power BI

Power BI will consume the Curated Layer to build enterprise dashboards.

---

## Dashboard 1

Executive Summary

KPIs

* Total Customers

* Total Policies

* Active Policies

* Total Claims

* Premium Collected

---

## Dashboard 2

Customer Analytics

Charts

* Customers by State

* Customers by City

* Customers by Agent

* Customer Growth

---

## Dashboard 3

Policy Analytics

Charts

* Policies by Type

* Premium by Policy

* Expired Policies

* Active Policies

---

## Dashboard 4

Claim Analytics

Charts

* Claims by Month

* Claims by Reason

* Claims by Status

* Total Claim Amount

---

## Dashboard 5

Financial Dashboard

Charts

* Monthly Premium

* Quarterly Premium

* Annual Premium

* Revenue Trend

---

# Postman

The Nested JSON generated from SQL Server is designed to serve REST APIs.

Example endpoints

```text
GET /customers

GET /policies

GET /claims

GET /products
```

Response

```text
Nested JSON
```

---

# Future Enhancements

Future improvements planned for this project include:

* Apache Airflow orchestration
* AWS Glue Crawlers
* AWS Glue ETL Jobs
* Amazon Redshift warehouse
* Amazon QuickSight dashboards
* AWS Lambda automation
* Amazon API Gateway
* CI/CD using GitHub Actions
* Docker containerization
* Terraform infrastructure as code
* Data quality monitoring
* Automated pipeline scheduling

---

# Skills Demonstrated

This project demonstrates practical experience with:

### Database

* SQL Server
* Relational Database Design
* SQL
* JSON Generation

### ETL

* SSIS
* Data Conversion
* Data Migration

### Cloud

* AWS S3
* AWS CLI
* Amazon Athena

### Big Data

* Apache Spark
* PySpark
* Pandas

### Data Lake

* Raw Layer
* Curated Layer
* Multi-format Storage

### Analytics

* Amazon Athena
* Power BI

### API

* Nested JSON
* REST API Design
* Postman

---

# Project Status

| Phase                    | Status         |
| ------------------------ | -------------- |
| Database Design          | ✅ Completed    |
| Initial Data Loading     | ✅ Completed    |
| SSIS ETL                 | ✅ Completed    |
| Raw Layer                | ✅ Completed    |
| Google Colab Integration | ✅ Completed    |
| PySpark Processing       | ✅ Completed    |
| CSV Generation           | ✅ Completed    |
| JSON Generation          | ✅ Completed    |
| ORC Generation           | ✅ Completed    |
| Parquet Generation       | ✅ Completed    |
| Curated Layer            | ✅ Completed    |
| Athena Setup             | 🔄 In Progress |
| Nested JSON              | 🔄 In Progress |
| Power BI                 | 📋 Planned     |
| REST API                 | 📋 Planned     |


# 📂 Complete Repository Structure

```
Insurance-Data-Lake-ETL-Pipeline
│
├── README.md
│
├── LICENSE
│
├── .gitignore
│
├── Database
│   ├── Database_Creation.sql
│   ├── Table_Creation.sql
│   ├── Sample_Data.sql
│   ├── Stored_Procedures.sql
│   ├── Nested_JSON.sql
│   └── Athena_Queries.sql
│
├── SSIS
│   ├── Insurance_ETL.dtsx
│   ├── Project.params
│   └── Screenshots
│
├── Raw_Data
│   ├── Customer.xlsx
│   ├── Policy.xlsx
│   ├── Claim.xlsx
│   └── ...
│
├── Google_Colab
│   ├── Customer_ETL.ipynb
│   ├── Policy_ETL.ipynb
│   └── ...
│
├── PySpark
│   ├── Customer_ETL.py
│   ├── Policy_ETL.py
│   ├── Common_Functions.py
│   └── Rename_Output.py
│
├── Output
│   ├── CSV
│   ├── JSON
│   ├── ORC
│   └── PARQUET
│
├── Athena
│   ├── DDL
│   ├── Analytics
│   └── Screenshots
│
├── PowerBI
│   ├── Insurance.pbix
│   └── Dashboard_Screenshots
│
├── Images
│   ├── Architecture
│   ├── ER_Diagram
│   ├── SSIS
│   ├── S3
│   ├── Athena
│   └── Dashboard
│
└── Documentation
    ├── Project_Report.pdf
    ├── Architecture.pdf
    └── Presentation.pptx
```

---

# ▶️ How to Run the Project

## Step 1

Clone Repository

```bash
git clone https://github.com/<username>/insurance-data-lake-etl-pipeline.git
```

---

## Step 2

Restore SQL Server Database

Execute

```
Database_Creation.sql

↓

Table_Creation.sql

↓

Sample_Data.sql
```

---

## Step 3

Run SSIS Package

Open

```
Insurance_ETL.dtsx
```

Execute package

↓

Excel files generated.

---

## Step 4

Upload Raw Data

Configure AWS CLI

```
aws configure
```

Upload

```
Excel

↓

AWS S3 Raw Layer
```

---

## Step 5

Open Google Colab

Run

```
Customer_ETL.ipynb
```

Repeat for every table.

---

## Step 6

Generated Outputs

```
CSV

JSON

ORC

PARQUET
```

---

## Step 7

Upload Curated Data

Using AWS CLI

```
aws s3 cp ...
```

↓

Curated Layer

---

## Step 8

Create Athena Tables

Execute

```
CREATE DATABASE

↓

CREATE TABLE

↓

SELECT
```

---

## Step 9

Power BI

Connect

```
Athena

↓

Power BI
```

Create dashboards.

---

# 📸 Project Screenshots

Include screenshots of:

## SQL Server

* Database
* Tables
* Sample Data

---

## SSIS

* Control Flow
* Data Flow
* Data Conversion

---

## AWS S3

* Raw Layer
* Curated Layer

---

## Google Colab

* Spark DataFrame
* CSV Generation
* Parquet Generation

---

## Athena

* Table Creation
* Query Results

---

## Power BI

* Executive Dashboard
* Claims Dashboard
* Customer Dashboard

---

# 🏆 Project Achievements

✔ Enterprise ETL Pipeline

✔ SQL Server Database Design

✔ Complete Relational Schema

✔ SSIS Data Migration

✔ Data Type Conversion

✔ AWS S3 Raw Data Lake

✔ Google Colab Integration

✔ Apache Spark Data Processing

✔ CSV Generation

✔ JSON Generation

✔ ORC Generation

✔ Parquet Generation

✔ AWS S3 Curated Layer

✔ Athena Analytics

✔ Nested JSON Generation

✔ REST API Ready Dataset

✔ Power BI Reporting

---

# 💼 Resume Highlights

### End-to-End Insurance Data Engineering Pipeline

Designed and implemented an enterprise-scale Insurance Data Lake pipeline using SQL Server, SSIS, AWS S3, Apache Spark (PySpark), Amazon Athena and Power BI. Developed ETL workflows for migrating relational data into a cloud-based data lake, generated multi-format datasets (CSV, JSON, ORC and Parquet), built hierarchical nested JSON using SQL Server, and prepared analytical datasets for Business Intelligence reporting.

---

# 🎯 Learning Outcomes

Through this project, I gained practical experience in:

* Database Design
* SQL Programming
* SQL Server Administration
* SSIS ETL Development
* Data Migration
* Data Lake Architecture
* Apache Spark
* PySpark
* Pandas
* Amazon S3
* AWS CLI
* Amazon Athena
* Data Format Conversion
* Nested JSON Generation
* REST API Data Modeling
* Power BI Reporting
* End-to-End Data Engineering Workflow

---

# 📈 End-to-End Workflow

```
                     SQL Server
                          │
                          ▼
                 Initial Data Loading
                          │
                          ▼
                       SSMS
                          │
                          ▼
                       SSIS ETL
                          │
                          ▼
                  Excel Extraction
                          │
                          ▼
                     AWS CLI Upload
                          │
                          ▼
                 AWS S3 Raw Layer
                          │
                          ▼
                 Google Colab ETL
                          │
                          ▼
                  Pandas + PySpark
                          │
        ┌─────────────────┼─────────────────┐
        ▼                 ▼                 ▼
      CSV               JSON             ORC
        │                                  │
        └───────────────┬──────────────────┘
                        ▼
                    Parquet
                        │
                        ▼
                AWS CLI Upload
                        │
                        ▼
              AWS S3 Curated Layer
                        │
        ┌───────────────┴────────────────┐
        ▼                                ▼
  Amazon Athena                 Nested JSON
        │                                │
        ▼                                ▼
   Power BI Dashboards          REST APIs / Postman
```

---

# 🔮 Future Roadmap

* Apache Airflow orchestration
* AWS Glue Crawlers
* AWS Glue ETL Jobs
* Amazon Redshift
* Amazon QuickSight
* AWS Lambda
* Amazon API Gateway
* CI/CD using GitHub Actions
* Docker
* Kubernetes
* Terraform
* Data Quality Framework
* Automated Testing
* Data Lineage
* Monitoring & Alerting

---

# 👨‍💻 Author

**Shubhayu Mallick**

**Data Engineer | SQL | PySpark | AWS | ETL | SSIS | Apache Spark**

---

# ⭐ If you found this project useful

Please consider giving the repository a ⭐ on GitHub.

---

# 📜 License

This project is licensed under the **MIT License**.

Feel free to fork, contribute, and extend the project for educational purposes.

---

## 🙏 Acknowledgements

This project was developed as a practical implementation of modern Data Engineering concepts using Microsoft SQL Server, SSIS, AWS Cloud Services, Apache Spark, and Power BI to simulate a real-world insurance data platform.

