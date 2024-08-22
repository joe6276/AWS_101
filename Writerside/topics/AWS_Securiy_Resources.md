# AWS Security  Resources

## Prevention Security Resources

### Web Application Firewall (WAF)
Monitors HTTP requests and prevents a variety of attacks like SQL injection and XSS
attacks.


### AWS Shield
AWS Shield detects and mitigates sophisticated distributed denial of service (DDoS) attacks.
A DDoS attack is when a perpetrator seeks to make a machine or network resource
unavailable to its intended users by temporarily or indefinitely disrupting the services of a host
connected to a network.
- Denial of service is typically accomplished by flooding the targeted machine or resource
  with fake requests to overload systems and prevent some or all legitimate requests from
  being fulfilled.


### AWS Network Firewall
It is a stateful managed firewall and intrusion detection and prevention service for VPCs. It monitors traffic going into and out of a VPC.

## Detection Security Resources
AWS Inspector
AWS inspector scans workloads running on AWS for software vulnerabilities and
undesired network exposure.
- It automatically discovers and scans EC2 instances, container images in ECR, and
Lambda function.
-  It continues to assess your environment throughout the lifecycle of your resources by
automatically rescanning resources in response to changes that could introduce new
vulnerabilities.
1. Installing new package
2. Installing a patch
3. New common vulnerabilities and Exposures (CVE) are released
   ● If vulnerabilities are identified, AWS Inspector produces a finding that you can
   investigate.
### Amazon GuardDuty

![image_53.png](image_53.png)

### Amazon Detective
Amazon Detective helps you quickly analyze and investigate security events across one
or more AWS accounts.
1. It ingests data from VPC flow logs, CloudTrail logs, and GuardDuty findings.
2. It uses machine learning and statistical analysis to create advanced
   visualizations that show resource behaviors and interactions over time.
   Amazon Detective simplifies the process of investigating security incidents by providing
   interactive dashboards and visualizations.

### AWS Config
It tracks how the resource is configured and records the previous configuration states, so
you can see how the configs for it have changed over time

AWS Security Hub
It automates security checks and brings security alerts into a central location:
- Ingests data from other services like AWS Config, GuardDuty, Firewall Manager,
Inspector, etc.
- Performs validation against AWS/Security best practices
- ![image_54.png](image_54.png)
  
### CloudTrail
CloudTrail tracks user activity with an AWS account.
- It tells us who is doing what.
- Anytime a user performs an action within AWS, an event is logged in CloudTrail, such
as:
1. Logging in
2. Modifying security policies
3. Accessing/creating/deleting a service
   ● It logs actions taken in the console, command line, and AWS SDK/APIs.

### Security Lake
   It collects security logs and events from multiple sources including on-premises, AWS services,
   and third-party services. It transforms the data into storage and query-efficient Parquet format
   ![image_55.png](image_55.png)
   
## AWS Macie
AWS Macie uses pattern matching and machine learning to automatically discover sensitive data.
Macie will generate an inventory report of S3 buckets and scan objects for sensitive data and notify you.

## Detection Summary
![image_56.png](image_56.png)


## Management Security Resources

### Firewall Manager
It helps manage security services (WAF, security groups, network firewall) across multiple AWS
accounts. It configures rules just once and has them available across all accounts.

![image_57.png](image_57.png)
### Resource Access Manager
It helps you securely share resources across accounts, organizations, and OUs. So, you can
create a resource once and have the Resource Access Manager make that resource usable by
other accounts.
![image_58.png](image_58.png)


### AWS Cognito
AWS Cognito helps implement customer identity and access management for mobile and web
applications.
● It manages all user credentials.
● It makes adding signup/login functionality easy without social authentication on any app.

### IAM Identity Center
It simplifies managing users across multiple AWS accounts. It also allows you to manage sign-in
security for your users centrally and grant them access across all AWS accounts and resources.
### Secrets Manager
The Secrets Manager helps retrieve and rotate secrets and other sensitive data like credentials
and Auth tokens.
- No need to hard code credentials in application source code
- Makes it more difficult to leak or compromise sensitive credentials
- Can configure automatic rotation schedule for your secrets
- Having short-term secrets decreases the risk of compromise

### AWS Certificate Manager (ACM)
It handles the complexity of creating, storing, and renewing public and private SSL/TLS
certificates and keys that protect AWS websites and applications.
- If users need to communicate with an ELB or API gateway, you now no longer need to
purchase a paid certificate from a third party.
-ACM can generate them for you, and end-user traffic will be encrypted.
- You can issue certificates directly from ACM or import third-party certificates.

### AWS Private Certificate Authority
It provides users with a private CA that is managed by AWS.
- Issues certificates for authenticating internal users, computers, and applications
- Certificates issued by a private CA are trusted only within your organization and not on
the internet
- Saves the hassle of having to set up, configure, and maintain your own internal
certificate authority

### Key Management Service (KMS)
KMS helps create and manage cryptographic keys used for encrypting/decrypting data.
- It allows you to provide granular control over who has access to the keys
- Key rotation can be configured
### CloudHSM
CloudHSM provides customers with a hardware security module in the cloud.
- All cryptographic keys are securely stored on the HSM, and they never exit the device
- Data is sent from the clients to the HSM for encryption/decryption
- Because all keys are securely stored on the HSM in a central location, it helps minimize
the risk of keys getting leaked or stolen
