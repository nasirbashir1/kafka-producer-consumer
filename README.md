The project generates data from Twitter feed based on the keywords provided and sends the data to kafka, wherein Elastic search consumes the data.

To start zookeeper\
zookeeper-server-start config/zookeeper.properties

To start kafka host\
kafka-server-start config/server.properties

To create "twitter_tweets" topic\
kafka-topics --zookeeper 127.0.0.1:2181 --topic twitter_tweets --create --partitions 3 --replication-factor 1

Some of the features include\
Consumer is "Idempotent",\
Offsets are manually committed,\
Acknowledgment used is "All",\
Compression used is "snappy",\
Batch size is 32 MB,\
Retries set to Integer.MAX_VALUE




