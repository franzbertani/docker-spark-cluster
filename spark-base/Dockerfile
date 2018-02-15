#Spark base image
FROM ubuntu

RUN apt-get update && apt-get install -y \
 wget \
 default-jdk \
 python2.7 \
 scala && cd / && mkdir spark &&  cd /spark && \
 wget https://www.apache.org/dist/spark/spark-2.2.0/spark-2.2.0-bin-hadoop2.7.tgz && \
 tar -xvf spark-2.2.0-bin-hadoop2.7.tgz && \
 cd / && mkdir hadoop && cd /hadoop && \
 wget https://archive.apache.org/dist/hadoop/core/hadoop-2.8.0/hadoop-2.8.0.tar.gz && \
 tar -xvf hadoop-2.8.0.tar.gz 

ENV JAVA_HOME /usr/lib/jvm/java-1.8.0-openjdk-amd64 
ENV SPARK_HOME /spark/spark-2.2.0-bin-hadoop2.7
ENV HADOOP_HOME /hadoop/hadoop-2.8.0
ENV CORE_CONF_fs_defaultFS=hdfs://namenode:8020

RUN export PATH=/hadoop/hadoop-2.8.0/bin:$PATH

COPY ./core-site.xml /hadoop/hadoop-2.8.0/etc/hadoop
COPY ./hdfs-site.xml /hadoop/hadoop-2.8.0/etc/hadoop
