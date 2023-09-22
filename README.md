# Azure Data Pipeline
The purpose of this project was to get hands on experience with designing and implementing an end-to-end data pipeline for large datasets on Azure Cloud service.

### Architecture
![Architecture](Data%20Architecture.png)

## Pipeline
### Data Factory
Integrated the data from CSV files and loaded them into Data Lake.
Each copy is a file being extracted and loaded into a data lake container.
![Factory](Data%20factory.png)

### Data Lake Storage Gen2

The files are loaded into 'raw-data' folder under the 'tokyo-olympic-data' container.
![Storage](Storage.png)

### Databricks
The data was processed and transformed utilizing PySpark on Databricks on a standard cluster provisioned on Databricks. After the transformations were made, the files were loaded into 'transformed-data' folder in data lake.

![Transformations](Databricks.png)

### Synapse Analytics
Data was loaded from 'transformed-data' folder in the data lake and loaded onto dare warehouse for querying and analytics.

![Warehouse](warehouse.png)

![Analytics](queries.png)