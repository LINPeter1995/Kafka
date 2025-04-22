# Kafka

有Web UI 介面

http://localhost:19900/overview

官網

https://kafka.apache.org/documentation/

Module 1：Introduction to Kafka and the Ecosystem

 1-1：WhyApache Kafka
 
 1-2：Use cases of Apache Kafka
 
 1-3：Kafka ecosystem Architecture & Administration Monitoring Tools
 
Module 2：Basic Concepts of Apache Kafka

 2-1：Topics and partitions
 
 2-2：Broker
 
 2-3：Producer & Consumer
 
Module 3：Hands-on Practice of Apache Kafka

Windows  - Go into Kafka docker container
  
 • Start Docker Desktop
 
 • $ cd $env:USERPROFILE\Desktop
 
 • $ git clone https://github.com/semicolon1709/kafka-tutorial-docker-env.git
 
 • $ cd kafka-tutorial-docker-env
 
 • $ docker-compose up -d
 
 • $ docker exec -it kafka bash

 kafka-topics --create \
 
  --bootstrap-server localhost:9092 \
  
  --replication-factor 1 \
  
  --partitions 1 \
  
  --topic test


 
