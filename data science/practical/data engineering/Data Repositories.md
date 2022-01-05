## Data Lake 💧
Unstructured, highly flexible pool of raw data

- Vast pool of raw data
- File-based (essentially just a file bucket!) + Meta data
- Purpose not yet clear
- More flexible: Quick to update / add data
- Aimed at data scientists, more technical personel
- Cons
	- Data quality can easily deteriorate => can turn into a data swamp

## Data Warehouse 📦️
More structured collection of processed data

- Repository of structured, filtered data
- Data has been processed
- Is already in use for e.g. BI
- Not as quick to update
- Aimed at BI
- Can be organized into sections of data marts, with each data mart organized around a specific business function

## Data Lakehouse 🌈
- Tries to combine the benefits of data lake and warehouse
- Kind of a proprietary idea of databricks
- Data Lake with Meta Data for Datasets (e.g. versioning) and ACID Transactions

## Databases ⏹️
- Can be contained within data warehouses
- Can be relational or not

### Relational
- Tabular form
- Well defined structure / schema
	- Can specify and enforce relationships and constraints
- Queried via [[SQL - Structured Query Language|SQL]]
- Highly optimized for fast querying 
- Typically [[ACID Transactions|ACID]] compliant 

### Non-Relational (NoSQL)
- Usually more flexible than relational
- 4 types
	- Key-Value Store
		- e.g. Redis, Memcached, DynamoDB
	- Document Based
		- e.g. MongoDB, DocumentDB, CouchDB, Cloudant
	- Column Based
		- e.g. Cassandra, Apache hbase
	- Graph Based
		- e.g. Neo4J, CosmosDB
- For less structured data
- Often used for bigger data
- NoSQL = not only SQL
- Often *not* [[ACID Transactions|ACID]] compliant