**🍽️ End-to-End Zomato Food Delivery Lakehouse Project using Databricks**
_______________________________________________________________________________________________________________________
**📌 Overview**

This project implements a complete Lakehouse architecture using Databricks on a Zomato-like food delivery dataset.
It integrates data from multiple sources such as orders, customers, restaurants, and delivery partners to generate meaningful business insights.
________________________________________________________________________________________________________________________
**🎯 Business Problem**

A food delivery platform operates across multiple cities with data stored in separate systems, making it difficult to:

Track total revenue across cities
Monitor delivery performance
Analyze customer behavior
Identify top-performing restaurants
Understand order and sales trends

This project builds a single source of truth using a Lakehouse solution for better decision-making.
_____________________________________________________________________________________________________________________________
**📂 Dataset**

Source: Zomato Food Delivery Insights Dataset (Kaggle)
Records: ~1500+ orders

**📊 Tables Used:**
orders (main dataset)
customers (~500 records)
restaurants (~200 records)
delivery (~1500 records)
delivery_persons (~500 records)

**🔑 Key Columns:**
order_id, customer_id, restaurant_id
order_date, delivery_time, status
total_amount, payment_mode, discount, feedback
___________________________________________________________________________________________________________________________
**🏗️ Architecture**

This project follows the Medallion Architecture:

**🥉 Bronze Layer**
Raw data ingestion from CSV files
Stored as Delta tables
No transformations applied
**🥈 Silver Layer**
Data cleaning and preprocessing
Handling null values and duplicates
Fixing invalid data (wrong dates, negative values)
Standardizing formats
Joining multiple datasets (orders + customers + restaurants + delivery)
**🥇 Gold Layer**
Aggregated and business-ready data
KPI tables for analytics and dashboards
_____________________________________________________________________________________________________________________________
**⚙️ Technologies Used**
Databricks
PySpark
SQL
Delta Lake
_____________________________________________________________________________________________________________________________
**🔄 Workflow**
Load raw datasets into Bronze layer
Perform cleaning and transformation in Silver layer
Join all datasets into a unified structure
Use Delta operations:
MERGE (incremental loads)
UPDATE and DELETE
Apply:
Schema Evolution
Time Travel
Build Gold layer tables for analytics
____________________________________________________________________________________________________________________________
**📈 Key Insights**
💰 Total Revenue by City
🍴 Top Restaurants by Orders
📅 Daily & Monthly Order Trends
🚚 Delivery Time Analysis
👥 Customer Segmentation (High-value customers)
🌆 Top Cities by Orders
🔁 Repeat Customer Analysis
📊 Executive KPI Dashboard
____________________________________________________________________________________________________________________________
**🚀 How to Run**
Upload dataset to Databricks
Create Bronze tables using PySpark
Clean and transform data into Silver layer
Join datasets and apply Delta operations
Create Gold tables using SQL
Run queries to generate insights and dashboards
_____________________________________________________________________________________________________________________________
**👥 Team Roles**
Ingestion Engineer – Handles data loading and Bronze layer
Transformation Engineer – Data cleaning, joins, Silver layer
Analytics Engineer – Builds Gold KPIs and dashboards
_____________________________________________________________________________________________________________________________
**🧠 Learnings**
Medallion Architecture (Bronze–Silver–Gold)
Delta Lake operations (MERGE, UPDATE, DELETE)
Schema Evolution & Time Travel
Data transformation using PySpark
Building real-world data engineering pipelines
____________________________________________________________________________________________________________________________
**📦 Deliverables**
Databricks Notebooks
SQL Scripts
Screenshots
Gold Tables
README Documentation
Final Presentation
