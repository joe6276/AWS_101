# Compute Services

In order to run an application we need servers in order to deploy our code.

Before AWS :

You needed to find a data center or build a data center then:
![image_85.png](image_85.png)

This is time-consuming , costly and involved multiple people.

With AWS a Server is Just a Click-away. The service responsible for providing servers in the cloud is an EC2.

## Amazon EC2 
EC2 allows you to provision a server on AWS within minutes, it provides secure, resizable compute capacity in the cloud

There is a potential that An AWS server has several EC2 instances deployed there.
VPCs are used to logically isolate each customers' infrastructure.
![image_86.png](image_86.png)


If you are using a physical server you will have to install an operating system but what about EC2 instances?

### Amazon Machine Images(AMI)

AMI is an image that provides the information required to launch an EC2 instance.

AMI is a blueprint that contains information such as what operating system and what software/packages should be installed on an instance.

We can use one AMI for multiple EC2 instances. Think of AMI as an installer disk used for installing a new Server
![image_87.png](image_87.png)

AMI Can be fully customized to:
- Add application source code 
- Add dependencies
- Customize OS firewall

If you are shopping for a physical server there will be specifications that you will consider e.g. Memory, CPUs even storage
Now how does that happen in the cloud.
### Instance Types

EC2 provides a wide selection of instance types optimized to fit different use cases.

Instance types have varying combination of CPU, Memory, storage, and Networking capacity.
They are just different server models to select from.

There are different types:
#### General Purpose

- Provide a good balance of compute, memory and networking resources
- Can be used for diverse workloads
- Ideal for applications that use resources in equal proportions 

#### Compute Optimized
- Optimized for compute-heavy applications
- Contain high-performance CPUs
- Ideal  for batch processing workloads, media transcoding, machine learning and gaming servers.

#### Memory Optimized 

- Deliver fast performance for memory-intensive workloads
- Suited for database

#### Storage Optimized
- Optimized for workloads that require high, sequential read and write access to large data sets on local storage.
- Can deliver tens of thousands of low-latency, random I/O operations per second (IOPS)

#### Accelerated Computing
- Utilize hardware accelerators to perform expensive calculations 
- Great for graphics processing and data pattern matching 

## EC2 Pricing

### On-demand Pricing
Here you pay for compute capacity by the hour. 
Only billed when instance is running:
- Still charged for storage attached to instance 
NO upfront payment or long-term commitment
- Great for short-term, irregular or unpredictable workloads.

### Spot Pricing

Amazon tries to maximize the usage of their servers. For example if they have a machine with 64GB and the EC2
instances running inside the machine only use 20 GB then 44GB is idle.
![image_88.png](image_88.png)
Instead of it being idle, Amazon offers spare compute capacity at discounted rates
Spot instances are recommended for:
- Applications that have flexible start time and end time
- Applications that need low compute prices
Not suitable for application that cannot tolerate interruptions.

### Reserve Pricing
Reserve instance is a billing discount that allows you to save on your EC2 costs.
Offers discounted rates when reserved for a certain period (1year or 3 year contract)

When purchasing a reserved instance, you are not actually buying an instance. You are merely committing to using
an on-demand instance for a long-term period.

When you deploy an on-demand instance with matching attributes as the reservation(instance type, region, platform), it will be charged at the reserved price and not the default.

![image_89.png](image_89.png)
In the above diagram,what reserved instance means is any instance that is M3.Large you will be charged as a reserved instance 
but any other type of instance you will be charged as an On-demand instance.
