# AWS Security Compliance 
## What is Compliance 

Organizations in specific industries must adhere to certain rules and guidelines specific
to that industry (Finance, Health, Federal Government). 

Compliance and regulatory frameworks are sets of guidelines and best practices. Organizations follow these guidelines to meet regulatory requirements, improve
processes, strengthen security, and achieve other business goals

## AWS Compliance
AWS undergoes certification reviews and audits to meet regulatory requirements too.
Audit reports are available on **AWS Artifacts**. Customers and review and accept agreements in the Artifact.

### Customer Compliance Center
![image_43.png](image_43.png)

### AWS AUdit Manager
AWS Audit Manager continuously collects data to prepare for audits and ensures that
you are achieving compliance with regulatory standards. It helps build audit-ready
reports.
### AWS Config
It tracks how the resource is configured and records the previous configuration states, so
you can see how the configs for it have changed over time

With AWS config it keeps track of all the changes made to a resource . Example if I launch an EC2 instance ,
then add a security group, then add an EBS volume . AWS config will keep track of all 
these configurations that im making to the ECS. This will be a great tool for auditing and compliance.

## Short Summary

![image_44.png](image_44.png)