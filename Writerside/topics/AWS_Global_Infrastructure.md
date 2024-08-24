# Global Infrastructure 

## region 
An AWS region is a geographic location where  resources can be deployed.Each region id designed to be isolated from each other for:
- Fault tolerance 
- Stability

<tip>
But all the regions are not the same 
</tip>
## Selecting a Region

- Not all services are available in all regions.
- GovCloud regions designed for U.S. Government and customers who need to meet regulatory and compliance requirements.
- You should select a region as close to your customers as possible to minimise latency.
- Cost od services varies from region to region
- Due to compliance and legal requirement , you may need to run your infrastructure in certain regions.

## Availability Zones (AZ)

Within a region there are multiple Availability zones. An Availability zone is one or more discrete data centers with redundant power, networking, and connectivity in an AWS region.
Availability zones provide redundancy within a region.
![image_59.png](image_59.png)

But instead we can have the application in multiple availability zones so that if one is down , another can cover it up.
![image_60.png](image_60.png)

Global Content Delivery and Edge Locations
![image_61.png](image_61.png)
If we have a web server in N.America and a customer from the same country is accessing a resource then this will
be faster but if the customer is accessing from India then that's a longer distance and we might experience latency.

AWS noticed this and Solved it using Edge Locations:
![image_62.png](image_62.png)

## Edge Locations
AWS Edge Locations are strategically positioned points in the AWS network optimized for low-latency content delivery, ensuring that data reaches users swiftly. In contrast, AWS regions are larger geographic areas with multiple Availability Zones.

Now instead of the request being sent to N.America, Its going to be sent to an edge location near India hence low-latency.

## Local Zones
Local zones are extension of an AWS Region. local zones allow you to use select AWS services like compute, and storage closer to end-user.
Local Zones provide high-bandwidth , secure connection to parent AWS region. Great for low latency applications like real-time
gaming, live-streaming and virtual workstations for the local city.
![image_63.png](image_63.png)


## Edge Locations vs Local Zones

![image_64.png](image_64.png)

## Short Summary
![image_65.png](image_65.png)