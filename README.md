Project Title:-  Retail Data Warehouse using Snowflake
Project Overview :

This project demonstrates the implementation of an end-to-end data warehouse solution in Snowflake using Medallion Architecture (Bronze, Silver, and Gold layers). The project covers data ingestion, transformation, data quality validation, incremental loading using Streams, task automation, stored procedures, and dimensional modeling for analytics.

Technologies Used :-

Snowflake
SQL
Medallion Architecture
ETL/ELT
Star Schema
Streams
Tasks
Stored Procedures
Views
Data Quality Framework

Key Features :-

Bronze, Silver, and Gold data layers
Retail sales data warehouse
Data cleansing and transformation
Star Schema (Fact & Dimension Tables)
Customer, Product, and Revenue analytics
Data Quality validation framework
Pipeline audit logging
Incremental data loading using Streams
Automated pipeline execution using Tasks
Stored Procedures for reusable ETL logic
Analytics-ready Gold Layer

Project Workflow :-

                                  RETAIL DATA WAREHOUSE PROJECT
                                              │
                                              ▼
                              Source CSV Files (Customers, Products, Orders)
                                              │
                                              ▼
                          Load Raw Data into Snowflake Bronze Layer
                           (CUSTOMERS_RAW, PRODUCTS_RAW, ORDERS_RAW)
                                              │
                                              ▼
                            Bronze Layer (Raw Data Storage)
                  • Raw data ingestion
                  • No transformations
                  • Historical data preserved
                                              │
                                              ▼
                      Data Cleaning & Standardization (Silver Layer)
                  • Remove invalid records
                  • Convert data types
                  • Standardize date formats
                  • Handle null values
                  • Data validation
                                              │
                                              ▼
                              Silver Layer (Cleaned Data)
                      CUSTOMERS | PRODUCTS | ORDERS
                                              │
                    ┌─────────────────────────┴─────────────────────────┐
                    ▼                                                   ▼
         Incremental Data Loading                             Data Quality Checks
      • Snowflake Streams                                   • Null validation
      • Capture new records                                 • Duplicate detection
      • Incremental ETL                                     • Orphan record checks
      • Pipeline Audit Logging                              • Negative amount validation
                    │
                    └─────────────────────────┬─────────────────────────┘
                                              ▼
                             Automation & Orchestration
                  • Snowflake Tasks (Scheduled every minute)
                  • Stored Procedures
                  • Automated Incremental Loading
                                              │
                                              ▼
                            Gold Layer (Business Ready Data)
                  • CUSTOMER_SALES
                  • PRODUCT_SALES
                  • MONTHLY_REVENUE
                                              │
                                              ▼
                           Dimensional Modeling (Star Schema)
                  ┌─────────────────────────────────────────────────┐
                  │ DIM_CUSTOMERS                                  │
                  │ DIM_PRODUCTS                                   │
                  │ FACT_ORDERS                                    │
                  └─────────────────────────────────────────────────┘
                                              │
                                              ▼
                               Business Analytics Views
                  • VW_CUSTOMER_ANALYTICS
                  • VW_PRODUCT_ANALYTICS
                  • VW_REVENUE_DASHBOARD
                                              │
                                              ▼
                               Reporting & Business Insights
                  • Customer Performance
                  • Product Performance
                  • Revenue Trends
                  • Sales Analytics
                  • Dashboard Integration (Power BI/Tableau)
