---
created: 2023-03-02T11:26:49 (UTC +01:00)
tags: [ea, microservices]
source: https://scoutapm.com/blog/distributed-monoliths-vs-microservices
author: Ganesh Mani
type: definitie
---

# Distributed Monoliths vs. Microservices: Which Are You Building? 

> [!abstract]
> What is a distributed monolith architecture and how does it differ from microservices? Learn more by reading our latest blog

---
Distributed Monolith is a system that resembles the microservices architecture but is tightly coupled within itself like a monolithic application. Most people misunderstand the concept of microservices. It is not just about splitting the application entities into several services and implementing CRUD operation using REST API on top of them. Besides that, communication between those services should happen only in a synchronous way.  

Building a microservices-based app comes with a lot of advantages. But while making one, there are good chances that you might end up with a distributed monolith. 

Your microservice is just a distributed monolith if any of these apply to it:

-   A change in one service causes the re-deployment of other services.
-   Your microservices rely on low latency communications.
-   Many services in your application share a resource (such as a database) which makes them tightly coupled.
-   There is a shared codebase or test environment between microservices.

## What’s Wrong with Distributed Monoliths?

One of the primary reasons to build an application using microservice architecture is to have scalability. Therefore, microservices should have loosely coupled services which enable every service to be independent. The distributed monolith architecture takes this away and causes most components to depend on one another, increasing design complexity.

Once an application is decoupled into different services, it is easy to change its tech stack, scale it up or down based on requirements, and more. It also means that a service can be independent without worrying about other services. But in the case of a distributed monolith, changes in design, implementation, or behavior of one service can cause changes in other services. As a result, It can badly affect performance and productivity. Here are some other top disadvantages of using a distributed monolith architecture over a microservice-based one.

### Requires Low Latency Communication

A significant problem with a distributed monolith is latency. If your services are tightly coupled and depend on synchronous communication between several services, it will badly affect the application’s throughput. 

Synchronous communication induces high latency. Let’s say that Service A sends a request to Service B, and it takes a while to respond. It can be a crash or slow server etc. Due to that, Service B increases the overall latency of the communication and affects application throughput. It completely defeats the purpose of implementing the microservice architecture.

[[Microservice disaster]]
