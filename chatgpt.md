🟢【初階】搞懂 Kafka 是什麼、基本概念與操作
🎯 學習目標：
知道 Kafka 是什麼、為什麼使用它

能用基本指令操作 Topic / Producer / Consumer

📘 內容重點：
Kafka 是什麼？

分散式的訊息佇列系統（Message Queue）

高吞吐量、耐錯、可以持久化訊息

類似郵差系統：Producer 傳送、Kafka 儲存、Consumer 接收

核心元件

Broker：Kafka Server 本體

Topic：訊息分類的單位（像資料夾）

Partition：Topic 的分片（可同時處理提高效能）

Producer：發送訊息的角色

Consumer：接收訊息的角色

Zookeeper（舊版）：管理 broker，目前用 KRaft 取代中

常見指令與操作

kafka-topics --create

kafka-console-producer

kafka-console-consumer

docker-compose up 啟動 Kafka 環境

基本流程

Producer 傳資料 → Kafka → Consumer 收資料

🟡【中階】進入實戰應用與管理層面
🎯 學習目標：
開始開發 Kafka 應用程式

能使用程式碼傳送/接收資料

瞭解 Kafka 的架構與錯誤處理

📘 內容重點：
使用 Python / Java 來寫 Producer & Consumer

Python：confluent_kafka 套件

Java：kafka-clients

自訂 Consumer Group / offset

多個 Consumer 同時處理訊息（平行處理）

auto.offset.reset、enable.auto.commit

錯誤與重新連線機制

error_cb、KafkaError、timeout 設定

壓縮 / 序列化

訊息壓縮（gzip, snappy）

JSON、Avro 等格式處理

Kafka Connect / Sink / Source

把 Kafka 跟 MySQL / MongoDB / Elasticsearch 串接

用 Kafka 做 ETL 前處理、串流處理架構

🔴【進階】大型系統設計與監控
🎯 學習目標：
建構企業級 Kafka 架構

瞭解 Kafka 的內部運作與效能優化

管理數百萬筆資料流

📘 內容重點：
高可用架構設計

多 Broker、多 Partition

設定 replication.factor 是每個 partition 在 Kafka cluster 中會被複製的副本數量

Kafka 的 leader election 機制

效能優化

Consumer poll 的頻率

Producer 批次傳送 / async 傳送

調整 linger.ms, batch.size, acks

監控與管理工具

Kafka Manager、Control Center、JMX

Prometheus + Grafana 監控指標（lag、throughput）

Kafka Streams / KSQLDB

實現實時資料流分析

資料 join / 聚合

安全性與權限管理

SSL、SASL 認證機制

ACL 設定與多租戶權限控制

分區重分配 / 增加 partition

如何不中斷服務下調整 topic 結構

✅ 建議進修順序（可以搭配做 side project）：
操作 Kafka CLI → 熟悉基本流程

用 Python 寫 Producer & Consumer → 懂邏輯

架 Docker Kafka、寫一套串流流程

用 Kafka Connect 拉資料（例如：MySQL → Kafka → MongoDB）

學 Kafka Streams 或 Kafka Connect + Spark 做 ETL 流程

部署完整系統 + 加上監控工具

