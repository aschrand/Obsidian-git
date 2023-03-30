---
created: 2023-02-01T18:59:06 (UTC +01:00)
tags: [EA, microservices, IT, pattern]
source: https://www.baeldung.com/cs/saga-pattern-microservices#database-per-service-pattern
author: 
type: artikel
---

# Saga Pattern in Microservices | Baeldung on Computer Science

> [!abstract]
> Learn about the Saga architecture pattern to implement distributed transactions in a microservice-based application.

---
## 1\. Overview[](https://www.baeldung.com/cs/saga-pattern-microservices#introduction)

From its core principles and true context, **a [microservice](https://www.baeldung.com/spring-microservices-guide)\-based application is a distributed system.** The overall system consists of multiple smaller services, and together these services provide the overall application functionality.

Although this architectural style provides numerous benefits, it has several limitations as well. One of the major problems in a microservice architecture is how to handle a [transaction that spans multiple services](https://www.baeldung.com/transactions-across-microservices).

In this tutorial, we’ll explore the Saga architecture pattern that lets us manage distributed transactions in a microservice architecture.

## 2\. Database per Service Pattern[](https://www.baeldung.com/cs/saga-pattern-microservices#database-per-service-pattern)

One of the benefits of microservice architecture is that we can choose the technology stack per service.

For instance, we can decide to use a relational database for service A and a NoSQL database for service B.

This model lets the service manage domain data independently on a data store that best suites its data types and schema. Further, it also lets the service scale its data stores on demand and insulates it from the failures of other services.

However, at times a [transaction](https://www.baeldung.com/transactions-intro) can span across multiple services, and ensuring data consistency across the service database is a challenge. In the next section, we’ll look closer at the challenge of distributed transaction management with an example.

## 3\. Distributed Transaction[](https://www.baeldung.com/cs/saga-pattern-microservices#distributed-transaction)

To demonstrate the use of distributed transactions, we’ll take an example of an e-commerce application that processes online orders and is implemented with microservice architecture.

There is a microservice to create the orders, one that processes the payment, another that updates the inventory and the last one that delivers the order.

Each of these microservices performs a local transaction to implement the individual functionalities:

![distributed transaction](https://www.baeldung.com/wp-content/uploads/sites/4/2021/04/distributed-transaction.png)

This is an example of a distributed transaction as the transaction boundary crosses multiple services and databases.

To ensure a successful order processing service, all four microservices must complete the individual local transactions. If any of the microservices fail to complete its local transaction, all the completed preceding transactions should roll back to ensure data integrity.

## 4\. Challenges of Distributed Transaction[](https://www.baeldung.com/cs/saga-pattern-microservices#challenges-of-distributed-transaction)

In the previous section, we provided a real-life example of a distributed transaction. Distributed transactions in a microservice architecture pose two key challenges.

**The first challenge is maintaining ACID.** To ensure the correctness of a transaction, it must be Atomic, Consistent, Isolated and Durable (ACID). The _atomicity_ ensures that all or none of the steps of a transaction should complete. _Consistency_ takes data from one valid state to another valid state. _Isolation_ guarantees that concurrent transactions should produce the same result that sequentially transactions would have produced. Lastly, _durability_ means that committed transactions remain committed irrespective of any type of system failure. **In a distributed transaction scenario, as the transaction spans several services, ensuring ACID always remains key.**

**The second challenge is managing the transaction isolation level.** It specifies the amount of data that is visible in a transaction when the other services access the same data simultaneously. In other words, if one object in one of the microservices is persisted in the database while another request reads the data, should the service return the old or new data?

## 5\. Understanding Two-Phase Commit[](https://www.baeldung.com/cs/saga-pattern-microservices#understanding-two-phase-commit)

The Two-Phase Commit protocol (2PC) is **a widely used pattern to implement distributed transactions.** We can use this pattern in a microservice architecture to implement distributed transactions.

In a two-phase commit protocol, there is a coordinator component that is responsible for controlling the transaction and contains the logic to manage the transaction.

The other component is the participating nodes (e.g., the microservices) that run their local transactions:

![two phase commit](https://www.baeldung.com/wp-content/uploads/sites/4/2021/04/two-phase-commit.png)

As the name indicates, the two-phase commit protocol runs a distributed transaction in two phases:

1.  **Prepare Phase** – The coordinator asks the participating nodes whether they are ready to commit the transaction. The participants returned with a _yes_ or _no_.
2.  **Commit Phase** – If all the participating nodes respond affirmatively in phase 1, the coordinator asks all of them to commit. If at least one node returns negative, the coordinator asks all participants to roll back their local transactions.

## 6\. Problems With 2PC[](https://www.baeldung.com/cs/saga-pattern-microservices#problems-with-2pc)

Although 2PC is useful to implement a distributed transaction, it has the following shortcomings:

-   The **onus of the transaction is on the coordinator node**, and it can become the single point of failure.
-   All other services need to wait until the slowest service finishes its confirmation. So, the overall performance of the transaction is bound by the slowest service.
-   The two-phase commit protocol is **slow by design due to the chattiness and dependency on the coordinator.** So, it can lead to scalability and performance issues in a microservice-based architecture involving multiple services.
-   Two-phase commit protocol is **not supported in NoSQL databases.** Therefore, in a microservice architecture where one or more services use NoSQL databases, we can’t apply a two-phase commit.

## 7\. Introduction to Saga[](https://www.baeldung.com/cs/saga-pattern-microservices#introduction-to-saga)

### 7.1. What Is Saga Architecture Pattern?[](https://www.baeldung.com/cs/saga-pattern-microservices#1-what-is-saga-architecture-pattern)

The Saga architecture pattern **provides transaction management using a sequence of local transactions.**

A local transaction is the unit of work performed by a Saga participant. Every operation that is part of the Saga can be rolled back by a compensating transaction. Further, the Saga pattern guarantees that either all operations complete successfully or the corresponding compensation transactions are run to undo the work previously completed.

In the Saga pattern, **a compensating transaction must be _idempotent_ and _retryable_.** These two principles ensure that we can manage transactions without any manual intervention.

The Saga Execution Coordinator (SEC) guarantees these principles:

![saga pattern](https://www.baeldung.com/wp-content/uploads/sites/4/2021/04/saga-pattern.png)

The above diagram shows how to visualize the Saga pattern for the online order processing scenario we discussed earlier.

### 7.2. The Saga Execution Coordinator[](https://www.baeldung.com/cs/saga-pattern-microservices#2-the-saga-execution-coordinator)

The **Saga Execution Coordinator is the central component to implement a Saga flow.** It contains a Saga log that captures the sequence of events of a distributed transaction.

For any failure, the SEC component inspects the Saga log to identify the impacted components and the sequence in which the compensating transactions should run.

For any failure in the SEC component, it can read the Saga log once it’s coming back up.

It can then identify the transactions successfully rolled back, which ones are pending, and can take appropriate actions:

![saga execution](https://www.baeldung.com/wp-content/uploads/sites/4/2021/04/saga-execution.png)

There are two approaches to implement the Saga pattern: choreography and orchestration. Let’s discuss them in the next sections.

### 7.3. Implementing Saga Choreography Pattern[](https://www.baeldung.com/cs/saga-pattern-microservices#3-implementing-saga-choreography-pattern)

In the Saga Choreography pattern, **each microservice that is part of the transaction publishes an event that is processed by the next microservice.**

To use this pattern, we need to decide if the microservice will be part of the Saga. Accordingly, the microservice needs to use the appropriate framework to implement Saga. In this pattern, the Saga Execution Coordinator is either embedded within the microservice or can be a standalone component.

In the Saga, choreography flow is successful if all the microservices complete their local transaction, and none of the microservices reported any failure.

The following diagram demonstrates the successful Saga flow for the online order processing application:

![saga coreography](https://www.baeldung.com/wp-content/uploads/sites/4/2021/04/saga-coreography.png)

In the event of a failure, **the microservice reports the failure to SEC, and it is the SEC’s responsibility to invoke the relevant compensation transactions**:

![saga coreography 2](https://www.baeldung.com/wp-content/uploads/sites/4/2021/04/saga-coreography-2.png)

In this example, the Payment microservice reports a failure, and the SEC invokes the compensating transaction to unblock the seat. If the call to the compensating transaction fails, it is the SEC’s responsibility to retry it until it is successfully completed. Recall that in Saga, a compensating transaction must be _idempotent_ and _retryable_.

The Choreography pattern **works for greenfield microservice application development.** Also, this pattern is suitable when there are fewer participants in the transaction.

Here are a few frameworks available to implement the choreography pattern:

-   [Axon Saga](https://docs.axoniq.io/reference-guide/v/3.1/part-ii-domain-logic/sagas) – a lightweight framework and widely used with Spring Boot-based microservices
-   [Eclipse MicroProfile LRA](https://github.com/eclipse/microprofile-lra) – implementation of distributed transactions in Saga for HTTP transport based on REST principles
-   [Eventuate Tram Saga](https://eventuate.io/docs/manual/eventuate-tram/latest/getting-started-eventuate-tram-sagas.html) – Saga orchestration framework for Spring Boot and Micronaut-based microservices
-   [Seata](http://seata.io/en-us/docs/dev/mode/saga-mode.html) – open-source distributed transaction framework with high-performance and easy-to-use distributed transaction services

### 7.4. Implementing Saga Orchestration Pattern[](https://www.baeldung.com/cs/saga-pattern-microservices#4-implementing-saga-orchestration-pattern)

In the Orchestration pattern, **a single orchestrator is responsible for managing the overall transaction status.**

If any of the microservices encounter a failure, the orchestrator is responsible for invoking the necessary compensating transactions:

![saga orchestration](https://www.baeldung.com/wp-content/uploads/sites/4/2021/04/saga-orchestration.png)

The Saga orchestration pattern is **useful for brownfield microservice application development architecture.** In other words, this pattern works when we already have a set of microservices and would like to implement the Saga pattern in the application. We need to define the appropriate compensating transactions to proceed with this pattern.

Here are a few frameworks available to implement the orchestrator pattern:

-   [Camunda](https://camunda.com/) is a Java-based framework that supports Business Process Model and Notation (BPMN) standard for workflow and process automation.
-   [Apache Camel](https://camel.apache.org/components/latest/eips/saga-eip.html) provides the implementation for Saga Enterprise Integration Pattern (EIP).

## 8\. Conclusion[](https://www.baeldung.com/cs/saga-pattern-microservices#conclusion)

In this article, we discussed the Saga architecture pattern to implement distributed transactions in a microservice-based application.

We first introduced the challenges of these implementations.

We then explored the two-phase commit protocol, a popular alternative of Saga, and examined its limitation to implement distributed transactions in microservice-based applications.

Lastly, we discussed the Saga architecture pattern, how it works and the two main approaches to implementing the Saga pattern in microservice-based applications.

If you have a few years of experience in Computer Science or research, and you’re interested in sharing that experience with the community, have a look at our [**Contribution Guidelines**](https://www.baeldung.com/cs/contribution-guidelines).

Zie ook:
- [[CQRS]]
-  [[Circuit Breaker Pattern]]
-  [[Strangler Pattern]]
-  [[Microservice development pattern]]
- 
