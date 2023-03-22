---
created: 2023-02-14T15:14:27 (UTC +01:00)
tags: [EA, IT, microservices]
source: https://solace.com/blog/microservices-choreography-vs-orchestration/
author: Jonathan Schabowsky
type: artikel
---

# Microservices Choreography vs Orchestration Overview

> [!abstract]
> Learn how choosing between microservices choreography vs orchestration will affect how microservices will communicate with one another behind the scenes.

---
In orchestration, one service controller handles all communications between microservices, and directs each service to perform the intended function. In our symphony example, the function would be “play the music.”

### **Disadvantages of Microservices Orchestration**

One [disadvantage of orchestration](https://www.youtube.com/watch?v=fvXkN5cFMFY&t=32s) is that the controller needs to directly communicate with each service and wait for each service’s response. Now that these interactions are occurring across the network, invocations take longer and can be impacted by downstream network and service availability.

In smaller environments this may work fine, but things fall apart when you’re talking about hundreds or even thousands of microservices. You’ve basically created a distributed monolithic application that’s slower and more brittle than those of the past! Just like a conductor would lose their ability to effectively manage a massive orchestra, because each musician is awaiting individual attention, its not viable to ask a service control to manage that many microservices.

#### **Tight coupling**

When orchestrating microservices, you’ll find that they’re highly dependent upon each other — when they’re synchronous, and each service must explicitly receive and respond to requests to make the whole service work, failure at any point could stop the process in its tracks.

When we’re talking about microservices in an enterprise environment, sometimes thousands of microservices are applied to a single business function. At this scale, one-to-one interactions simply can’t keep up with business demand.

#### **Reliance on RESTful APIs**

An orchestration approach also relies on RESTful APIs — which are typically created as tightly coupled services — so using them can actually _increase_ the tight coupling in your architecture. Plus, building new functionality comes at a high cost and has a high impact on the API.

So if RESTful APIs and orchestration can’t scale, what does a solution look like for deploying and managing microservices? The answer will take us out of the orchestra pit and onto the stage…
[[Orchestration vs. Choreography]]
[[Communication between microservices]]
[Open Source Durable Execution Platform | Temporal Technologies](https://temporal.io/)
