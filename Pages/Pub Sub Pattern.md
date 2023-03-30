---
created: 2023-02-02T15:17:23 (UTC +01:00)
tags: [ea, IT, pattern]
source: https://www.redhat.com/architect/pub-sub-pros-and-cons
author: Bob Reselman
type: artikel
---

# The pros and cons of the Pub-Sub architecture pattern | Enable Architect

> [!abstract]
> Having a grasp of common architectural patterns is essential to designing software architecture at scale. Using them saves not only time but also ensures a reliable implementation of your design. There’s no need to reinvent the wheel when there’s an architectural pattern available that applies to an architecture you’re developing. The following is a brief overview of the Pub-Sub architectural pattern.

---
Having a grasp of common architectural patterns is essential to designing software architecture at scale. Using them saves not only time but also ensures a reliable implementation of your design. There’s no need to reinvent the wheel when there’s an architectural pattern available that applies to an architecture you’re developing.

The following is a brief overview of the Pub-Sub architectural pattern.

## Understanding the Pub-Sub pattern

The Pub-Sub pattern is one in which a process sends a message into a message broker. Then, the message is forwarded to one or more parties listening for incoming messages according to a given topic. You can think of a topic as an “inbox.”

Sending a message to the broker is called _publishing_. Binding to a particular topic and then listening for incoming messages at the inbox is called _subscribing_. Hence, the term _Pub-Sub_.

![[Pasted image 20230202151828.png]]
**Figure 1: The Pub-Sub architecture pattern**

Pros

-   Pub-Sub activity is asynchronous (a.k.a, “fire and forget”). Hence, there is little risk of performance degradation due to a process getting caught in a long-running data exchange interaction.
-   Adding or removing subscribers to a topic is a matter of configuration. No complex programming is required. Thus, Pub-Sub systems provide a great deal of scalability and flexibility.

Cons

-   Testing can be a challenge. Because interactions are asynchronous, testing is not a matter of making a request and then analyzing the result. Rather a message must be sent into the system, and then the test needs to observe the behavior of the process(s) under test to see when and how it handles the message. And, if the process under test requires consuming many messages from a topic over time, the testing regimens can become more difficult to manage.
-   An unexpected surge in message emission can cause bottlenecks in the network and have unexpected results for the consuming message broker.
-   Requires a well-defined policy for message formatting and message exchange; otherwise, message consumption can become mangled and error-prone.

## Putting it all together

The Pub-Sub pattern is the bedrock of asynchronous architectural design. There are a large number of messaging applications and cloud services dedicated to the Pub-Sub pattern. Using Pub-Sub can be tricky, particularly when there are many topics in play. Learning the basic concepts is straightforward, but implementations can be challenging depending on the messaging technology used and the scope of asynchronous activity that needs to be supported. Still, when it comes to implementing asynchronous communication among services and components in a large distributed application, the Pub-Sub pattern is quite popular.

Zie ook:
-  [[Microservice development pattern]]
-  [[Saga]]
-  [[Strangler Pattern]]
-  [[CQRS]]
