# Large Scale Machine Learning

## Data 

### Data Ingestion 
Streaming ingestion involves: 
* **Clickstream** : an ordered series of interactions that users have with some interface. 
* **Change data capture**: process of recording changes within a databade system. 
* **Live video**

**Clickstream tools**

KAFKA 
* Open source software platform which provides a way to handle real-time data streaming. 
* If clickstream logs come at a faster pace than the broker can handle you need more brokers. 
*
file:///home/mariana.almeida/Imagens/kafka.png![image](https://user-images.githubusercontent.com/39881974/216361735-a50acd67-c1d2-46ff-9862-237224da64dc.png)

KAFKA x Rest APIs 
* Kakfa APIs are used to implement data pipelines, real-time data streams, etc. On the other hand, a **REST API**  is used to act as a bridge between client and server. The client requests data from the server, and the server sends back a response. 
* With Kafka APIs, you publish and subscribe to topics. With the REST API, you request and await a response. It is also done on demand.
* Kafka APIs store data in topics. With REST APIs, you can store data in the database on the server.
* With Kafka API, you often are not interested in a response. You are typically expecting a response back when using REST APIs.
* Kafka provides bidirectional communication. The REST API is unidirectional, i.e., you can only send or receive a response at a time.

AMAZON KINESIS 
* Amazon Kinesis is an Amazon Web Service designed to process large-scale data streams from a multitude of services in real-time. It can be considered, like Apache Kafka, as a kind of message broker. This means that it operates as a middleman between various data generating sources, to allow other applications or services to work with the source data.
* With Amazon Kinesis, you can ingest real-time data such as video, audio, application logs, website clickstreams, and IoT telemetry data for machine learning, analytics, and other applications.
* Data is sent from producers to shards and from them to the consumers. 
* How to ingest data is called 'change data capture' 
* 
### Data Storage 
* **Parquet**: a column oriented data-storage format provided by Apache. 

### Data Processing 

### Processing Orchestration 

## Exploration

### Workspaces 

## Experimentation 

### Frequentist AB Testing 

### Bayesian AB Testing 

### Multi Armed Bandit 

## Large Scale Training 

### Basic Models 

### Deep learning models 

### Model Validation 
