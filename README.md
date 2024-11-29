# Wikimedia Producer and OpenSearch Consumer  

This project streams real-time data from Wikimedia using **Kafka** and stores it in **OpenSearch** for efficient querying and analysis. The Kafka producer fetches live updates from Wikipedia and sends them to a Kafka topic, while the consumer processes the data and ingests it into an OpenSearch cluster.  

## Features  
- **Real-Time Data Streaming**: Streams live changes from Wikimedia using Kafka.  
- **Seamless Integration with OpenSearch**: Indexes and stores data for querying.  
- **Scalable and Fault-Tolerant Architecture**: Leverages Kafka's distributed messaging system.  

## Architecture  
1. **Kafka Producer**: Connects to Wikimedia's API and streams changes to a Kafka topic.  
2. **Kafka Consumer**: Reads from the Kafka topic and sends processed data to OpenSearch.  
3. **OpenSearch**: Stores indexed data, enabling fast searches and analytics.  

## Requirements  
- **Kafka**: Apache Kafka installed and configured.  
- **OpenSearch**: An OpenSearch cluster set up and running.  
- **Python** (or language of choice for producer/consumer scripts).  

## Setup  
1. **Kafka Setup**:  
   - Install Kafka and start the Zookeeper and Kafka servers.  
   - Create a topic (e.g., `wikimedia.recentchange`).  

   ```bash
   bin/kafka-topics.sh --create --topic wikimedia.recentchange --bootstrap-server localhost:9092
   ```

2. **OpenSearch Setup**:  
   - Install and configure OpenSearch.  
   - Set up an index for Wikimedia data 

3. **Producer**:  
   - Use Wikimedia's API to fetch live changes.  
   - Send data to Kafka.  

4. **Consumer**:  
   - Read data from Kafka and ingest into OpenSearch.  

## Usage  
1. Start the Kafka producer to fetch live Wikimedia changes.  
2. Start the Kafka consumer to process data and ingest it into OpenSearch.  
3. Query the data in OpenSearch for analytics and insights.  
