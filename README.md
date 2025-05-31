# 🍕 Pizza ETL Data Pipeline: A Medallion Architecture Exploration (Landing, Bronze, Silver)

## Project Overview

This repository showcases a hands-on data pipeline development project, designed to illustrate the principles of a robust, layered data architecture using the **Medallion Architecture (Landing, Bronze, Silver layers)**. Developed within a practical 'pizza ETL data pipeline' scenario, this project transforms raw data into clean, refined datasets ready for analysis. It was a fantastic learning experience focusing on scalable data ingestion, transformation, and management.

## 🚀 Features & What You'll Find

* **Comprehensive Data Pipeline:** End-to-end ETL (Extract, Transform, Load) process demonstrated.
* **Medallion Architecture Implementation:** Practical application of Landing, Bronze, and Silver data layers for organized and governed data.
    * **Landing Zone:** Initial raw data capture and storage.
    * **Bronze Layer:** Storing raw, untransformed data.
    * **Silver Layer:** Refining raw data through cleansing, transformation, and standardization.
* **Efficient Data Storage:** Utilization of **Parquet format** for optimized performance and columnar storage at both Bronze and Silver layers.
* **Database Integration:** Management and querying of data using **SQL Server Management Studio (SSMS)**.
* **Scenario-Based Learning:** A relatable 'pizza ETL data pipeline' scenario to understand real-world data challenges.

## 🛠️ Technologies & Tools Used

* **Microsoft SQL Server:** For database hosting, schema management, and data querying.
* **Python:** The primary language for scripting the ETL processes, data manipulation, and pipeline orchestration.
* **Parquet:** A columnar storage file format used for efficient data storage and retrieval.
* **Medallion Architecture:** A data architecture pattern implemented to structure the data lake into distinct layers (Landing, Bronze, Silver).

## 🏛️ Medallion Architecture Breakdown

This project strictly adheres to the Medallion architecture pattern, ensuring data quality, governance, and scalability:

1.  **🛬 Landing Zone:**
    * **Purpose:** The initial staging area for raw data, exactly as it arrives from source systems. No transformations occur here.
    * **Role in Project:** Simulates the entry point for our raw 'pizza order' data.

2.  **🥉 Bronze Layer:**
    * **Purpose:** Stores raw, ingested data in its original format. Acts as a historical archive and a source for subsequent layers.
    * **Implementation:** Raw data from the Landing Zone is moved here and stored efficiently in **Parquet format**. This layer ensures data traceability and immutability.

3.  **🥈 Silver Layer:**
    * **Purpose:** Focuses on refining the data from the Bronze layer. This involves cleansing, standardizing, filtering, and applying basic transformations.
    * **Implementation:** Transformed data from the Bronze layer is processed, cleaned, and then stored in **Parquet format**, making it suitable for analysis and downstream consumption.

## 🍕 The Pizza ETL Data Pipeline Scenario

Imagine a system handling pizza orders! This project simulates an ETL pipeline where:
* **Raw order data** (e.g., customer details, pizza toppings, prices) enters the **Landing Zone**.
* This data is then moved to the **Bronze Layer** for raw storage.
* The **Silver Layer** takes this raw data, cleans it (e.g., standardizing topping names, ensuring valid prices), calculates derived metrics (e.g., total order cost), and structures it for easier analysis.
* **SSMS** would be used to manage the database, query the refined data, and potentially set up tables for further reporting or consumption.

## 📊 Data Flow & Project Steps

1.  **Data Ingestion:** Raw pizza order data is brought into the **Landing Zone**.
2.  **Bronze Layer Load:** Data from the Landing Zone is copied into the **Bronze Layer**, stored in **Parquet files**.
3.  **Silver Layer Transformation:** Python scripts read data from the Bronze Layer, perform specified transformations (cleansing, standardization, aggregation), and write the refined data to the **Silver Layer** as **Parquet files**.
4.  **Database Integration:** (Optional/Conceptual) The refined Silver Layer data can then be loaded into SQL Server tables for reporting or further consumption, managed via SSMS.


## 🙏 Learning & Acknowledgements

This project was an incredible learning experience, deepening my understanding of modern data architecture and Python-based ETL processes.

A huge thank you to **Mr. Alif Irfan**, Senior Data Engineer, for his exceptional guidance and for fostering such an engaging and hands-on learning environment. His insights were invaluable.

I also want to acknowledge my talented friends and collaborators, **Nurul Erina** and **Nur Farah Adibah**, for their partnership and shared learning journey.

