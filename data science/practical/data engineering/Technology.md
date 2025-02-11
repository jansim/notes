## Dealing with Big Data

- Apache Spark ✨
	- Distributed analytics framework for complex, realtime analytics
	- General purpose processing engine for many use-cases
	- Works in-memory and only uses disk when memory is constrained
	- Can run on itself or ontop of e.g. hadoop
- Apache Hadoop 🐘
	- Distributed storage and processing
	- Reliable, scalable, cost-effective
	- no format requirements
	- supports new / emerging data formats
	- Quick access to data
	- HDFS: Hadoop Distributed File System
		- Big files are split across nodes in the network, analyses are run on nodes
		- Incl replication / redundancy
- Apache Hive 🐝
	- [[Data Repositories#Data Warehouse 📦️|Data Warehouse]] for querying and analysis
	- Querying system built ontop of Hadoop
	- High latency (i.e. slow!)
	- Good for ETL etc.