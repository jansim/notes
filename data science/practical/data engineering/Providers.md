# Databricks 🧱
- Provides hosted service / unified platform with data lakehouse and tools
	- Tools: redash for BI, data science workspace (jupyter-like + UI for underlying spark cluster), mlflow, delta lake
- Allows parallelization of ETL pipeline
- Sits on top of existing data lake or other storage provider
- Allows streaming processing / ingestion of data as well
- Advertises a three-tier system of data quality
	- 🥉 Bronze: Raw, unprocessed data
	- 🥈 Silver: Processed, transformed => filtered, cleaned, augmented
		- Why silver tables in-between? Chances are that they may serve as the basis for multiple Gold tables, so this way 
	- 🥇 Gold: Aggregated, prepared for analytics / ML
- Delta Lake (part of the service)
	- Can unify static and streaming data sources
	- Implements [[ACID Transactions]]

# Microsoft Azure 🟦
- Azure Data Factory
	- Serverless ETL
- Azure Analytics
- 


# Snowflake ❄️
TODO