#Serverless #IT 

# Serverless deployment

A deployment infrastructure that hides any concept of servers (i.e. reserved or preallocated resources)- physical or virtual hosts, or containers. The infrastructure takes your service's code and runs it. You are charged for each request based on the resources consumed.

The benefits of using serverless deployment include:
- It eliminates the need to spend time on the undifferentiated heavy lifting of managing low-level infrastructure. Instead, you can focus on your code.
- The serverless deployment infrastructure is extremely elastic. It automatically scales your services to handle the load.
- You pay for each request rather than provisioning what might be under utilized virtual machines or containers.

The drawbacks of serverless deployment include:
- Significant limitation and constraints - A serverless deployment environment typically has far more constraints that a VM-based or Container-based infrastructure. For example, AWS Lambda only supports a few languages. It is only suitable for deploying stateless applications that run in response to a request. You cannot deploy a long running stateful application such as a database or message broker.
- Limited 'input sources' - lambdas can only respond to requests from a limited set of input sources. AWS Lambda is not intended to run services that, for example, subscribe to a message broker such as RabbitMQ.
- Applications must startup quickly - serverless deployment is not a good fit your service takes a long time to start
- Risk of high latency - the time it takes for the infrastructure to provision an instance of your function and for the function to initialize might result in significant latency. Moreover, a serverless deployment infrastructure can only react to increases in load. You cannot proactively pre-provision capacity. As a result, your application might initially exhibit high latency when there are sudden, massive spikes in load.

[[Key attributes of cloud native apps]]
[[Kubernetes]]
