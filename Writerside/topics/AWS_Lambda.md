# AWS Lambda

Before we check on Lambda let check at what we have right now:

![image_90.png](image_90.png)

When we want a server running, we must choose the right AMI, we must add the right dependencies , we must copy the code
and Even after the application is running we must watch out for updates and software patches.Not  forgetting that
in case of traffic we need to spin up or down more servers. That's a lot of work and a developer just wants to write code.
This is where AWS Lambda Comes in 

## What is Lambda
AWS Lambda is a compute service that let's you run your code without having to provision or manage servers.You just copy the code to AWS
and AWs will manage the underlying infrastructure like starting a server and running it.
Lambda is AWS' serverless offering:
- AWS manages the server maintenance,scaling, capacity provisioning and logging.

But serverless , does that mean there is no servers?

## Serverless

No, to run and application there will always need to be a  server but with Lambda serverless means from the user perspective 
you just upload your code and then AWS will manage the infrastructure.
![image_91.png](image_91.png)

What happens is AWS will have a Lambda service reserve pool  that contains several servers
and there will be an event that will be triggered for you code to run, when the event is triggered then some servers are pulled from the list of servers in the service pool
, they will run the code and when done they will be freed and taken back to the service pool.


## Lambda Use Case

- File processing - Eg resizing an image everytime an image is uploaded.
- Stream processing
- Web application
- Mobile/ Web backend

## Lambda Components

### Lambda Function
This is basically your code
![image_92.png](image_92.png)

### Trigger

Trigger determines when your lambda function should run.

![image_93.png](image_93.png)

### Event 
Event is the information of what trigger took place, eg of an event is about file upload then the event could include the name of the file .


## Benefits of Lambda
- No Server to manage
  - No need for an infra team 
  - No patching/upgrading
  - Faster development
- Auto scale to handle traffic spikes
- Pay for what you use
    - pay per invocation
    - No extra cost during low traffic
## Downsides of Lambda
- No Local state
  - Will need a separate database to store data that needs to persist
- Limited execution duration
  - Function can run at most for 15 minutes
  - Not good for long-running tasks
- Cold starts
  - Cold start occur due to the time it takes to initialize and load a function.


## Lambda Pricing
You will be charged for:
- Number of time the function ran 
- How long did it run for
- How much memory/ CPU did it require.

