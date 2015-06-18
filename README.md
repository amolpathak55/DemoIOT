Demo IoT pipeline -
Spark streaming consumer gets events from MQTT broker and writes to Cassandra
Main java class takes 3 arguments - MQTT broker URL (tcp://brokerhost:1883), MQTT Topic name and Cassandra Host.

Cassandra needs to have the schema populated like below 
CREATE KEYSPACE ks WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 1};
CREATE TABLE ks.cf (id UDID PRIMARY KEY, payload TEXT);
