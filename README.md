# Assignment-2.2
1.	HDFS-The HDFS(Hadoop distributed file system) is the component of Hadoop framework for the storage and access of data in Hadoop cluster.The file store in HDFS provides scalable, fault-tolerant storage at low cost. • The HDFS software detects and compensates for hardware issues, including disk problems and server failure. HDFS has been designed keeping in view of the following features: • Very large files: Files that are megabytes, gigabytes, terabytes, or petabytes of size. • Streaming data access: HDFS is built around the idea that data is written once but read many times. A dataset is copied from source and then analysis is done on that dataset over time. • Commodity hardware: Hadoop does not require expensive, highly reliable hardware as it is designed to run on clusters of commodity hardware.



2.Hadoop cluster-A Hadoop cluster is a special type of computational cluster designed specifically for storing and analyzing huge amounts of unstructured data in a distributed computing environment. Such clusters run Hadoop's open source distributed processing software on low-cost commodity computers. Typically one machine in the cluster is designated as the NameNode and another machine the as JobTracker; these are the masters. The rest of the machines in the cluster act as both DataNode and TaskTracker; these are the slaves. Hadoop clusters are often referred to as "shared nothing" systems because the only thing that is shared between nodes is the network that connects them. 
Hadoop clusters are known for boosting the speed of data analysis applications. They also are highly scalable: If a cluster's processing power is overwhelmed by growing volumes of data, additional cluster nodes can be added to increase throughput. Hadoop clusters also are highly resistant to failure because each piece of data is copied onto other cluster nodes, which ensures that the data is not lost if one node fails.



3.	HDFS Blocks- Hadoop distributed file system also stores the data in terms of blocks. However the block size in HDFS is very large. The default size of HDFS block is 128MB. The files are split into 128MB blocks and then stored into the hadoop filesystem. The hadoop application is responsible for distributing the data blocks across multiple nodes. 
The benefits with HDFS block are: 

•	The blocks are of fixed size, so it is very easy to calculate the number of blocks that can be stored on a disk.
•	HDFS block concept simplifies the storage of the datanodes. The datanodes doesn’t need to concern about the blocks metadata data like file permissions etc. The namenode maintains the metadata of all the blocks.
•	If the size of the file is less than the HDFS block size, then the file does not occupy the complete block storage.
•	As the file is chunked into blocks, it is easy to store a file that is larger than the disk size as the data blocks are distributed and stored on multiple nodes in a hadoop cluster.
•	Blocks are easy to replicate between the datanodes and thus provide fault tolerance and high availability. Hadoop framework replicates each block across multiple nodes (default replication factor is 3). In case of any node failure or block corruption, the same block can be read from another node.
	
