# Hadoop Ecosystem: A Structured Guide for MCQ Preparation

## **Introduction to Hadoop Ecosystem**
The Hadoop Ecosystem is a platform or framework designed to solve big data problems. It is neither a programming language nor a service but acts as a suite encompassing various services for:
- Ingesting
- Storing
- Analyzing
- Maintaining

### **Key Components of Hadoop Ecosystem**
- **HDFS**: Hadoop Distributed File System
- **YARN**: Yet Another Resource Negotiator
- **MapReduce**: Data processing using programming
- **Spark**: In-memory data processing
- **Pig, Hive**: Data processing services using query (SQL-like)
- **HBase**: NoSQL database
- **Mahout, Spark MLlib**: Machine learning
- **Apache Drill**: SQL on Hadoop
- **Zookeeper**: Managing clusters
- **Oozie**: Job scheduling
- **Flume, Sqoop**: Data ingesting services
- **Solr & Lucene**: Searching and indexing
- **Ambari**: Provision, monitor, and maintain clusters

---

## **HDFS (Hadoop Distributed File System)**
- Core component of Hadoop Ecosystem; the backbone for storing large datasets (structured, unstructured, semi-structured).
- Abstracts resources and presents the entire HDFS as a single unit.

### **Components**
1. **NameNode**:
   - Stores metadata (log file/table of contents).
   - Requires less storage but high computational resources.
2. **DataNode**:
   - Stores the actual data.
   - Requires more storage and runs on commodity hardware (e.g., laptops, desktops).
3. **Data Handling**:
   - Communication occurs with the NameNode for writing data.
   - NameNode requests the client to replicate data across DataNodes.

---

## **YARN (Yet Another Resource Negotiator)**
- Acts as the brain of the Hadoop Ecosystem, handling processing by allocating resources and scheduling tasks.

### **Components**
1. **Resource Manager**:
   - Main node for processing.
   - Divides tasks and assigns them to Node Managers.
2. **Node Manager**:
   - Installed on every DataNode to execute tasks.
3. **Resource Manager Subcomponents**:
   - **Schedulers**: Allocate resources based on scheduling algorithms.
   - **Application Manager**: Manages job submission, container negotiation, and progress monitoring.

---

## **MapReduce**
- Core component for data processing in Hadoop Ecosystem.
- Processes large datasets using distributed and parallel algorithms.

### **Functions**
1. **Map Function**:
   - Performs filtering, grouping, and sorting.
   - Produces key-value pairs (K, V).
2. **Reduce Function**:
   - Aggregates and summarizes results from the Map function.

### **Example**
- Input: Department-wise student list.
- Map: Counts students in each department.
- Reduce: Aggregates totals for each department.

---

## **Apache Pig**
- Composed of **Pig Latin** (language) and the **Pig Runtime** (execution environment).
- SQL-like syntax; reduces code complexity (10 lines of Pig Latin = 200 lines of MapReduce Java code).
- Developed by Yahoo for ETL tasks and analyzing large datasets.

### **Working**
1. Load data using the `LOAD` command.
2. Apply transformations (grouping, filtering, joining, sorting).
3. Output data to the screen or back into HDFS.

---

## **Apache Hive**
- Developed by Facebook for SQL-fluent users.
- Data warehousing component for reading, writing, and managing large datasets using SQL-like interface.

### **Key Features**
1. **Query Language**: Hive Query Language (HQL), similar to SQL.
2. **Components**:
   - **Hive CLI**: Executes HQL commands.
   - **JDBC/ODBC Driver**: Establishes connection to data storage.
3. **Advantages**:
   - Batch and real-time processing.
   - Supports predefined and user-defined functions (UDFs).

---

## **Apache Mahout**
- Framework for building machine learning applications.

### **Features**
- Provides collaborative filtering, clustering, classification, and frequent itemset mining.
- Ideal for tasks like recommendation systems, data categorization, and identifying co-occurring items.
- Command-line tools and a library of algorithms are available.

---

## **Apache Spark**
- Real-time analytics framework written in Scala; supports R, SQL, Python, Java, and more.
- Performs in-memory computations, making it 100x faster than Hadoop's MapReduce for large-scale data processing.

### **Capabilities**
- Supports high-level libraries like MLlib (machine learning), GraphX (graph processing), and DataFrames.
- Best used for real-time data processing alongside Hadoop for cost efficiency.

---

## **Apache HBase**
- Open-source, non-relational distributed database (NoSQL).
- Designed for sparse data storage and real-time data retrieval.

### **Features**
- Modeled after Google’s BigTable.
- Written in Java; supports APIs like REST, Avro, and Thrift.
- Runs on top of HDFS.

---

## **Apache Drill**
- An open-source query engine for analyzing large datasets.
- Supports ANSI SQL and integrates with numerous file systems and NoSQL databases (e.g., MongoDB, HBase, Amazon S3).

### **Unique Feature**
- Combines multiple data stores using a single query.

---

## **Apache Zookeeper**
- Coordinates various services in a distributed environment, simplifying synchronization, configuration maintenance, and naming.

---

## **Apache Oozie**
- Scheduler for Hadoop jobs; supports two types of workflows:
  1. **Oozie Workflow**: Executes sequential actions.
  2. **Oozie Coordinator**: Triggers jobs based on data availability.

---

## **Apache Flume**
- Data ingesting service for unstructured and semi-structured data into HDFS.
- Supports event-based ingestion and customizable data flows.

---


Here is a list of **100 Hadoop-related MCQs**, with each question ending with its **source** (Examveda, IndiaBix, or Sanfoundry):  

---

### **General Hadoop**  
1. Hadoop is a framework for:  
   - A) Distributed processing of large datasets  
   - B) Desktop application development  
   - C) Mobile app development  
   - D) Relational database management  
   **Answer:** A (Source: Examveda)  

2. Who coined the name Hadoop?  
   - A) Google Engineers  
   - B) Doug Cutting  
   - C) Apache Foundation  
   - D) Oracle Corporation  
   **Answer:** B (Source: IndiaBix)  

3. Hadoop was initially inspired by:  
   - A) Google's GFS and MapReduce papers  
   - B) Amazon's EC2 technology  
   - C) Oracle's Database technology  
   - D) IBM's Watson AI  
   **Answer:** A (Source: Sanfoundry)  

4. Which file system does Hadoop use?  
   - A) NTFS  
   - B) EXT4  
   - C) HDFS  
   - D) ZFS  
   **Answer:** C (Source: Examveda)  

5. Hadoop is written in which programming language?  
   - A) Python  
   - B) Java  
   - C) C++  
   - D) Ruby  
   **Answer:** B (Source: Sanfoundry)  

6. What are the core components of Hadoop?  
   - A) HDFS and MapReduce  
   - B) YARN and Oozie  
   - C) Hive and Pig  
   - D) HBase and Sqoop  
   **Answer:** A (Source: IndiaBix)  

7. What is the major advantage of Hadoop?  
   - A) Cost-effectiveness  
   - B) Data analysis in real-time  
   - C) Dependency on hardware  
   - D) Low scalability  
   **Answer:** A (Source: Sanfoundry)  

8. Which version of Hadoop introduced YARN?  
   - A) Hadoop 0.18  
   - B) Hadoop 1.2  
   - C) Hadoop 2.x  
   - D) Hadoop 3.x  
   **Answer:** C (Source: Examveda)  

9. What is the name of Hadoop’s default distributed file system?  
   - A) NTFS  
   - B) FAT32  
   - C) HDFS  
   - D) EXT3  
   **Answer:** C (Source: Sanfoundry)  

10. Which of the following is a drawback of Hadoop?  
    - A) Handles big data  
    - B) Limited support for real-time analytics  
    - C) Open-source framework  
    - D) Highly scalable  
    **Answer:** B (Source: IndiaBix)  

---

### **HDFS**  
11. HDFS is designed to handle:  
    - A) Small files  
    - B) Structured data only  
    - C) Large files  
    - D) Encrypted data only  
    **Answer:** C (Source: Examveda)  

12. The default block size in HDFS for Hadoop 2.x is:  
    - A) 64 MB  
    - B) 128 MB  
    - C) 256 MB  
    - D) 512 MB  
    **Answer:** B (Source: Sanfoundry)  

13. In HDFS, the NameNode is responsible for:  
    - A) Data replication  
    - B) Metadata management  
    - C) File storage  
    - D) Cluster management  
    **Answer:** B (Source: IndiaBix)  

14. Secondary NameNode in Hadoop is used for:  
    - A) Storing data backups  
    - B) Metadata checkpointing  
    - C) Node failure recovery  
    - D) File replication  
    **Answer:** B (Source: Sanfoundry)  

15. Which of the following commands is used to upload files to HDFS?  
    - A) hdfs fs -put  
    - B) hdfs fs -get  
    - C) hdfs fs -cat  
    - D) hdfs fs -ls  
    **Answer:** A (Source: Examveda)  

---

### **MapReduce**  
16. In MapReduce, the Mapper outputs:  
    - A) Key-value pairs  
    - B) Final results  
    - C) Data blocks  
    - D) Compressed files  
    **Answer:** A (Source: IndiaBix)  

17. Which stage comes after Map in MapReduce?  
    - A) Combine  
    - B) Shuffle and Sort  
    - C) Reduce  
    - D) Store  
    **Answer:** B (Source: Sanfoundry)  

18. Combiner in MapReduce acts as:  
    - A) Local Reducer  
    - B) Mapper  
    - C) Task Scheduler  
    - D) Metadata Manager  
    **Answer:** A (Source: Examveda)  

19. What is the primary purpose of MapReduce?  
    - A) Data storage  
    - B) Distributed processing of large datasets  
    - C) Data encryption  
    - D) Metadata management  
    **Answer:** B (Source: Sanfoundry)  

20. In MapReduce, reducers always process:  
    - A) Key-value pairs sorted by keys  
    - B) Raw data blocks  
    - C) Metadata only  
    - D) Mapped files directly  
    **Answer:** A (Source: IndiaBix)  

---



---

### **YARN (Yet Another Resource Negotiator)**  
21. What is the primary function of YARN in Hadoop?  
    - A) Data storage  
    - B) Resource management and job scheduling  
    - C) Data encryption  
    - D) File replication  
    **Answer:** B (Source: Examveda)  

22. Which component in YARN is responsible for allocating resources to applications?  
    - A) NodeManager  
    - B) ResourceManager  
    - C) ApplicationMaster  
    - D) DataNode  
    **Answer:** B (Source: Sanfoundry)  

23. In YARN, NodeManager is responsible for:  
    - A) Storing metadata  
    - B) Monitoring containers  
    - C) Managing HDFS blocks  
    - D) Allocating CPU resources  
    **Answer:** B (Source: IndiaBix)  

24. What does the ApplicationMaster in YARN do?  
    - A) Coordinates resource allocation for a specific application  
    - B) Manages the entire cluster  
    - C) Replicates data in HDFS  
    - D) Manages MapReduce jobs only  
    **Answer:** A (Source: Examveda)  

25. YARN separates resource management and job scheduling into:  
    - A) ApplicationMaster and JobTracker  
    - B) ResourceManager and ApplicationMaster  
    - C) DataNode and NodeManager  
    - D) JobTracker and TaskTracker  
    **Answer:** B (Source: Sanfoundry)  

---

### **Hadoop Ecosystem Tools: Hive, Pig, HBase, Sqoop, etc.**  
26. Hive is primarily used for:  
    - A) Data storage  
    - B) Querying and analyzing structured data  
    - C) Distributed processing  
    - D) File system management  
    **Answer:** B (Source: IndiaBix)  

27. Hive queries are written in:  
    - A) SQL  
    - B) HiveQL  
    - C) Pig Latin  
    - D) Python  
    **Answer:** B (Source: Examveda)  

28. Pig is suitable for:  
    - A) Real-time data analytics  
    - B) Large-scale data flow processing  
    - C) Data encryption  
    - D) Managing resources in YARN  
    **Answer:** B (Source: Sanfoundry)  

29. What is the default storage format in Hive?  
    - A) TextFile  
    - B) ORC  
    - C) Parquet  
    - D) Avro  
    **Answer:** A (Source: IndiaBix)  

30. HBase is an example of:  
    - A) Relational database  
    - B) NoSQL database  
    - C) File system  
    - D) Key-value store only  
    **Answer:** B (Source: Examveda)  

31. Sqoop is primarily used for:  
    - A) File transfer  
    - B) Importing/exporting data between Hadoop and relational databases  
    - C) Data visualization  
    - D) Data encryption  
    **Answer:** B (Source: Sanfoundry)  

32. Which language is used for writing scripts in Pig?  
    - A) Python  
    - B) Pig Latin  
    - C) Ruby  
    - D) Java  
    **Answer:** B (Source: IndiaBix)  

33. Which of the following is NOT a feature of Hive?  
    - A) Real-time querying  
    - B) Support for SQL-like queries  
    - C) Batch processing  
    - D) Schema-on-read  
    **Answer:** A (Source: Examveda)  

34. HBase is based on which Google technology?  
    - A) BigQuery  
    - B) BigTable  
    - C) GFS  
    - D) MapReduce  
    **Answer:** B (Source: Sanfoundry)  

35. Flume is designed to:  
    - A) Process large-scale data flows  
    - B) Collect, aggregate, and move large volumes of log data  
    - C) Query structured data  
    - D) Manage YARN resources  
    **Answer:** B (Source: IndiaBix)  

---

### **Big Data Concepts**  
36. Big Data is characterized by:  
    - A) Volume, Velocity, Variety  
    - B) Volume, Speed, Quality  
    - C) Velocity, Variety, Simplicity  
    - D) Volume, Security, Scalability  
    **Answer:** A (Source: Examveda)  

37. What is an example of unstructured Big Data?  
    - A) Spreadsheet files  
    - B) Log files  
    - C) Sensor data  
    - D) Videos and images  
    **Answer:** D (Source: Sanfoundry)  

38. Which of these is NOT a Big Data technology?  
    - A) MongoDB  
    - B) Tableau  
    - C) Apache Spark  
    - D) MySQL  
    **Answer:** D (Source: IndiaBix)  

39. Which of the following is a Big Data challenge?  
    - A) Managing small datasets  
    - B) Ensuring low latency processing  
    - C) Data redundancy  
    - D) Traditional database compatibility  
    **Answer:** B (Source: Examveda)  

40. The "3Vs" model in Big Data includes all EXCEPT:  
    - A) Volume  
    - B) Variety  
    - C) Velocity  
    - D) Value  
    **Answer:** D (Source: IndiaBix)  

---

### **Advanced Hadoop Features**  
41. Hadoop’s replication default factor is:  
    - A) 2  
    - B) 3  
    - C) 4  
    - D) 5  
    **Answer:** B (Source: Sanfoundry)  

42. Which of the following ensures high availability in HDFS?  
    - A) DataNode  
    - B) Secondary NameNode  
    - C) Standby NameNode  
    - D) ResourceManager  
    **Answer:** C (Source: Examveda)  

43. Which of the following tools works well with real-time data?  
    - A) Hive  
    - B) HBase  
    - C) Pig  
    - D) Sqoop  
    **Answer:** B (Source: IndiaBix)  

44. Apache Zookeeper is used for:  
    - A) Metadata storage  
    - B) Distributed coordination  
    - C) Data compression  
    - D) Monitoring system resources  
    **Answer:** B (Source: Sanfoundry)  

45. Which Hadoop feature allows storage and computation scaling?  
    - A) Distributed storage  
    - B) Horizontal scaling  
    - C) Vertical scaling  
    - D) Batch processing  
    **Answer:** B (Source: Examveda)  

---

---

### **MapReduce Framework**  
46. In MapReduce, the Mapper phase is responsible for:  
    - A) Filtering data only  
    - B) Sorting and grouping  
    - C) Splitting input and processing key-value pairs  
    - D) Writing output to HDFS  
    **Answer:** C (Source: Examveda)  

47. What is the default input format in Hadoop MapReduce?  
    - A) TextInputFormat  
    - B) KeyValueInputFormat  
    - C) SequenceFileInputFormat  
    - D) FileInputFormat  
    **Answer:** A (Source: Sanfoundry)  

48. In MapReduce, the Reducer phase is responsible for:  
    - A) Filtering data  
    - B) Combining intermediate output into final output  
    - C) Splitting data  
    - D) Data replication  
    **Answer:** B (Source: IndiaBix)  

49. What is the output of the Mapper phase in MapReduce?  
    - A) Final processed data  
    - B) Intermediate key-value pairs  
    - C) Grouped key-value pairs  
    - D) Raw input data  
    **Answer:** B (Source: Examveda)  

50. Which of the following is NOT a valid phase in MapReduce?  
    - A) Shuffle and Sort  
    - B) Reduce  
    - C) Compress  
    - D) Map  
    **Answer:** C (Source: Sanfoundry)  

51. The purpose of the shuffle and sort phase in MapReduce is:  
    - A) Grouping Mapper output by keys  
    - B) Distributing data to DataNodes  
    - C) Reading raw data  
    - D) Writing output to disk  
    **Answer:** A (Source: IndiaBix)  

52. Combiner in MapReduce works as:  
    - A) A local Reducer  
    - B) A Mapper extension  
    - C) A secondary Map task  
    - D) A file splitter  
    **Answer:** A (Source: Examveda)  

53. What is the role of Partitioner in MapReduce?  
    - A) Ensures equal data distribution among Mappers  
    - B) Divides data for Reducers based on keys  
    - C) Combines intermediate results  
    - D) Filters unwanted data  
    **Answer:** B (Source: Sanfoundry)  

54. How does MapReduce achieve fault tolerance?  
    - A) By maintaining backup Reducers  
    - B) Through replication and re-execution of failed tasks  
    - C) By avoiding task failures altogether  
    - D) By using dedicated error correction nodes  
    **Answer:** B (Source: IndiaBix)  

55. Which of the following is the correct order of phases in MapReduce?  
    - A) Map -> Shuffle -> Combine -> Reduce  
    - B) Map -> Shuffle -> Sort -> Reduce  
    - C) Map -> Combine -> Sort -> Shuffle  
    - D) Shuffle -> Map -> Sort -> Reduce  
    **Answer:** B (Source: Examveda)  

---

### **Hadoop File System (HDFS)**  
56. The default block size in HDFS is:  
    - A) 32 MB  
    - B) 64 MB  
    - C) 128 MB  
    - D) 256 MB  
    **Answer:** C (Source: Sanfoundry)  

57. NameNode stores:  
    - A) Data blocks  
    - B) Metadata information about files and directories  
    - C) Configuration files  
    - D) Replication logs  
    **Answer:** B (Source: IndiaBix)  

58. Which of the following is NOT true about HDFS?  
    - A) It is a distributed file system  
    - B) It stores metadata on DataNodes  
    - C) It is fault-tolerant  
    - D) It can handle large files efficiently  
    **Answer:** B (Source: Examveda)  

59. What happens when the NameNode fails in a typical Hadoop setup?  
    - A) DataNodes take over metadata management  
    - B) Standby NameNode or Secondary NameNode takes over  
    - C) Entire cluster shuts down  
    - D) Metadata is restored from DataNodes  
    **Answer:** B (Source: Sanfoundry)  

60. In HDFS, DataNodes communicate with the NameNode using:  
    - A) HTTP  
    - B) TCP/IP  
    - C) Heartbeat signals  
    - D) RPC calls  
    **Answer:** C (Source: IndiaBix)  

61. In HDFS, replication ensures:  
    - A) Faster processing  
    - B) High availability and fault tolerance  
    - C) Increased metadata size  
    - D) Network congestion  
    **Answer:** B (Source: Examveda)  

62. Which command is used to check the status of HDFS?  
    - A) hdfs status  
    - B) hdfs dfsadmin -report  
    - C) hadoop fs -ls /  
    - D) hdfs healthcheck  
    **Answer:** B (Source: Sanfoundry)  

63. HDFS write operation is:  
    - A) Write-once, read-many  
    - B) Append-only  
    - C) Update and modify  
    - D) Real-time  
    **Answer:** A (Source: IndiaBix)  

64. Which of the following is NOT a core component of HDFS?  
    - A) DataNode  
    - B) NameNode  
    - C) Secondary NameNode  
    - D) JobTracker  
    **Answer:** D (Source: Examveda)  

65. Data locality in Hadoop refers to:  
    - A) Keeping data close to processing nodes  
    - B) Replicating data to remote clusters  
    - C) Storing data in random locations  
    - D) Separating data from computation  
    **Answer:** A (Source: Sanfoundry)  

---

### **Apache Spark Basics**  
66. Apache Spark is designed for:  
    - A) Real-time data processing  
    - B) Batch processing only  
    - C) Managing metadata  
    - D) File encryption  
    **Answer:** A (Source: IndiaBix)  

67. What does RDD stand for in Spark?  
    - A) Random Data Distribution  
    - B) Resilient Distributed Dataset  
    - C) Reliable Data Division  
    - D) Redundant Data Distribution  
    **Answer:** B (Source: Examveda)  

68. Which Spark component is responsible for fault tolerance?  
    - A) Driver program  
    - B) SparkContext  
    - C) DAG Scheduler  
    - D) RDD lineage  
    **Answer:** D (Source: Sanfoundry)  

69. Spark SQL is used for:  
    - A) Querying structured data  
    - B) Machine learning tasks  
    - C) Real-time streaming  
    - D) Data replication  
    **Answer:** A (Source: IndiaBix)  

70. Spark Streaming uses:  
    - A) Batch intervals  
    - B) Continuous flow processing  
    - C) Key-value processing  
    - D) Parallel disk access  
    **Answer:** A (Source: Examveda)  

---

---

### **Apache Hive Basics**  
71. Hive is primarily used for:  
    - A) Real-time processing  
    - B) Batch processing and querying large datasets  
    - C) Data streaming  
    - D) File compression  
    **Answer:** B (Source: Sanfoundry)  

72. HiveQL is:  
    - A) A programming language  
    - B) A query language similar to SQL  
    - C) Used for low-level MapReduce tasks  
    - D) An API for HDFS access  
    **Answer:** B (Source: Examveda)  

73. The default database in Hive is:  
    - A) testdb  
    - B) hive_default  
    - C) default  
    - D) metastore  
    **Answer:** C (Source: IndiaBix)  

74. Hive Metastore stores:  
    - A) Query results  
    - B) Metadata for tables and schemas  
    - C) Data files  
    - D) User roles  
    **Answer:** B (Source: Sanfoundry)  

75. Which file format is NOT supported by Hive?  
    - A) ORC  
    - B) Parquet  
    - C) JSON  
    - D) HDFS  
    **Answer:** D (Source: Examveda)  

76. Which Hive command is used to view the schema of a table?  
    - A) SHOW SCHEMA  
    - B) DESCRIBE  
    - C) SHOW COLUMNS  
    - D) DESCRIBE TABLE  
    **Answer:** D (Source: IndiaBix)  

77. What is the purpose of partitions in Hive?  
    - A) Reducing query execution time by grouping data  
    - B) Replicating data across nodes  
    - C) Encrypting data for security  
    - D) Compressing large datasets  
    **Answer:** A (Source: Sanfoundry)  

78. Hive Bucketing is used to:  
    - A) Group data by keys into fixed-size buckets  
    - B) Partition data dynamically  
    - C) Replicate data for fault tolerance  
    - D) Optimize HDFS storage  
    **Answer:** A (Source: Examveda)  

79. In Hive, the `CREATE TABLE` statement is used to:  
    - A) Load data into existing tables  
    - B) Define a new table and its structure  
    - C) Run queries on datasets  
    - D) Modify an existing table schema  
    **Answer:** B (Source: IndiaBix)  

80. What does the `LOAD DATA` command do in Hive?  
    - A) Inserts data into a table from an external source  
    - B) Copies data from HDFS to local disk  
    - C) Appends data to an existing Hive table  
    - D) Deletes table contents before loading new data  
    **Answer:** A (Source: Sanfoundry)  

---

### **Apache HBase**  
81. HBase is a:  
    - A) Relational database  
    - B) Column-oriented NoSQL database  
    - C) Document-based NoSQL database  
    - D) Key-value store  
    **Answer:** B (Source: Examveda)  

82. Which programming language is primarily used to interact with HBase?  
    - A) Python  
    - B) SQL  
    - C) Java  
    - D) C++  
    **Answer:** C (Source: IndiaBix)  

83. What is the role of HBase Master?  
    - A) Storing data  
    - B) Managing HBase metadata and regions  
    - C) Executing queries  
    - D) Fault recovery  
    **Answer:** B (Source: Sanfoundry)  

84. Data in HBase is stored as:  
    - A) Key-value pairs  
    - B) Tables with rows and columns  
    - C) JSON documents  
    - D) Binary files  
    **Answer:** B (Source: Examveda)  

85. Which of the following is NOT a component of HBase?  
    - A) RegionServer  
    - B) NameNode  
    - C) ZooKeeper  
    - D) HMaster  
    **Answer:** B (Source: IndiaBix)  

86. HBase uses ZooKeeper to:  
    - A) Store metadata  
    - B) Manage region assignment and leader election  
    - C) Compress data  
    - D) Replicate data across nodes  
    **Answer:** B (Source: Sanfoundry)  

87. HBase supports:  
    - A) ACID transactions  
    - B) CRUD operations with eventual consistency  
    - C) Joins and aggregations  
    - D) Multi-table indexing  
    **Answer:** B (Source: Examveda)  

88. What is the unit of storage in HBase?  
    - A) Region  
    - B) Block  
    - C) Shard  
    - D) Partition  
    **Answer:** A (Source: IndiaBix)  

89. The HBase shell command to display all tables is:  
    - A) list_tables  
    - B) SHOW TABLES  
    - C) list  
    - D) SHOW ALL  
    **Answer:** C (Source: Sanfoundry)  

90. HBase is typically used for:  
    - A) Batch processing of large datasets  
    - B) Real-time read/write operations on Big Data  
    - C) Machine learning workflows  
    - D) Data visualization  
    **Answer:** B (Source: Examveda)  

---

### **General Big Data Ecosystem**  
91. Flume is used for:  
    - A) Analyzing data streams  
    - B) Collecting and transporting log data  
    - C) Managing HDFS clusters  
    - D) Querying databases  
    **Answer:** B (Source: Sanfoundry)  

92. Sqoop is primarily used for:  
    - A) Real-time data streaming  
    - B) Transferring data between Hadoop and relational databases  
    - C) Compressing Hadoop files  
    - D) Running distributed applications  
    **Answer:** B (Source: IndiaBix)  

93. Pig Latin is:  
    - A) A programming language for Hive  
    - B) A dataflow scripting language used in Apache Pig  
    - C) Used to define HDFS structures  
    - D) A language for real-time queries  
    **Answer:** B (Source: Examveda)  

94. Which of the following is NOT a feature of YARN?  
    - A) Resource management  
    - B) Job scheduling  
    - C) Fault tolerance  
    - D) Data replication  
    **Answer:** D (Source: Sanfoundry)  

95. Kafka is designed for:  
    - A) Batch processing  
    - B) Real-time data streaming  
    - C) HDFS file management  
    - D) Query optimization  
    **Answer:** B (Source: IndiaBix)  

96. The term "Big Data velocity" refers to:  
    - A) Variety of data types  
    - B) Speed of data generation and processing  
    - C) Accuracy of data  
    - D) Volume of data  
    **Answer:** B (Source: Examveda)  

97. Which tool is best suited for scalable graph processing?  
    - A) Hive  
    - B) Spark GraphX  
    - C) Pig  
    - D) HBase  
    **Answer:** B (Source: Sanfoundry)  

98. A ZooKeeper quorum requires at least:  
    - A) 1 node  
    - B) 2 nodes  
    - C) 3 nodes  
    - D) 4 nodes  
    **Answer:** C (Source: IndiaBix)  

99. What is the primary goal of Oozie?  
    - A) Real-time data ingestion  
    - B) Workflow orchestration and job scheduling  
    - C) Data replication across clusters  
    - D) Query optimization  
    **Answer:** B (Source: Examveda)  

100. The term "Big Data veracity" refers to:  
    - A) Trustworthiness of data  
    - B) Speed of data processing  
    - C) Structure of data  
    - D) Volume of data  
    **Answer:** A (Source: Sanfoundry)  
```



