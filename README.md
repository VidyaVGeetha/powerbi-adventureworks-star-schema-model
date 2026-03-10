# Power BI Star Schema Data Modeling – AdventureWorks

## Project Overview

This project demonstrates how to design a **Star Schema data model in Power BI** using the AdventureWorks dataset. The goal is to create a structured and optimized data model that supports efficient business reporting and analysis.

The project focuses on identifying fact and dimension tables, configuring relationships, and implementing best practices for Power BI data modeling.

---

## Business Scenario

AdventureWorks is a global manufacturing company that wants to analyze its sales performance across different products, regions, and salespeople.

However, raw datasets often contain multiple tables that are not structured optimally for analysis. To enable effective reporting and faster queries, the company requires a **Star Schema data model**.

As a Data Analyst, the task was to transform the available datasets into a structured data model that supports efficient analysis of sales performance.

---

## Dataset Tables

The dataset contains four tables:

**Sales (Fact Table)**  
Contains transactional sales data.

Columns include:

- SalesOrderNumber
- OrderDate
- ProductKey
- EmployeeKey
- SalesTerritoryKey
- Quantity
- Unit Price
- Sales
- Cost

---

**Product (Dimension Table)**  
Contains product information such as:

- Product
- Category
- Subcategory
- Standard Cost

---

**Region (Dimension Table)**  
Contains geographical information:

- Country
- Region
- Group
- SalesTerritoryKey

---

**Salesperson (Dimension Table)**  
Contains employee information:

- EmployeeKey
- Salesperson
- Title

---

## Data Modeling Approach

The **Sales table** was identified as the **Fact Table** because it contains transactional sales records and numerical measures.

The remaining tables were identified as **Dimension Tables**.

### Relationships Created

| From Table | Column | To Table | Column | Cardinality |
|------------|--------|----------|--------|-------------|
Sales | ProductKey | Product | ProductKey | Many-to-One |
Sales | EmployeeKey | Salesperson | EmployeeKey | Many-to-One |
Sales | SalesTerritoryKey | Region | SalesTerritoryKey | Many-to-One |

The filter direction was configured as **Single Direction**, following Power BI best practices.

---

## Star Schema Structure
Product
|
Region — Sales — Salesperson

The **Sales table acts as the central fact table**, while Product, Region, and Salesperson serve as dimension tables.

---

## Validation Steps Performed

Several validation steps were conducted to ensure model accuracy:

✔ Verified primary and foreign key relationships  
✔ Confirmed correct data types for key columns  
✔ Ensured correct cardinality (Many-to-One)  
✔ Checked relationship activation status  
✔ Verified filter direction (Single Direction)  
✔ Confirmed fact table measures are numeric  

---

## Skills Demonstrated

This project demonstrates the following data analytics skills:

- Power BI Data Modeling
- Star Schema Design
- Fact and Dimension Table Identification
- Relationship Configuration
- Data Model Optimization
- Data Validation

---

## Tools Used

- Microsoft Power BI
- AdventureWorks Dataset
- Data Modeling Best Practices

---

## Author

Vidya V Geetha  
Aspiring Data Analyst | Power BI | Python | SQL | APIs
