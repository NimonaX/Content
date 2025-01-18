# Apache Spark

## What is Apache Spark
Apache spark is a unified analytics engine for big data processing. it is known for its speed, ease to use
and support for wide range applications.

## Key Features :
+ In Memory Processing : Spark Processes data in memory, making much faster then traditional disk based system 
like Haddop.

+ Unified Engine : It supports batch Processing, Stream Processing, machine Learning, Graph processing and SQL Operations 
within a single Framework.

+ Ease to Use : It Provides APIs in multiple languages, including Python, Java, Scala and R

+ Support for various Data Source : Can integrate with Hadoop HDFS(Distibuted File System), S3, Cassandra, MongoDB and more.

+ Distributed Computing : Runs Computations across multiple nodes in a cluster

## What is Nodes and Types :
Nodes refer to the individual machine or servers that make a cluster. Spark Operates on a disributed computing model, and each node in the cluster plays specific role to executing jobs.

#### Types of Nodes :
+ 1- Driver Node: Responsible for scheduling task, maintaining information about spark application, and run main program 
creates the SparkSession and SparkContext.

+ 2- Worker Node: These Node performs actual data processing, worker node store intermediate data during prcessing and communicate with the driver.

+ 3- Cluster Manger Node: Resposnsible for allocates resources(CPU, memory) to the driver and worker nodes, and monitors health 
of the cluster.
Example :
Standalone Mode : Sparks built-in cluster 
YARN : Used with Hadoop cluster 
Kubernetes: for containerzied applications 
Mesos : A general purpose cluster manager.


## What are the main features of Apache Spark?
Main features of Apache Spark are as follows:
+ Performance: The key feature of Apache Spark is its Performance. With Apache Spark we can run programs up to 100 times faster than Hadoop MapReduce in memory. On disk we can run it 10 times faster than Hadoop.
+ Ease of Use: Spark supports Java, Python, R, Scala etc. languages. So it makes it much easier to develop applications for Apache Spark.
+ Integrated Solution: In Spark we can create an integrated solution that combines the power of SQL, Streaming and data analytics.
  R+ un Everywhere: Apache Spark can run on many platforms. It can run on Hadoop, Mesos, in Cloud or standalone. It can also connect to many data sources like HDFS, Cassandra, HBase, S3 etc.
+ Stream Processing: Apache Spark also supports real time stream processing. With real time streaming we can provide real time analytics solutions. This is very useful for real-time data.

## What is a Resilient Distribution Dataset in Apache Spark?
RDD is a fundamental data structure in apache spark it is an immutable, distributed collections of objects that can be processed in parallel across a cluster.

+ Resilient: Fault-tolerant with the ability to rebuild data in case of failures
+ Distributed: Data is distributed across multiple nodes in a cluster
+ Dataset: Collection of partitioned data with primitive values or values of any type

## Key characteristics of RDDs:

+ Immutability: Once created, RDDs cannot be modified. Any transformation creates a new RDD.
+ Lazy Evaluation: Transformations on RDDs are lazy, meaning they aren't executed until an action is called. 
example :
            #This transformation isn't executed yet
            mapped_rdd = rdd.map(lambda x: x * 2)
            #The computation happens when we call an action
            result = mapped_rdd.collect()

+ In-memory Computing: RDDs can be cached in memory for faster access.
+ Parallel Processing: Operations can be performed in parallel across the cluster.

## What is a Transformation in Apache Spark?
Transformation in Apache Spark is a function that can be applied to a RDD. Output of a Transformation is another RDD. Transformation in Spark is a lazy operation. It means it is not executed immediately. Once we call an action, transformation is executed. A Transformation does not change the input RDD. We can also create a pipeline of certain Transformations to create a Data flow.


## What are security options in Apache Spark?
Apache Spark provides following security options:
Encryption: Apache Spark supports encryption by SSL. We can use HTTPS protocol for secure data transfer. Therefore data is transmitted in encrypted mode. We can use spark.ssl parameters to set the SSL configuration.

Authentication: We can perform authentication by a shared secret in Apache Spark. We can use spark.authenticate	to configure authentication in Spark.
Event Logging: If we use Event Logging, then we can set the permissions on the directory where event logs are	stored.	These permissions can ensure access control for Event log.


## How will you monitor Apache Spark?
We can use the Web UI provided by SparkContext to monitor Spark. We can access this Web UI at port 4040 to get the useful information. Some of the information that we can monitor is:
+ Scheduler tasks and stages RDD	Sizes	and	Memory usage Spark	Environment Information
+ Executors Information
+ Spark also provides a Metrics library. This library can be used to send Spark information to HTTP, JMX, CSV files etc.This is another option to collect Spark runtime information for monitoring another dashboard tool.

## What are the main libraries of Apache Spark?
Main libraries of Apache Spark are as follows:
+ MLib: This is Spark’s Machine Learning library. We can use it to create scalable machine learning system. We can use various machine learning algorithms as well as features like pipelining etc with this library.
+ GraphX: This library is used for computation of Graphs. It helps in creating a Graph abstraction of data and then use various Graph operators like- SubGraph, joinVertices etc.
+ Structured Streaming: This library is used for handling streams in Spark. It is a fault tolerant system built on top of Spark SQL Engine to process streams.
+ Spark SQL: This is another popular component that is used	for	processing	SQL queries on Spark platform.
+ SparkR: This is a package in Spark to use Spark from R language. We can use R data frames, dplyr etc from this package. We can also start SparkR from RStudio.


## What are the main functions of Spark Core in Apache Spark?
Spark Core is the central component of Apache Spark. It serves following functions:
+ Distributed Task Dispatching
+ Job Scheduling
+ I/O Functions


## How will you do memory tuning in Spark?

In case of memory tuning we have to take care of these points.

- Amount of memory used by objects Cost of accessing objects Overhead	of Garbage Collection.
- Apache Spark stores objects in memory for caching. So it becomes important to perform memory tuning in a Spark application. First we determine the memory usage by the application. To do this we first create a RDD and put it in cache. Now we can see the size of the RDD in storage page of Web UI. This will tell the amount of memory consumed by RDD. Based on the memory usage, we can estimate the amount of memory needed for our task. In case we need tuning, we can follow these practices to reduce memory usage:
- Use data structures like Array of objects or primitives instead of Linked list or HashMap. Fastutil library provides convenient collection classes for primitive types compatible with Java.
- We have to reduce the usage of nested data structures with a large number of small objects and pointes. E.g. Linked list has pointers within each node.
- It is a good practice to use numeric IDs instead of Strings for keys.
- We can also use JVM flag `-XX:+UseCompressedOops` to	make pointers be four bytes instead of eight.

## What are the two ways to create RDD in Spark?
We can create RDD in Spark in following two ways:
+ Internal: We can parallelize an existing collection of data within our Spark Driver program and create a RDD out of it.
+ External: We can also create RDD by referencing a Dataset in an external data source like AWS S3, HDFS, HBASE etc.

## What are the main operations that can be done on a RDD in Apache Spark?
There are two main operations that can be performed on a RDD in Spark:
+ Transformation: This is a function that is used to create a new RDD out of an existing RDD.
+ Action: This is a function that returns a value to Driver program after running a computation on RDD.


## What are the common Transformations in Apache Spark?
Some common transformations in Apache Spark are as follows:
+ Map(func): This is a basic transformation that returns a new dataset by passing each element of input dataset through func function.
+ Filter(func):	This transformation returns a new dataset of elements that return true for func function. It is used to filter elements in a dataset based on criteria in func function.
+ Union(other Dataset): This is used to combine a dataset with another dataset to form a union of two datasets.
+ Intersection(other Dataset):	This transformation gives the elements common to two datasets.
+ Pipe(command, [envVars]): This transformation passes each partition of the dataset through a shell command.


## What are the common Actions in Apache Spark?
Some commonly used Actions in Apache Spark are as follows:
+ Reduce(func): This Action aggregates the elements of a dataset by using func function.
+ Count(): This action gives the total number of elements in a Dataset.
+ Collect(): This action will return all the elements of a dataset as an Array to the driver program.
+ First(): This action gives the first element of a collection.
+ Take(n): This action gives the first n elements of dataset.
+ Foreach(func): This action runs each element in dataset through a for loop and executes function func on each element.


## What is a Shuffle operation in Spark?
Shuffle operation is used in Spark to re-distribute data across multiple partitions. It is a costly and complex operation. In general a single task in Spark operates on elements in one partition. To execute shuffle, we have to run an operation on all elements of all partitions. It is also called all-to-all operation.


## What are the operations that can cause a shuffle in Spark?
Some of the common operations that can cause a shuffle internally in Spark are as follows:
+ Repartition
+ Coalesce
+ GroupByKey
+ ReduceByKey
+ Cogroup
+ Join


## What is purpose of Spark SQL?
Spark SQL is used for running SQL queries. We can use Spark SQL to interact with SQL as well as Dataset API in Spark. During execution, Spark SQL uses same computation engine for SQL as well as Dataset API. With Spark SQL we can get more information about the structure of data as well as computation being performed. We can also use Spark SQL to read data from an existing Hive installation. Spark SQL can also be accessed by using JDBC/ODBC API as well as command line.


## What is a DataFrame in Spark SQL?
A DataFrame in SparkSQL is a Dataset organized into names columns. It is conceptually like a table in SQL.In Java and Scala, a DataFrame is a represented by a DataSet of rows. We can create a DataFrame from an existing RDD, a Hive table or from other Spark data sources.

## What is a Parquet file in Spark?
Apache Parquet is a columnar storage format that is available to any project in Hadoop ecosystem. Any data processing framework, data model or programming language can use it. It is a compressed, efficient and encoding format common to Hadoop system projects. Spark SQL supports both reading and writing of parquet files. Parquet files also automatically preserves the schema of the original data. During write operations, by default all columns in a parquet file are converted to nullable column.


## What is the difference between Apache Spark and Apache Hadoop MapReduce?
Some of the main differences between Apache Spark and Hadoop MapReduce are follows:
+ Speed: Apache Spark is 10X to 100X faster than Hadoop due to its usage of in memory processing.
+ Memory: Apache Spark stores data in memory, whereas	Hadoop MapReduce stores data in hard disk.
+ RDD: Spark uses Resilient Distributed Dataset (RDD) that guarantee fault tolerance. Where Apache Hadoop uses replication of data in multiple copies to achieve fault tolerance.
+ Streaming: Apache Spark supports Streaming with very less administration. This makes it much easier to use than Hadoop for real-time stream processing.
+ API: Spark provides a versatile API that can be used with multiple data sources as well as languages. It is more extensible than the API provided by Apache Hadoop.
