# Benchmarking-between-spark-and-mahout
Time Performance and Accuracy comparison in between machine learning libraries of Spark and Mahout


Installed VMWare Player and extracted the files of CloudEra.
Ran the CloudEra Application file on the VMPlayer.
Installed Mahout and Spark on VMPlayer
Activated Hue Environment in CloudEra.
Uploaded Data using file browser to put Data into Hadoop File System.
Google Drive was used to move Data from local machine to client machine.


Activated the HUE environment in CloudEra by using the default credentials.
Data which is downloaded from the google drive was uploaded to HDFS by creating a directory.
Created a HIVE table in Hadoop and performed basic hive SQL such as Joins, Various Select Statements with different where clause commands. 
Sample Query: SELECT a.* FROM a JOIN b ON (a.id = b.id AND a.department = b.department)
Visualized the status of map- reduce Hadoop jobs in CloudEra.


MAHOUT: Mahout is a data-mining system, to the point that regularly runs combined with the Hadoop foundation at its experience to oversee gigantic volumes of information.
Mahout bolsters four fundamental information science use cases: 
COLLABORATIVE FILTERING – mines client conduct and makes item suggestions (e.g. Amazon proposals) 
CLUSTERING – takes things in a specific class, (for example, site pages or daily paper articles) and arranges them into actually happening gatherings, such that things fitting in with the same gathering are like one another 
CLASSIFICATION – gains from existing classifications and after that allocates unclassified things to the best class 
FREQUENT ITEM - set mining – examines things in a gathering (e.g. things in a shopping basket or terms in a question session) and afterward recognizes which things regularly seem together.


SPARK: Spark is a quick and general motor for huge scale information preparing. 

Sparkle MLlib is a conveyed machine learning system on top of Spark Core that, due in expansive part of the disseminated memory-based Spark engineering, is as much as nine times as quick as the plate based usage utilized by Apache Mahout and scales superior to anything Vowpal Wabbit. Many regular machine learning and measurable calculations have been actualized and are dispatched with MLlib which disentangles substantial scale machine learning pipelines.

Classification and regression: bolster vector machines, logistic relapse, direct relapse, choice trees, gullible Bayes grouping 

Collaborative filtering methods including Alternating Least squares (ALS)
 
Clustering investigation techniques including k-means, and Latent Dirichlet Allocation (LDA) 


####Comparison Results

The primary contrast will be originated from hidden systems. In the event of Mahout it is Hadoop MapReduce and if there should arise an occurrence of MLib it is Spark. To be more particular - from the distinction in per work overhead.
As far as my understanding Spark takes less time in computing the iterative computations when compared to mahout because of its in-memory computing.
To explain well let us take an example where an algorithm needs to complete 1000 cycles to be completed for accomplishing a task,

Let us consider that it takes 20 seconds for each computation then the total time taken by each of the technology would be 
Mahout total time taken would be= 1000* 20 secs=20000 seconds.
Spark total time taken would be=1*20sec +999* 1 second=1019 seconds.
This huge difference is because the mahout map-reduce frame requires to fetch data from Hadoop distributed file system each and every iteration, but when it comes to spark it first takes the data from hdfs and create an rdd in memory and if any iterative operations occur instead of fetching data from hdfs it checks whether the data required is there in memory and performs operations.
This is the reason for spark lightening speeds when compared to mahout mahout-map-reduce. 

![Diagramatic representation of this program](https://github.com/chaithu123/Benchmarking-between-spark-and-mahout/blob/master/x.jpg)
![Diagramatic representation of this program](https://github.com/chaithu123/Benchmarking-between-spark-and-mahout/blob/master/y.jpg)
![Diagramatic representation of this program](https://github.com/chaithu123/Benchmarking-between-spark-and-mahout/blob/master/z.jpg)
![Diagramatic representation of this program](https://github.com/chaithu123/Benchmarking-between-spark-and-mahout/blob/master/zz.jpg)
