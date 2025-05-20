## 🧱 Databricks Sales Lakehouse Pipeline with Medallion Architecture

This project implements a Lakehouse architecture in Databricks to process sales data in layered stages (bronze → silver → gold).

- **Bronze Layer:** Raw data storage layer  
- **Silver Layer:** Cleaned, transformed, and analysis-ready data  
- **Gold Layer:** Business intelligence-optimized layer containing dimension and fact tables  

Each layer performs distinct data processing tasks, culminating in a star schema with dimension and fact tables.

---

## 🔄 Layered Data Processing Workflow

### 1️⃣ Bronze Layer – Raw Data Ingestion 🔶

**Objective:**  
Ingest raw data from external sources and persist it within Databricks.

**Process Steps:**  
- Data is typically read in CSV format.  
- Data is stored as Delta tables forming the bronze layer.

---

### 2️⃣ Silver Layer – Cleaned and Transformed Data ◻️

**Objective:**  
Prepare raw data for analysis by performing data type conversions, removing unnecessary columns, and cleaning null values.

**Process Steps:**  
- Read data from the bronze layer.  
- Select only required columns.  
- Convert data types and formats suitable for analysis.  
- Store transformed data as Delta tables in the silver layer.  
- Merge new incoming data with existing records to update.

---

### 3️⃣ Gold Layer – Star Schema Data Modeling 🟡

**Objective:**  
Convert data into dimension and fact tables for BI and reporting, optimized for performance and usability.

---

### Dimension Tables

- **DimDate:** Extracts unique dates and enriches with day, month, year fields.  
- **DimCustomer:** Parses customer names and assigns unique customer IDs.  
- **DimProduct:** Extracts and structures product details, assigning product IDs.

---

### Fact Table

- **FactSales:** Joins silver layer data with dimension tables to create the sales fact table, serving as the primary table for sales analysis.

---

## 📌 Outcome

- Data successfully processed through layered stages (bronze → silver → gold).  
- Improved data quality, manageability, and reusability.  
- BI-optimized star schema data model established.  
- All operations performed using Delta Lake infrastructure and merge-on-read strategy.

---

## 🛠️ Technologies Used

- Databricks Notebooks  
- Apache Spark (PySpark)  
- Delta Lake  
- Azure Data Lake (Optional)  
- Lakehouse architecture

---

## Screenshots

<img width="1430" alt="1" src="https://github.com/user-attachments/assets/78495047-5058-4ea7-95f7-aeb8f124c793" />

<img width="1494" alt="2" src="https://github.com/user-attachments/assets/11b64c5c-59de-4a65-9194-da6161ffdcbc" />

<img width="1456" alt="3" src="https://github.com/user-attachments/assets/fc73c2b1-344e-449f-b299-d8d9d5286605" />

<img width="1020" alt="4" src="https://github.com/user-attachments/assets/482d1ca0-e248-439e-948a-ec3b2d900466" />

<img width="1477" alt="5" src="https://github.com/user-attachments/assets/8701064a-920b-4c38-9477-324d5b3e5b9b" />

<img width="1046" alt="6" src="https://github.com/user-attachments/assets/9610f373-ac7b-444c-b9ab-75359a91fe9d" />

<img width="1143" alt="7" src="https://github.com/user-attachments/assets/f421bf1d-23a3-4a2f-a9cc-6c21e61f62f3" />

<img width="1125" alt="8" src="https://github.com/user-attachments/assets/fa6f8b44-bf06-475e-891e-43be4829ab70" />

<img width="1303" alt="9" src="https://github.com/user-attachments/assets/26818ee9-b260-4d8e-99f2-49efb3376822" />

<img width="1120" alt="10" src="https://github.com/user-attachments/assets/47eab6e5-457e-4536-9812-bb03c57172b6" />

<img width="994" alt="11" src="https://github.com/user-attachments/assets/12ae65a2-78c1-48d6-83fc-dd42190b2946" />

<img width="1374" alt="12" src="https://github.com/user-attachments/assets/94c11f12-a3c8-4984-b6d6-11672fe177e9" />

<img width="1206" alt="13" src="https://github.com/user-attachments/assets/2c14556d-d0fb-45a3-be20-0959fe04cbef" />

<img width="1425" alt="14" src="https://github.com/user-attachments/assets/0fe55067-0a86-49fc-a840-356e4e9ae38b" />

<img width="1341" alt="15" src="https://github.com/user-attachments/assets/8a75f39f-f58a-43de-810d-6a361a62b1db" />

<img width="1460" alt="16" src="https://github.com/user-attachments/assets/0db43fcc-8daf-4c2f-be98-8ac15da072a4" />

<img width="1022" alt="17" src="https://github.com/user-attachments/assets/7aff2609-e5b9-4ac0-8c85-3d5745fcc624" />

<img width="1121" alt="18" src="https://github.com/user-attachments/assets/795407e2-c790-4a33-ba55-bf076f0c1112" />



