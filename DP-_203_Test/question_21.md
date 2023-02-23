You are designing the folder structure for an Azure Data Lake Storage Gen2 container.

Users will query data by using a variety of services including Azure Databricks and Azure Synapse Analytics serverless SQL pools. The data will be secured by subject area. Most queries will include data from the current year or current month.

Which folder structure should you recommend to support fast queries and simplified folder security?

- a) /{SubjectArea/{DataSource}/{DD}/{MM}/{YYYY}/{FileData}_{YYYY}_{MM}_{DD}.csv
- b) /{SubjectArea/{DataSource}/{YYYY}/{MM}/{DD}/{FileData}_{YYYY}_{MM}_{DD}.csv
- c) /{YYYY}/{MM}/{DD}/{SubjectArea/{DataSource}/{FileData}_{YYYY}_{MM}_{DD}.csv
- d) /{DD}/{MM}/{YYYY}/{SubjectArea/{DataSource}/{FileData}_{YYYY}_{MM}_{DD}.csv


Correct: B.