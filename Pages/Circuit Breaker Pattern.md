---
created: 2023-02-02T15:27:32 (UTC +01:00)
tags: [ea, IT, pattern]
source: https://www.redhat.com/architect/14-software-architecture-patterns
author: Vicki Walker
type: definitie
---

# Circuit Breaker Pattern

> [!abstract]
> Architectural patterns increase your productivity: These reusable schemes address common software design challenges.

---
The [**circuit breaker**](https://www.redhat.com/architect/circuit-breaker-architecture-pattern) pattern minimizes the effects of a hazard by rerouting traffic to another service. While it helps make systems more fault tolerant to prevent accidents, it also requires sophisticated testing and using an infrastructure-management technology like service mesh.


#### Pros

  * Using a circuit breaker to respond to the onset of a hazardous condition in a fault tolerant manner is an excellent way to prevent accidents before they happen. 
  * Provides a good way to make systems fault-tolerant at a fine level of activity.

#### Cons

  * Testing can be harder than it appears. More is required than simply having the circuit breaker close down access to a particular service. A variety of failure responses need to be in force and these responses need to be tested.
  * Circuits are difficult to do as a one-off. They require an infrastructure management technology such as a service mesh that can manage the switching on and off.

Zie ook:
- [[Pub Sub Pattern]]
-  [[Microservice development pattern]]
-  [[Saga]]
-  [[CQRS]]
