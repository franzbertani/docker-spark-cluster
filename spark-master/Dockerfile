#Spark Master
FROM spark-cluster:base

EXPOSE 8080 7077 6066

ENTRYPOINT ["/spark/spark-2.2.0-bin-hadoop2.7/bin/spark-class","org.apache.spark.deploy.master.Master"]
