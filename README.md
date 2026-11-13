# Food Delivery Data Warehouse (ETL)

A Data Warehousing and Mining (DWM) ETL pipeline implementation for a Food Delivery analytics system using Apache Hop.

## 📌 Project Overview
This project models and transforms raw food delivery transactional data into a star schema data warehouse containing dimension tables and a centralized fact table.

### Architecture & Data Model (Star Schema)
- **Fact Table:**
  - `Fact_Order.hpl`: Central fact table capturing order transactions, financial metrics (order amount, delivery fee, discount, tax, total amount), delivery performance metrics (delivery time in minutes), and customer ratings.
- **Dimension Tables:**
  - `Dim_Customer.hpl`: Customer demographics and geographic information (customer ID, name, city).
  - `Dim_Restaurant.hpl`: Restaurant attributes including restaurant ID, name, and cuisine type.
  - `Dim_Delivery.hpl`: Delivery partner and delivery status attributes.
  - `Dim_Date.hpl`: Date dimension for temporal analysis (order date, meal type, etc.).

## 📁 Repository Structure
```
├── Dim_Customer.hpl                  # Apache Hop pipeline for Customer Dimension
├── Dim_Date.hpl                      # Apache Hop pipeline for Date Dimension
├── Dim_Delivery.hpl                  # Apache Hop pipeline for Delivery Dimension
├── Dim_Restaurant.hpl                # Apache Hop pipeline for Restaurant Dimension
├── Fact_Order.hpl                    # Apache Hop pipeline for Orders Fact Table
├── FoodDelivery_DWM_Single_Dataset.csv # Raw food delivery dataset
└── README.md                         # Project documentation
```

## 🛠️ Tools & Technologies
- **ETL Tool:** Apache Hop (`.hpl` pipelines)
- **Data Warehouse Schema:** Star Schema (Dimensions & Fact)
- **Source Data:** CSV (Transactional food delivery records)
