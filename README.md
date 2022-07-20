# BigData-Airline_Data_Analysis
Airline data analysis using Hive, Druid &amp; Quicksite on AWS

## Introduction to Big data

● Real time streaming data being captured at regular intervals of time from millions of IOT devices like 
sensors,clickstreams,logs from the device APIs and historical data from SQL databases.
● To store the huge volumes of data with high velocity and veracity ,we need an efficient scalable storage 
system which is distributed across different nodes either in local or in cloud. 
● Here comes the Hadoop concept which can be classified into two groups -Storage and processing 
● Storage will be done in HDFS and processing is done using Map reduce
● Initially the processing of this data used to be done in Java by writing mapreduce programs with controller 
services. Now a days lot of tools have been developed on top of map reduce such as Hive ,Presto,Druid etc 
which can be directly used by their built in SQL interfaces and are much faster due to inbuilt indexing of 
the data.
● Underlying storage will be HDFS for all kinds of big data scenarios and underlying processing is Map 
reduce in most of the cases.

## Introduction to Data Pipeline

● It refers to a system for moving data from one system to another. The data may or may not 
be transformed, and it may be processed in real time (or streaming) instead of batches.
● Right from extracting or capturing data using various tools , storing raw data,cleaning, 
validating data, transforming data into query worthy format ,visualisation of KPIs including 
Orchestration of the above process is data pipeline.
● Scalability, reliability, security should be taken into consideration in each step of data 
pipeline building in big data environments.
● Transformed data can be used to derive KPIs and derive initial insights from the data for 
exploratory analysis
● Further analysis of data using ML algorithms can be used to derive predictions out of the 
data either historical or near real time 

## Business Impact of building data pipelines

● Saves time and effort for actuaries,BI analysts
● Manual process of cleaning, validating of raw data takes on an average of 3-4 hours of 
time for each and every raw file received at a certain interval of time.
● Automating this simple process saves 3-4 hours for each run.
● Similarly automation of ETLs using Cron,Oozie, Airflow processes etc saves effort and 
time for Data engineers as well as Analysts.
● Only pipeline monitoring and maintenance needs to be taken care of once the pipeline is 
built.
● Grabbing the data from source to destination-sources being APIs, Google sheets ,Local 
systems ,SQL based databases etc. Destination systems can be HDFS for storage , 
Kafka,Flume,Storme,Logstash to grab real time streaming data

## Overview

Process to gather streaming data from Airline API using NiFi & batch data using AWS redshift using Sqoop and 
build a data pipeline to analyse the data using Apache Hive and Druid and compare the performances ,to discuss 
the hive optimization techniques and visualise the data using AWS Quicksight
● Extract streaming data from APIs at a certain interval of time using NiFi.
● Extract the batch data from RDS using sqoop and store into HDFS .
● Parse the data using Nifi which pushes the data into Kafka topic to send streaming data in turn directly to 
Druid.
● Extract the data from HDFS into hive and druid to analyse,optimize and compare performance of each of the 
tools .
● Perform ETLs on Hive table vs ETLs during druid data ingestion. 
● Orchestrate the above process using Airflow
● Visualize the KPIs or metrics in AWS Quicksight

