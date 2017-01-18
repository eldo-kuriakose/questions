## Spark
----

#### What is Apache Spark?

Spark is essentially a fast and flexible data processing framework. It has an advanced execution engine supporting cyclic data flow with in-memory computing functionalities. Apache Spark can run on Hadoop, as a standalone system or on the cloud. Spark is capable of accessing diverse data sources including HDFS, HBase, Cassandra among others

#### What is “RDD”?

RDD stands for Resilient Distribution Datasets: a collection of fault-tolerant operational elements that run in parallel. The partitioned data in RDD is immutable and is distributed in nature.

#### What does the Spark Engine do?

Spark Engine is responsible for scheduling, distributing and monitoring the data application across the cluster.

#### What is an “RDD Lineage”?

Spark does not support data replication in the memory. In the event of any data loss, it is rebuilt using the “RDD Lineage”. It is a process that reconstructs lost data partitions.

#### What is a “Spark Driver”?

“Spark Driver” is the program that runs on the master node of the machine and declares transformations and actions on data RDDs. 

#### What is SparkContext?

“SparkContext” is the main entry point for Spark functionality. A “SparkContext” represents the connection to a Spark cluster, and can be used to create RDDs, accumulators and broadcast variables on that cluster.


#### Name a few commonly used Spark Ecosystems.

* Spark SQL (Shark)
* Spark Streaming
* GraphX
* MLlib

#### What is “Spark Streaming”?

Spark supports stream processing, essentially an extension to the Spark API. This allows stream processing of live data streams. The data from different sources like Flume and HDFS is streamed and processed to file systems, live dashboards and databases

#### What is “GraphX” in Spark?

“GraphX” is a component in Spark which is used for graph processing. It helps to build and transform interactive graphs.

#### Which file systems does Spark support?

* Hadoop Distributed File System (HDFS)
* Local File system
* S3

#### List the benefits of Spark over MapReduce.
 
 * Due to the availability of in-memory processing, Spark implements the processing around 10-100x faster than Hadoop MapReduce.
 Hadoop MapReduce is highly disk-dependent whereas Spark promotes caching and in-memory data storage

#### What is a “Spark Executor”?

When “SparkContext” connects to a cluster manager, it acquires an “Executor” on the cluster nodes. “Executors” are Spark processes that run computations and store the data on the worker node.


#### Explain about transformations and actions in the context of RDDs ?

Transformations are functions executed on demand, to produce a new RDD. All transformations are followed by actions. Some examples of transformations include map, filter and reduceByKey.

Actions are the results of RDD computations or transformations. After an action is performed, the data from RDD moves back to the local machine. Some examples of actions include reduce, collect, first, and take.


#### How can you minimize data transfers when working with Spark?

Minimizing data transfers and avoiding shuffling helps write spark programs that run in a fast and reliable manner. The various ways in which data transfers can be minimized when working with Apache Spark are:

* Using Broadcast Variable- Broadcast variable enhances the efficiency of joins between small and large RDDs.
* Using Accumulators – Accumulators help update the values of variables in parallel while executing.
* The most common way is to avoid operations ByKey, repartition or any other operations which trigger shuffles.
