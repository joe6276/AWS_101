# Compute Container 

## What is a container first
Container are a tool that allows you to package an application and all the necessary files, libraries and dependencies the applications need to run.

Containers can be deployed on a machine and since they have everything the application
needs to run there is nothing else that needs to be done. They are just small lightweight version of virtual machines.

## Container Challenges
Ultimately we want our application to be in multiple hosts, we need to restart faulty container, we need to scale up and down,we also need to replace a host if its not working.
. In that case we need something to manage the hosts. This is where container Orchestrators comes in.

### Container Orchestrators

Container orchestrators are the brains of a containerized environment.
Responsibilities include:
- Deploying containers across all available servers 
- Load balancing  request to containers
- Providing container to container connectivity
- Restarting failed containers
- Moving containers when hosts fail
Here is  example services for containers orchestrators
![image_95.png](image_95.png)

## Elastic Container Service (ECS)

Fully managed container orchestration service that helps manage, and scale containerized applications.
- ECS is managed by AWS
- Containers run on EC2 instances or Fargate
ECS is proprietary software (only available in AWS)
- Migrating to a different cloud provider will be more difficult.

## EKS
Lets first understand Kubernetes

### Kubernetes
Kubernetes is an open-source container orchestrator.
Kubernetes cluster has two types of nodes
- Control-plane nodes - managers of the cluster
  - Watch over cluster and make sure cluster is kept in a working state
- Worker nodes- responsible for actually running the containerized workload


Managing Control planes and the worker nodes is difficult:
- Running & scaling control-plane
- Properly securing the control-plane

AWS Elastic Kubernetes Service  is a managed Kubernetes service
- EKS will manage the control-plane for you
- Users are still responsible for managing worker nodes
- If you use Fargate AWS will manage worker nodes too


## Benefit of EKS
- Runs and scales control-plane across multiple Availability Zones 
- Scales control-plane instances based on load
- Can integrate with other AWS services 
  - IAM for authentication
  - Elastic load balancer 
  - ECR for container Images

### ECS VS EKS

ECS is proprietary to AWS so migrating to another cloud provider can be difficult
EKS is kubernetes which is  open-source  and can run on any platform.
- Keep in mind the more AWS service you configure your cluster to interact with the harder 
it will b to move to another provider because of service specific configuration.

ECs has a simple architecture
- Simpler API
- Easier to ramp up new team members 
Kubernetes is very complex and has a steep learning curve
- With EKS you'll have to learn kubernetes as well as EKS specific features.

Kubernetes has a larger community
- More support online
- More tooling like Helm/ Kustomize/ArgoCD

ECS pricing - No cost for control-plane , only pay for infrastructure running applications (EC2/ Fargate , EBS)
EKS pricing - more expensive, you have to pay for control-plane and worker nodes/ Fargate.





