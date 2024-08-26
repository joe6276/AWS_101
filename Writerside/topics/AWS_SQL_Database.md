# SQL Data stores (Structured) 
Back to the Car database
![image_102.png](image_102.png)

We have 5 databases in this case:
![image_103.png](image_103.png)
But it hard to grow in terms if write but easy to grow in terms of read.

But what if you want something that is a bit faster .
![image_104.png](image_104.png)
This ia where Aurora comes in 

## SQL Data stores - Aurora ( really RDS Aurora)

Here they took Postgres and MySQL from the traditional RDS and made them :
- Higher capacity and higher performance
- Grows more easily that the main RDS service
- Managed services for Databases
- Cloud Native
![image_105.png](image_105.png)

But assuming again you want something that you only pay for it when you use it ( more of an uber here ) Here we have:

## Aurora Serverless V2

Again here we have a :
- Managed service for databases
- Cloud native
- Higher capacity and higher performance
- Capacity can go up and down easier than other RDs servicePay little storage, but not compute when you are not using it
![image_106.png](image_106.png)

But sometimes you have a lot of data that needs analyzing and processing reports (you need a bus not a car)

## RedShift
This is the SQL data warehouse service is SQL. Sometimes you don't want transactional database but a data warehouse.
RedShift is used when:
- When you need a data warehouse not a transactional data store
- it's the SQL data warehouse in AWS
- Petabyte scale
- Serverless and 'Server' ed versions
- Think reporting and analyzing not transactional

### Short Summary

![image_108.png](image_108.png)


