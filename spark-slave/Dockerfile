#Spark worker
FROM spark-cluster:base

EXPOSE 8081

ENTRYPOINT /spark/spark-2.2.0-bin-hadoop2.7/bin/spark-class org.apache.spark.deploy.worker.Worker spark://master:7077
