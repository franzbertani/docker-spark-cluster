#Spark Master
FROM franzbertani/spark-cluster:base

EXPOSE 8080 7077 6066

ENTRYPOINT ["/home/spark/spark-2.1.1-bin-hadoop2.6/bin/spark-class","org.apache.spark.deploy.master.Master"]
