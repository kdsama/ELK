

run:
	make restart  

topics: 
	docker exec -it kafka /opt/bitnami/kafka/bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --partitions 1 --replication-factor 1 --topic applogs


listtopics:
	docker exec -it kafka /opt/bitnami/kafka/bin/kafka-topics.sh --list --zookeeper zookeeper:2181 


listenAPPLOGS:
	docker exec -it kafka /opt/bitnami/kafka/bin/kafka-console-consumer.sh --bootstrap-server 172.17.0.1:9092 --topic er --from-beginning
writeAPPLOGS:
	docker exec -it kafka /opt/bitnami/kafka/bin/kafka-console-producer.sh --broker-list 172.17.0.1:9092 --topic applogs

