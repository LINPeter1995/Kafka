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

# 在 Windows PowerShell 執行 
 
cd $env:USERPROFILE\Desktop 切到桌面資料夾
 
git clone https://github.com/semicolon1709/kafka-tutorial-docker-env.git 用 git clone 下載範例專案
 
cd kafka-tutorial-docker-env 進入專案資料夾
 
docker-compose up -d 用 docker-compose 啟動 Kafka、Zookeeper 等容器

# 進入 Kafka Docker 容器後執行
 
docker exec -it kafka bash

進入容器裡的 Linux 終端機

root@<container_id>:/#     

在這裡你才能下 Kafka CLI 的指令
 
kafka-topics --create \ 表示你要「建立（create）」一個新的 Topic
 
--bootstrap-server localhost:9092 \ 指定 Kafka 伺服器的位置。這裡的 localhost:9092 是 Kafka Broker 的位址和 port
  
--replication-factor 1 \ 表示這個 Topic 的資料副本數量是 1。Kafka 支援高可用性，一個 Topic 可以有多個副本
  
--partitions 1 \ 表示這個 Topic 有 1 個 partition。Partition 是 Kafka 用來水平切分資料的方式，與並行處理有關
  
--topic test 這是你要建立的 Topic 名稱，這裡叫做 test


 
