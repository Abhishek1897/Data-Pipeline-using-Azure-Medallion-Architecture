# 🌊 Build Data Pipeline using Azure Medallion Architecture

## 📘 Project Overview
This project demonstrates the end-to-end development of a **cloud-based data pipeline** using **Azure Medallion Architecture** to process and analyze **aggregated water sensor data** collected from various European countries.  

The pipeline integrates multiple Azure services — from **data ingestion** to **data transformation** to **visualization** — providing a scalable and automated framework for managing complex datasets.

Blog Link: https://medium.com/@abhishekshinde189/building-an-end-to-end-data-pipeline-on-azure-using-medallion-architecture-b780bdd1697a
---

## 🧩 Business Objective
The aim of this project is to **analyze historical water quality data** using Azure’s data engineering ecosystem.  
By leveraging Azure’s cloud-native tools, the solution ensures:
- High scalability
- Automated data orchestration
- Improved data quality and reliability
- Real-time visualization for decision-making

This architecture can be extended to use cases in **environmental monitoring**, **IoT sensor analytics**, and **governmental data integration**.

---

## ⚙️ Tech Stack
| Category | Tools/Services |
|-----------|----------------|
| **Programming** | SQL, Scala |
| **Data Storage** | Azure Managed SQL Database, Azure Blob Storage, Azure Data Lake Storage Gen2 |
| **Orchestration** | Azure Data Factory |
| **Automation** | Azure Logic Apps |
| **Processing** | Azure Databricks |
| **Visualization** | Power BI |

---

## 🧱 Architecture
The project is designed following the **Medallion Architecture** pattern, which structures data into three progressive layers:

1. **Bronze Layer:**  
   Raw ingestion of data from **Azure SQL Database** into **Azure Data Lake Storage Gen2** using **Azure Logic Apps** and **Data Factory**.

2. **Silver Layer:**  
   Data cleaning, transformation, and deduplication using **Azure Databricks** (Spark).

3. **Gold Layer:**  
   Aggregated, analytics-ready data stored in **Databricks tables** and visualized in **Power BI** dashboards.

![Architecture Diagram](architecture-diagram.png)  
*(Add your architecture diagram image here)*

---

## 🧠 Use Case
This project focuses on **“Aggregated Sensor Water Data”**, where environmental agencies collect readings across:
- Different time periods
- Countries and water bodies
- Vegetation and habitat types

Key columns include:
- `countryCode`
- `observedPropertyDeterminandLabel`
- `resultMeanValue`
- `parameterWaterBodyCategory`
- `resultStandardDeviationValue`
- `procedureAnalyticalMethod`

Each record contributes to determining the concentration of substances in water, enabling better **environmental assessment and decision-making**.

---

## 🔄 Workflow Summary

### 1. **Data Ingestion**
- Upload raw Excel/CSV data to **Azure SQL Database** using **SSMS** or **Azure Data Studio**.
- Create Logic Apps workflow to **automate extraction** from SQL Database.

### 2. **Data Movement**
- Use **Azure Logic App** to fetch data from SQL DB and store it as JSON in **Azure Blob Storage**.
- Use **Azure Data Factory** to orchestrate the transfer from **Blob Storage** → **Data Lake Storage Gen2**.

### 3. **Data Processing**
- Apply the **Medallion Architecture** using **Azure Databricks**:
  - **Bronze:** Raw ingestion
  - **Silver:** Clean and normalize
  - **Gold:** Aggregate and model for BI

### 4. **Visualization**
- Connect **Power BI** to Databricks tables for real-time dashboards.  
- Use **DAX** to derive metrics and KPIs.

---

## 📊 Key Features
- **End-to-End Cloud Data Pipeline** – Ingest, transform, and visualize large-scale sensor data.
- **Modular Design** – Each Azure service acts as an independent, scalable component.
- **Automation** – Logic Apps handle data fetching and movement.
- **Data Quality Assurance** – Databricks Medallion architecture ensures clean, structured data.
- **Real-Time Insights** – Power BI integration enables quick and dynamic visualization.

---

## 🧰 Prerequisites
- Active [Azure Account](https://azure.microsoft.com/en-in/pricing/purchase-options/azure-account)
- Installed Tools:
  - **SQL Server Management Studio (SSMS)** *(Windows)*
  - **Azure Data Studio** *(macOS/Linux)*
  - **Power BI Desktop**
- Dataset: [Aggregated Sensor Water Data](https://s3.amazonaws.com/projex.dezyre.com/data-pipeline-with-medallion-architecture-azure/materials/Data.zip)

---

## 🚀 Execution Steps

1. **Create Azure Resource Group**
2. **Create Azure SQL Database & Import Data**
3. **Create Blob Storage and Container**
4. **Build Logic App Workflow for Data Extraction**
5. **Set up Data Factory Pipeline (Blob → ADLS Gen2)**
6. **Implement Databricks Medallion Layers (Bronze, Silver, Gold)**
7. **Visualize Results in Power BI**

Each step is detailed in the [Cookbook](Cookbook.pdf) document.

---

## 🎯 Key Learnings
- Data orchestration and pipeline automation using Azure services  
- Medallion Architecture for structured and high-quality data  
- Integration between SQL, Blob Storage, ADLS, Databricks, and Power BI  
- Security management via Azure roles and managed identities  
- Cost optimization and monitoring for Azure resources

---

## 🧾 References
- [Microsoft Learn – Azure Data Studio](https://learn.microsoft.com/en-us/azure-data-studio/)
- [Microsoft Learn – Azure Data Factory](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Microsoft Learn – Power BI](https://learn.microsoft.com/en-us/power-bi/)

---

## 🏁 Conclusion
This project demonstrates a **real-world Azure Data Engineering solution** showcasing:
- Seamless integration between Azure components  
- Medallion architecture for scalable and reliable data transformation  
- Insightful analytics through Power BI  

The final pipeline effectively transforms raw sensor readings into actionable insights that support **public safety, environmental sustainability, and policy decisions**.

---

## 🧑‍💻 Author
**Abhishek Shinde**  
🎓 Master’s in Applied Data Science, Syracuse University  
🔗 [LinkedIn](https://www.linkedin.com/in/abhishekshinde189) | [GitHub](https://github.com/Abhishek1897)



