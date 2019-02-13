# spark-streming-examples

Examples of Apache Spark Streaming
These examples have been made during the course https://www.udemy.com/taming-big-data-with-spark-streaming-hands-on/

🦜🦜🦜
Twitter
=======

To execute the twitter example we need to create a twitter App in https://developer.twitter.com/en/apps
and fill the twitter.txt in the resources path with the credentials of our app.

Netcat
======
To execute most of the examples locally, it is necessary it's necessary to execute the netcat command in a Shell.
https://docs.oracle.com/cd/E86824_01/html/E54763/netcat-1.html

We can use this command to create a streaming of example with a text file.

* Mac Example:
     > nc -kl 7777 < src/main/resources/access-log.txt


Kafka
=====
To execute the Kafka example we need to download Apache Kafka locally and Create a Topic
1. Download from https://kafka.apache.org/downloads
2. We can read the https://kafka.apache.org/quickstart to run Apache Kafka.

  2.1 Start the server:
        > bin/zookeeper-server-start.sh config/zookeeper.properties

  2.2 Create a topic:
        > bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic testLogs

  2.3 Create a console producer:
        > bin/kafka-console-producer.sh --broker-list localhost:9092 --topic testLogs < src/main/resources/access_log.txt
