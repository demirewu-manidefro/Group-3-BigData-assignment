#  BIG DATA ANALYTICS ASSIGNMENT

##  Group Members

| No. | Name                     | ID Number     |
|-----|--------------------------|---------------|
| 1 | **Demirewu Manidefro** | DBU1501123 |
| 2 | **Lamrot Solomon** | DBU1501315 |
| 3 | **Mikiyas Tolko** | DBU1501375 |
| 4 | **Nahom Teshome** | DBU1500984 |
| 5 | **Yonas Abebe** | DBU1501655 |
| 6 | **Abaynewu Aberu** | DBU1501615 |
| 7 | **Yonas Habtamu** | DBU1501578 |

---

 *Submitted as part of the Big Data Analytics course project.*

 **SUMITTED TO: inst  Derbew Felasman**   
 **Institution:** Debre Berhan University  
**Department:** Datascience
**SUBMISSION DATE:** 29,OCT 2025

---

                                                
                                                                
# Design and Implementation of a Data Pipeline and ETL Process for NYC Yellow Taxi Trip Data

##Introduction
This project presents the **end-to-end design and implementation** of an ETL (Extract, Transform, Load) pipeline for the **NYC Yellow Taxi Trip dataset**.  
The primary objective is to extract raw trip data, clean and transform it into a usable format, and load it into a **PostgreSQL database** for analytics.  
Through this project, we demonstrate practical expertise in **data engineering**, **Python-based automation**, and **business intelligence pipeline design**.

---

##Objectives
- Efficiently extract and process large-scale datasets using **Python** and **Pandas**.  
- Perform **data cleaning, transformation, and enrichment** for analytical readiness.  
- Load transformed data into **PostgreSQL** with a well-structured schema.  
- Maintain data integrity through **reference tables** and **foreign key relationships**.  
- Enable **querying and CRUD operations** for flexible data management.  

---

##Data Source
- **Dataset:** NYC Yellow Taxi Trip Data (January 2025)  
- **Size:** ~3.47 million rows  
- **Format:** Parquet  
- **Key Columns:**  
  `VendorID`, `tpep_pickup_datetime`, `tpep_dropoff_datetime`, `passenger_count`,  
  `trip_distance`, `payment_type`, `fare_amount`, `tip_amount`, `taxes`, and `surcharges`.

**Business Relevance:**  
This dataset supports analyses such as **ride demand forecasting**, **driver performance evaluation**, and **revenue optimization**.

---

##ETL Process

###1 Extract
- Data was read from a **Parquet file** for speed and memory efficiency.  
- Conducted initial inspection to detect **missing values**, **duplicates**, and **format inconsistencies**.

### 2 Transform
- **Data Cleaning:** Replaced or removed missing and inconsistent values in key fields.  
- **Derived Features:** Created new metrics such as `trip_duration`, `pickup_hour`, and `pickup_date`.  
- **Standardization:** Renamed columns and enforced consistent data types.  
- **Validation:** Filtered out invalid or zero-distance trips to maintain accuracy.

###3 Load
- Implemented **chunked data loading** to handle millions of rows without memory overload.  
- Successfully loaded ~3.47 million records into PostgreSQL table **`trips`**.  
- Added **indexes** on key columns to boost query performance.

---

##Database Management

### Schema Design
A relational schema was designed consisting of:
- **Main Table:** `trips`
- **Reference Tables:**  
  - `vendors`  
  - `rate_codes`  
  - `payment_types`  
  - `locations`

**Foreign key constraints** were enforced to ensure referential integrity.

### CRUD Operations
Demonstrated database interactions include:
- Inserting new trip records  
- Querying trips by pickup or payment type  
- Updating fare or tip details  
- Deleting invalid or test data  

---

##Results
- Built a **robust and scalable ETL pipeline** for large datasets.  
- Achieved a fully **cleaned, enriched, and standardized dataset**.  
- Schema design ensured **data consistency** and **efficient querying**.  
- Verified CRUD functionality for **business analytics workflows**.

---

##Conclusion
This project successfully delivers a **functional and maintainable ETL pipeline** using **Python, Pandas, and PostgreSQL**.  
It demonstrates the complete **data lifecycle** — from ingestion to transformation and storage — while ensuring **data quality, integrity, and usability**.  
The final system forms a foundation for **data-driven decision-making** and can be extended for **real-time analytics**.

---

##Future Enhancements
- Automate the ETL pipeline for **scheduled or continuous ingestion**.  
- Implement **data validation** and **anomaly detection** modules.  
- Optimize the database with **partitioned tables** and **advanced indexing**.  
- Integrate with **BI tools** (Power BI, Tableau) for **interactive dashboards** and reporting.  

---

##Technologies Used
| Category | Tools / Libraries |
|-----------|------------------|
| Language | Python 3.x |
| Data Processing | Pandas, PyArrow |
| Database | PostgreSQL |
| ORM / Connection | SQLAlchemy, psycopg2 |
| File Format | Parquet |
| Version Control | Git, GitHub |


