# Application Integration

Application integration is something that manages or enhances the communication between application.

### App to App
![image_122.png](image_122.png)

### Internet to App
![image_123.png](image_123.png)
### App to customer
![image_124.png](image_124.png)

Application  integration is managing the flow, quality, buffering, speed, rate of communication between two application

## Amazon Simple Notification Service
Is a service used between two application in order to duplicate a message and send to multiple customers.

SNS is used when you want an application to send messages to customers via text, email, or mobile push or when 
you want to copy a single message to multiple applications.
![image_125.png](image_125.png)

## Amazon Simple  Queue Service
SQS is used when you want to send a message to another application, but there is a chance that a sudden increase in user traffic could
generate a large amount of message.

The orders will just queue until your backend can process them.
![image_126.png](image_126.png)

While SNS duplicate SQS will make sure that you won't overload your backend.

## Amazon Elastic Load Balancing

Used to direct traffic to backend servers and distribute workloads evenly across servers. Unhealthy servers are not available if failing.

Can be used with EC2, ECS, EKS and lambda among others.
![image_127.png](image_127.png)

## Amazon AutoScaling
A companion  service that is used with elastic Load Balancer (ELB). It monitors traffic and checks the number of people waiting in line and 
if I get a certain number of people then it's going to add more servers to allow that  traffic to be handled.

Many applications have autoscaling like DynamoDB and EC2.

Allows for scale up and down to numbers you specify.

Like 2 instances minimum and 4 instances maximum( shown below)

Scales as you need to within your limits.

![image_128.png](image_128.png)


## Other services
![image_129.png](image_129.png)