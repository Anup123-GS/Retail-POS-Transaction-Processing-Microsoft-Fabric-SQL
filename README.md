# Retail POS Transaction Processing Using Microsoft Fabric

## Project Overview
Built an automated data pipeline using Microsoft Fabric to process retail POS transaction CSV files and load data into a Fabric Data Warehouse.

## Technologies Used
Microsoft Fabric | Lakehouse | Data Warehouse | SQL | Data Pipelines

## Pipeline Flow
**CSV Files → Lakehouse → Get Metadata → ForEach → Copy Data → Staging Table → SQL UPSERT → Gold Table**

## Key Features
- Ingested multiple CSV files dynamically using Get Metadata and ForEach.
- Used Copy Data to load transactions into a staging table.
- Implemented TRUNCATE to refresh staging data before each load.
- Developed a SQL stored procedure to update existing transactions and insert new records.
- Used `last_updated` timestamps to identify newer transactions.
- Maintained consolidated transaction records in the Gold table.
