#Spark worker
FROM franzbertani/spark-cluster:base

EXPOSE 8081

ENTRYPOINT /home/spark/bin/spark-class org.apache.spark.deploy.worker.Worker spark://master:7077
