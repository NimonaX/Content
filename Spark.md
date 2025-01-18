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
Resilient Distribution Dataset (RDD) is an abstraction of data in Apache Spark. It is a distributed and resilient collection of records spread over many partitions. RDD hides the data partitioning and distribution behind the scenes.
Main features of RDD are as follows:
+ Distributed: Data in a RDD is distributed across multiple nodes.
+ Resilient: RDD is a fault- tolerant dataset. In case of node failure, Spark can re- compute data.
+ Dataset: It is a collection of data similar to collections in Scala.
+ Immutable: Data in RDD cannot be modified after creation. But we can transform it using a Transformation.

