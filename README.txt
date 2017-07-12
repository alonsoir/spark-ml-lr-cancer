
This is an example using Spark Machine Learning decision trees , written in Scala, 
to demonstrate How to get started with Spark ML on a MapR sandbox 

There are  1 datafile  in this directory :
	wbcd.csv 
 
You will need to copy these files to your MapR sandbox, or wherever you have Spark installed.

You can run these examples in the spark shell by putting the code from the scala file in the spark shell after launching:
 
$spark-shell 

Or you can run the applications with these steps:

Step 1: First compile the project: Select project  -> Run As -> Maven Install

Step 2: Copy the sparkflightmllab-1.0.jar to the sandbox 

To run the  standalone :

spark-submit --class example.Cancer --master yarn sparkcancermllab-1.0.jar

Alonso update

to run this, i have to invoke the project using a command like this:

/Users/aironman/spark-2.1.1-bin-hadoop2.7/bin/spark-submit --master local[*] --class solutions.Cancer target/sparkcancermllab-1.0.jar

The main class is located in a package named solutions, not example.

Using spark-2.1.1 version, i got this exception:

17/07/12 11:57:57 INFO spark.SparkContext: Created broadcast 0 from textFile at Cancer.scala:57
Exception in thread "main" java.lang.NoSuchMethodError: scala.reflect.api.JavaUniverse.runtimeMirror(Ljava/lang/ClassLoader;)Lscala/reflect/api/JavaMirrors$JavaMirror;
	at solutions.Cancer$.main(Cancer.scala:60)
	at solutions.Cancer.main(Cancer.scala)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.apache.spark.deploy.SparkSubmit$.org$apache$spark$deploy$SparkSubmit$$runMain(SparkSubmit.scala:743)
	at org.apache.spark.deploy.SparkSubmit$.doRunMain$1(SparkSubmit.scala:187)
	at org.apache.spark.deploy.SparkSubmit$.submit(SparkSubmit.scala:212)
	at org.apache.spark.deploy.SparkSubmit$.main(SparkSubmit.scala:126)
	at org.apache.spark.deploy.SparkSubmit.main(SparkSubmit.scala)





