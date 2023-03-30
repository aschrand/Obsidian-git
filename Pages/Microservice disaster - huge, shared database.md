---
type: definition
tags: [ea, microservices]
source: https://world.hey.com/joaoqalves/disasters-i-ve-seen-in-a-microservices-world-a9137a51
author: João Alves
---
An easy way out of the monoliths while keeping data consistency across them is to keep using a shared database. It does not increase the operational load, and it makes it easy to slice a monolith step-by-step. However, it also comes with considerable disadvantages. Aside from being an obvious single-point-of-failure, defeating some of the service-oriented architecture's principles, there's more. Do you create a user per service? Do you have fine-grained permissions so service A can only read or write from specific tables? What if someone removes an index unintentionally? How do we know how many services are using different tables? What about scaling?

Disentangling all of this becomes a whole new problem on its own. Technically, it may not be trivial, considering that databases tend to outlive software. Solving the problem using data replication — be it Kafka, AWS DMS or whatever — creates a need for your engineering teams to understand database specifics and how to deal with duplicated events, and so on.

[[Microservice disaster]]