#Microservices #pattern 

---

# Microservices Development Patterns: Sync vs. Async
The general properties for each communication style are as follows. 

Synchronous 
* Better for read-heavy service operations
* Generally provides immediate data consistency
* Potential for moderate scaling 
* Tight coupling between services
* Simpler to design
* Requires special constructs such as circuit breakers to avoid cascading failures due to high load

Asynchronous
* Better for write-heavy service operations
* Generally provide eventual data consistency
* Potential for higher scaling 
* Loose coupling between services
* Comparatively more complicated to design
* Naturally resilient to traffic bursts and failures

## Synchronous
REST with HTTP most popular.
Communication resiliency through:
* Circuit Breaker
* Load Balancing
* Failover
* Retry
* Timeouts

Intern communication by using a binary protocol as gRPC.
Service mesh: Istio

## Asynchronous
Asynchronous communication is mainly used in scenarios where most of our operations are commands to be executed via microservices. That is, it will be a one-way message going to a target service where we don’t expect anything in return; at least not something immediately anyway.

Products: Nats, Kafka, RabbitMQ