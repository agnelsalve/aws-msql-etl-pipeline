# AWS ETL Pipeline for On-Prem MS SQL to Amazon Redshift VIA JDBC Connection 

This repository showcases a production-ready ETL pipeline that integrates on-premises MS SQL Server with AWS services via JDBC Connection(**Cost-Effective**) to enable efficient data ingestion, transformation, and visualization via Power BI.

---

## 🔧 Architecture Overview

<img width="1080" height="382" alt="image" src="https://github.com/user-attachments/assets/8b3aee67-f100-4e83-8fbe-af7bac4f6d65" />

---

## 📌 Components & Flow

1. **On-Premises MS SQL Server**  
   Source system hosting structured business data.

2. **JDBC over VPN**  
   Secure data transfer via JDBC connection established over a VPN tunnel.

3. **Visual ETL: MSSQL_to_AWS**  
   - Orchestrates extraction and writes raw data to S3 in Parquet format.

4. **AWS Glue & PySpark**  
   - Performs transformation and cleansing:
     - `POS_master_update`
     - `Parquet_conso`

5. **Business Layer**  
   - Aggregates and curates data into `final_all_data_dump`.

6. **Amazon Athena**  
   - Enables SQL-based ad-hoc querying on data in S3.

7. **Amazon Redshift**  
   - Acts as the performance-optimized warehouse for dashboard consumption.

8. **Power BI**  
   - Visualizes insights via an **On-Prem Gateway**.

---

## 📊 Business Use Case

Designed for a high-performance, scalable, and secure ETL flow to power executive dashboards and analytics in real-time with historical data processing.

---

## 📁 Repository Contents

| File/Folder            | Description                             |
|------------------------|-----------------------------------------|
| `architecture/`        | Contains architecture diagrams          |
| `docs/`                | Detailed documentation and flow notes   |

---

## 📈 Future Enhancements

- Add CI/CD pipeline for Glue job deployment.
- Implement AWS Lake Formation for fine-grained data governance.
- Enable Redshift Spectrum for direct S3 querying.

---

## 📬 Contact

For any questions or collaborations, please contact:  
**Rakesh Goyal**  
Founder, Pro Insurance Brokers Pvt. Ltd.  
Mumbai, India  
