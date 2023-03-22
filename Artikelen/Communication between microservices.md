---
type: artikel
source: https://reddit.com/r/microservices/comments/10sfhrc/_/j71o9wk/?context=1
tags: [IT, EA, microservices]
---

The communication between microservices can by synchronous or asynchronou. Async communication is better because it will improve the availability

Lets sey system “A” has 99.9% of availability and system “B” has 99.5%.

If “A” communicate with “B” in a sync way the hole availability drops to almost 99.4%(99.9 * 99.5). This problem will scale as the application scales and more communications appears. Even that a ms goes down the entire system will die.

Async communication solves this problem but the application gets harder at the engeneering level but this is microservices!!! Very hard to do right.

For async communication AMQP is a good protocol you can chose RabbitMQ(simple option) or your favorit cloud message bus. Kafka is the bigger player.

Sync communication is not wrong but be carefull as u/MartzReddit has said it is a “bad smell”. If you are being forced to sync too much it is a sign that your bounded context is wrong and maybe you should merge these two microservices that are heavely coupled.

Zie ook:
[[Domain Driven Design (DDD) in gewoon Nederlands]]
[[Circuit Breaker Pattern]]
[[Microservice workflow automation]]

