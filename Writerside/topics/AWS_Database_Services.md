# AWS Databases
Database is basically an application that stores data.

## Types of Databases (Datastores)
There are three types of databases:
- Self-Managed Data stores
- SQL/Relational Data stores
- NoSQL Data stores

## Structured Data VS Unstructured Data

![image_96.png](image_96.png)
Lets use the above diagram to explain a relational database.
Assuming we have buses an in one bus we have Gordon and in the other we have Marconi .
If we need to find Gordon we need to go to Row 1 Column 3
Assuming there is a relationship between Marconi and Gordon( friends )
Then if marconi moves rows we have to update Gordon where marconi is

This is structured data and what SQL datastore are used for.

![image_97.png](image_97.png)

Assuming now we just come and ask if there is Gordon in the bus and  Gordon raises his hand.
Here we just use a key like 'name ' to search


![image_98.png](image_98.png)
In Structured data stores , the buses represents tables and the tables have relationship with each other.
Data her is a bit structured and organized.
Used primarily when you have complex relationship with your data
Think Transactional (like banking) or reporting use cases for these data stores

![image_99.png](image_99.png)
On the other side we just need to know a key like 'movieId' or 'bookName' and just search it.
NoSQL is good for search.
Used when you have simple but specific needs for data
Think search, High performance, Documents, Relationship use case.

## Self-Managed Data stores

![image_100.png](image_100.png)

Assuming a database is a car and you want full control of everything
Own the car entirely (Own the database)
Drive it (In charge of the database)
Repair the car ( Repair database in case of any issue)
Customize the Car (Customize it how you want it, make updates too)
Fully Responsible for the car ( You in charge of everything about the database)

If you decide to use EC2 Virtual Machines or ECSor EKs that is a Self-Managed Database.

- Can run  your own  database software on EC2 or any container services (ECS or EKS)
- Increased control and Flexibility
- Increased Operational overhead and responsibility
- Mainly used when you have specific software or security requirements.

![image_101.png](image_101.png)

