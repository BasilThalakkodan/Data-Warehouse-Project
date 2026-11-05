🏢 SQL Server Data Warehouse & Analytics Project
An end-to-end data warehousing and analytics solution: from ingesting raw ERP and CRM data to building a clean, analysis-ready warehouse and producing business insights with SQL.
Built as a portfolio project to demonstrate data engineering and data analytics best practices.
---
📌 Table of Contents
Project Overview
Project Requirements
Architecture
Data Model
Repository Structure
Tech Stack
Getting Started
Key Insights
About Me
---
🔎 Project Overview
This project covers the full data lifecycle:
Data Engineering: build a SQL Server data warehouse that consolidates sales data from two source systems.
ETL: extract CSV files, clean and transform them, and load them into structured layers.
Data Modeling: design a star schema (fact and dimension tables) for fast analytical queries.
Analytics & Reporting: write SQL queries that answer real business questions.
---
🚀 Project Requirements
Part 1: Building the Data Warehouse (Data Engineering)
Objective: Develop a modern data warehouse in SQL Server that consolidates sales data and supports analytical reporting and informed decision-making.
Area	Requirement
Data Sources	Import data from two source systems (ERP and CRM) provided as CSV files
Data Quality	Cleanse the data and resolve quality issues before analysis
Integration	Combine both sources into a single, user-friendly data model built for analytical queries
Scope	Latest dataset only; historization is not required
Documentation	Provide clear documentation of the data model for both business stakeholders and analytics teams
Part 2: BI Analytics & Reporting (Data Analytics)
Objective: Develop SQL-based analytics that deliver detailed insights into:
Customer Behavior
Product Performance
Sales Trends
These insights give stakeholders the key business metrics they need for strategic decisions.
---
🏗️ Architecture
The warehouse follows the Medallion Architecture with three layers:
Layer	Purpose	Details
🥉 Bronze	Raw data	CSV files from ERP and CRM loaded as-is into SQL Server
🥈 Silver	Cleaned data	Data cleansing, standardization, normalization, and deduplication
🥇 Gold	Business-ready data	Star schema with fact and dimension views for reporting and analytics
> 📷 Add your architecture diagram here: `docs/data_architecture.png`
---
🧩 Data Model
The Gold layer uses a star schema:
`dim_customers`: customer details (merged from CRM and ERP)
`dim_products`: product details and categories
`fact_sales`: sales transactions linked to customers and products
> 📷 Add your data model diagram here: `docs/data_model.png`
---
📁 Repository Structure
```
data-warehouse-project/
│
├── datasets/                 # Raw ERP and CRM CSV files
│
├── docs/                     # Diagrams, data catalog, naming conventions
│   ├── data_architecture.png
│   ├── data_model.png
│   ├── data_catalog.md
│   └── naming_conventions.md
│
├── scripts/
│   ├── init_database.sql     # Create database and schemas
│   ├── bronze/               # Raw data load scripts
│   ├── silver/               # Cleaning and transformation scripts
│   └── gold/                 # Star schema views
│
├── analytics/                # SQL queries for insights
│
├── tests/                    # Data quality checks
│
├── README.md
└── .gitignore
```
---
🛠️ Tech Stack
Database: Microsoft SQL Server
Language: T-SQL
Tools: SQL Server Management Studio (SSMS), Git & GitHub
Diagramming: draw.io
Source Data: CSV files (ERP and CRM)
---
⚙️ Getting Started
Clone the repository
```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   ```
Install SQL Server and SSMS.
Run `scripts/init_database.sql` to create the database and the `bronze`, `silver`, and `gold` schemas.
Load Bronze: update the CSV file paths in the bronze scripts, then run them.
Build Silver: run the silver layer scripts to clean and transform the data.
Build Gold: run the gold layer scripts to create the star schema views.
Analyze: run the queries in the `analytics/` folder.
---
📊 Key Insights
The analytics layer answers questions such as:
Who are our top customers, and how do they segment by spend and activity?
Which products and categories drive the most revenue?
How do sales trend over time (monthly, yearly, cumulative)?
Which products or customers are performing above or below average?
> Add screenshots or sample query results here.
---
🌟 About Me
Hi, I'm Basil Thalakkodan, a Data Analyst who enjoys turning raw data into clear, practical insights using SQL.
📫 Connect with me:
LinkedIn: <your-link>
GitHub: <your-link>
Email: <your-email>
