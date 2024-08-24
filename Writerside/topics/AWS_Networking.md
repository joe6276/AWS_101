# AWS Networking

In AWS you rent a slice of a machine because renting the whole machine, That means that one machine can have several customer applications.
But does that mean that they will be able to communicate with one another?
![image_66.png](image_66.png)

Amazon thought about  this and came up with VPC

## VPC

Every customer will have their application running on a private cloud  which can't communicate with another private cloud.
![image_67.png](image_67.png)
Virtual private cloud(VPC) is a secure, isolated network segment hosted within AWS.
VPC isolates computing resources from other computing resources
It gives the customer full control of the networking in the cloud and provides:
- Sub-netting 
- Routing( Routes Tables)
- Firewalls (NACLs and Security Groups)
- Gateways

But does it mean every customer gets one VPC?

No you can create multiple VPC and you can create a VPC for different environments or applications.


### VPC and Regions

A VPC is specific to a single region


## Subnets
Subnets are a group of IP addresses in your VPC. For example if you deploy a website on an EC2 it means that the application will be running on one of the IP address of a subnet.

A subnet also resides within a single availability zone
![image_68.png](image_68.png)
A Subnet can  either be public or private to allow external access to resources within them.

A private subnet means that the subnet can't talk to the internet and also
the internet cant talk to the subnet. It's good for something like a database

A Public subnet on the other side means that the subnet can talk to the internet and you can also access it from the internet.

Every VPC has a range of IP addresses assigned to it called the CIDR block.

A CIDR block defines the IP addresses that resources in the VPC can use

A CIDR block size can be anywhere from /16 to a /28

e.g. !92.168.0.0/16 : Will give  you a range from 192.168.0.0 - 192.168.255.255
Subnet within a VPC must be within the CIDR range:
![image_70.png](image_70.png)

The first 4 IP addresses of a subnet are reserved and cannot be used.

- 192.168.10.0 : Network address
- 192.168.10.1 - 192.168.10.3 : Reserved for AWS
- The Last IP address of a subnet is reserved as the broadcast address : 192.168.10.255
- The first address ready for use should be 192.168.10.4

## VPC External Connectivity
## Internet Gateway
Subnet when first created are private and nor exposed to the internet.
![image_71.png](image_71.png)

Then if private it means that the resources running inside it cannot be accessed from the internet.

To make a private subnet public an Internet gateway is attached to a VPC  to allow subnet in a VPC to communicate with the internet and vice versa.

The ability to access an internet gateway is what determines whether a subnet is public or private.

### NAT Gateway
With NAT Gateway a connection must be initiated from within the VPC, if the connection is from the internet its
going to be blocked unlike internet gateway.

This means that a private subnet can use the NAT Gateway for Communication with the internet.
![image_72.png](image_72.png)

To connect to a private subnet you use a Virtual Network Gateway or Direct connect.

## Default VPCs

There a two rypes of VPC
- Default 
- Custom

### Default VPC
Every account has a default VPC in each region.

- Default VPCs have configurations defined by AWS.
- Default VPC uses CIDR block 172.31.0.0/16 (65,536 addresses)
- In each availability zone we will have a subnet with a /20 ( 4096 addresses)
- An Internet gateway is attached to the VPC
- A route that points all traffic (0.0.0.0/0) to the **internet gateway**
- All the  subnet are going to be public 
- A Default security group is also created 
- A Default network access control list too.


### Custom VPC 

Custom VPC allow you to create.modify all configurations associated with the VPC.



