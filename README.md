# 🏢 SQL Server Data Warehouse & Analytics Project

An end-to-end **Data Warehousing and Analytics solution** built using Microsoft SQL Server. This project demonstrates the complete data lifecycle, from ingesting raw ERP and CRM data to transforming it into a structured data warehouse and generating meaningful business insights using SQL.

Developed as a portfolio project to demonstrate best practices in **Data Engineering, ETL, Data Modeling, and Data Analytics**.

---

## 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Project Requirements](#-project-requirements)
3. [Architecture](#-architecture)
4. [Data Model](#-data-model)
5. [Repository Structure](#-repository-structure)
6. [Tech Stack](#-tech-stack)
7. [Getting Started](#-getting-started)
8. [Key Insights](#-key-insights)
9. [About Me](#-about-me)

---

## 🔎 Project Overview

This project covers the complete data lifecycle, including:

- **Data Engineering:** Building a SQL Server data warehouse that consolidates sales data from two source systems.
- **ETL:** Extracting data from CSV files, cleaning and transforming it, and loading it into structured warehouse layers.
- **Data Modeling:** Designing a Star Schema consisting of fact and dimension tables to support efficient analytical queries.
- **Analytics & Reporting:** Developing SQL queries to answer real-world business questions and generate actionable insights.

---

## 🚀 Project Requirements

### Part 1: Building the Data Warehouse (Data Engineering)

**Objective:** Develop a modern data warehouse in SQL Server that consolidates sales data and supports analytical reporting and informed business decisions.

| Area | Requirement |
|---|---|
| **Data Sources** | Import data from two source systems (ERP and CRM) provided as CSV files. |
| **Data Quality** | Cleanse the data and resolve data quality issues before analysis. |
| **Integration** | Combine both sources into a single, user-friendly data model designed for analytical queries. |
| **Scope** | Use the latest available dataset. Historical data tracking (historization) is not required. |
| **Documentation** | Provide clear documentation of the data model for business stakeholders and analytics teams. |

### Part 2: BI Analytics & Reporting (Data Analytics)

**Objective:** Develop SQL-based analytics to deliver detailed insights into:

- Customer Behavior
- Product Performance
- Sales Trends

These insights provide stakeholders with the key business metrics required for strategic decision-making.

---

## 🏗️ Architecture

The data warehouse follows the **Medallion Architecture**, consisting of three layers:

| Layer | Purpose | Details |
|---|---|---|
| 🥉 **Bronze** | Raw Data | CSV files from ERP and CRM systems are loaded into SQL Server as-is. |
| 🥈 **Silver** | Cleaned Data | Data cleansing, standardization, normalization, and deduplication are performed. |
| 🥇 **Gold** | Business-Ready Data | A Star Schema is created using fact and dimension views for reporting and analytics. |

### Data Architecture Diagram

![Data Architecture](Data-Warehouse-Project/high-level-data-warehouse-architecture.png)

---

## 🧩 Data Model

The Gold layer follows a **Star Schema** consisting of the following tables:

| Table | Description |
|---|---|
| `dim_customers` | Customer details integrated from CRM and ERP systems. |
| `dim_products` | Product information, including product details and categories. |
| `fact_sales` | Sales transactions linked to customer and product dimensions. |

### Data Model Diagram

![Data Model](docs/data_model.png)

---

## 📁 Repository Structure

```text
data-warehouse-project/
│
├── datasets/                       # Raw ERP and CRM CSV files
│
├── docs/                           # Project documentation and diagrams
│   ├── data_architecture.png       # Data architecture diagram
│   ├── data_model.png              # Star schema diagram
│   ├── data_catalog.md             # Data catalog
│   └── naming_conventions.md       # Naming conventions
│
├── scripts/
│   ├── init_database.sql           # Database and schema creation
│   │
│   ├── bronze/                     # Raw data loading scripts
│   │
│   ├── silver/                     # Data cleaning and transformation
│   │
│   └── gold/                       # Star schema views
│
├── analytics/                      # SQL analytical queries
│
├── tests/                          # Data quality validation scripts
│
├── README.md                       # Project documentation
│
└── .gitignore                      # Git ignore configuration
```

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| **Database** | Microsoft SQL Server |
| **Query Language** | T-SQL |
| **Database Management** | SQL Server Management Studio (SSMS) |
| **Version Control** | Git & GitHub |
| **Diagramming** | Draw.io |
| **Source Data** | CSV Files (ERP & CRM) |

---

## ⚙️ Getting Started

Follow these steps to set up and run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
```

### 2. Install the Required Software

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- Git

### 3. Initialize the Database

Execute the following script in SSMS:

```sql
scripts/init_database.sql
```

This creates the project database and the following schemas:

- `bronze`
- `silver`
- `gold`

### 4. Load the Bronze Layer

- Update the CSV file paths in the Bronze loading scripts.
- Execute the scripts to import the raw ERP and CRM data into SQL Server.

### 5. Build the Silver Layer

Execute the Silver layer scripts to:

- Clean and standardize the data.
- Handle missing and inconsistent values.
- Remove duplicate records.
- Prepare the data for integration.

### 6. Build the Gold Layer

Execute the Gold layer scripts to create the analytical data model using fact and dimension views.

### 7. Run the Analytics Queries

Execute the SQL queries available in the `analytics/` folder to explore business insights.

---

## 📊 Key Insights

The analytics layer answers important business questions, including:

### Customer Behavior
- Who are the top-performing customers based on total spending?
- How can customers be segmented based on spending and purchasing activity?
- Which customers contribute the most to overall revenue?

### Product Performance
- Which products and categories generate the highest revenue?
- Which products perform above or below the average sales level?
- What are the best-performing products?

### Sales Trends
- How do sales trends change monthly and yearly?
- What is the cumulative sales performance over time?
- Which periods generate the highest sales revenue?

### Analysis & Query Results

_Add screenshots of SQL queries, query outputs, and key business insights here._

---

## 🌟 About Me

Hi, I'm **Basil Thalakkodan**, a Data Analyst interested in transforming raw data into meaningful business insights using SQL and data analytics.

I enjoy working with data, solving business problems, and building analytical solutions that support data-driven decision-making.

### 📫 Connect With Me

- **LinkedIn:** [Your LinkedIn Profile](<your-linkedin-url>)
- **GitHub:** [Your GitHub Profile](<your-github-url>)
- **Email:** <your-email-address>

---

⭐ If you find this project useful, feel free to explore the repository!
