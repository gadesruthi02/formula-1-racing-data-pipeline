# Formula 1 Racing Data Pipeline

<p align="center">
  <img src="https://i.redd.it/jcfumtrdhue61.jpg" width="800" height="400" />
</p>

# Summary 

In this project, Azure Cloud Services were utilized to design and orchestrate a data pipeline to perform data engineering operations (Ingestion, Transformation, Analysis, Load) on a Formula 1 Racing Dataset. The pipeline handles end-to-end processing from raw data ingestion to final analysis for visualization.

# Data Source

The data for all the Formula 1 races from 1950s onwards is obtained from an open source API called [Ergast Developer API](http://ergast.com/mrd/). The structure of the database is shown in the following ER Diagram and explained in the [Database User Guide](http://ergast.com/docs/f1db_user_guide.txt)

![ERDiagram](http://ergast.com/images/ergast_db.png)

# Tools

- Python
- PySpark
- Azure Databricks
- Azure Data Factory (ADF)
- Azure Data Lake Storage Gen2 (ADLS)
- Delta Lake


# Architecture

The solution used in this project is based on the "Modern analytics architecture with Azure Databricks" from the Azure Architecture Center:

<p align="center">
  <img src="https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/media/azure-databricks-modern-analytics-architecture-diagram.png" width="70%" height="70%" />
</p>


# Project Structure

1. data - contains sample raw data from Ergast API.
2. set-up - notebooks to mount ADLS storages (raw, ingested, presentation) in Databricks.
3. raw - contains SQL file to create ingested tables using Spark SQL.
4. ingestion - contains notebooks to ingest all the data files from raw layer to ingested layer. Handles the incremental data for files results, pitstopes, laptimes and qualifying.
5. trans - contains notebooks to transform the data from ingested layer to presentation layer. Notebook performs transformations to setup for analysis.
6. analysis - contains SQL files for finding the dominant drivers and teams and to prepare the results for visualization.
7. includes - includes notebooks containing helper functions used in transformations.
8. utils - contains SQL file to drop all databases for incremental load.

# About the Developer

Sruthi Gade is a Business Data Analyst with over 3 years of experience translating complex business requirements into actionable, data-driven insights. With expertise in SQL, Python, and cloud-based analytics platforms, she specializes in improving operational efficiency and end-to-end analytics delivery.

Contact Information:
- Email: gade.sruhthi02@gmail.com
- Role: Business Data Analyst