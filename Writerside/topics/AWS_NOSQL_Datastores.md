# AWS NOSQL Data Sores

## Amazon DynamoDB
This is 'The lightning-fast king of key-value at AWS'

If you want to create blobs of data that you can search for with a single keyword or phrase we use **Amazon DynamoDB**
![image_110.png](image_110.png)

## DocumentDB
We use this Service when we want to retrieve a document like essays, profiles and more like collections of data.
![image_109.png](image_109.png)

## Keyspaces (Cassandra Compatibility)
you use these when you want a database that can run in many different locations across the planet and you need large-scale unstructured data.
![image_111.png](image_111.png)

## Neptune
When you need a database that will detect relationship between data like fraud detector or social network relationship this is when you use **Amazon Neptune** 
![image_112.png](image_112.png)

## ELasticCache
Sometimes you need a database that can cache expensive database results and be able to get it faster.
Here you need to store data in a location that is faster than my regular database.
We have two databases:

![image_113.png](image_113.png)
Here you will have your app listening to the cache but if something is not in the ache then we will have to go to the database but it will be a bit slow.
![image_114.png](image_114.png)

## OpenSearch Service
When you want a database that you can use to search through a bunch of information like a google search that give you relevant or related results, here you use 
**Amazon OpenSearch Service**
![image_115.png](image_115.png)

## Amazon Quantum Ledger Database Services
A database where everytime you modify a number or a transaction it keeps a record of it ( more like blockchain).It's great for security consistency.
Example databases:

![image_116.png](image_116.png)

## Timestream
This is the database you use when collecting data from IOT devices and you need a database that captures data from various sources at high scale and maintains the timestamp.
![image_117.png](image_117.png)
Good for collecting Logs from multiple devices
![image_118.png](image_118.png)
