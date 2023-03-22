---
created: 2023-02-02T15:24:06 (UTC +01:00)
tags: [ea, it, pattern]
source: https://www.redhat.com/architect/pros-and-cons-strangler-architecture-pattern
author: Bob Reselman
type: artikel
---

# The pros and cons of the Strangler architecture pattern | Enable Architect

> [!abstract]
> Having a grasp of common architectural patterns is essential to designing software architecture at scale. Using them saves not only time but also ensures a reliable implementation of your design. There’s no need to reinvent the wheel when there’s an architectural pattern available that applies to an architecture you’re developing.

---
Having a grasp of [common architectural patterns](https://www.redhat.com/architect/14-software-architecture-patterns) is essential to designing software architecture at scale. Using them saves not only time but also ensures a reliable implementation of your design. There’s no need to reinvent the wheel when there’s an architectural pattern available that applies to an architecture you’re developing.

**_\[ Download [An architect's guide to multicloud infrastructure](https://www.redhat.com/en/resources/architect-guide-to-multicloud-infrastructure-ebook?intcmp=7013a0000025wJwAAI) to explore important considerations for a variety of modern cloud architectures.\]_** 

The following is a brief overview of the Strangler architectural pattern.

## Understanding the Strangler pattern

The Strangler pattern is one in which an “old” system is put behind an intermediary facade. Then, over time external replacement services for the old system are added behind the facade.

The facade represents the functional entry points to the existing system. Calls to the old system pass through the facade. Behind the scenes, services within the old system are refactored into a new set of services. Once a new service is operational, the intermediary facade is modified to route calls that used to go to the service on the old system to the new service. Eventually, the services in the old system get "strangled" in favor of the new services.

![[Pasted image 20230202152513.png]]
**Figure 1: The Strangler architecture pattern**

Pros

-   Provides a way to reduce risk when doing a system transformation.
-   Keeps old services in play while refactoring to updated versions.
-   Adds uniquely new services while refactoring older services.

Cons

-   Requires a lot of ongoing attention to routing and network management.
-   A refactor effort can get stuck in “adapter hell.” Each instance of strangling an old service in favor of a new one will require special logic to accommodate the rerouting from the old service to the new service. When you have dozens, if not hundreds of services in play, this can be a lot of work.
-   Requires making sure that you have a rollback plan in play for each refactored instance. Things will go wrong. You need to be able to roll back to the old way of doing things quickly and safely.

**_\[ Read more: [How to architect intelligent automation using the Strangler pattern: A real-world example](https://www.redhat.com/architect/insurance-process-automation-strangler-pattern). \]_**

## Putting it all together

One of the ongoing challenges in architecture design and implementation is transformation risk. Any change to an existing system can result in unanticipated hazards. The Strangler pattern provides increment transformation to a system and reduces larger systemic risk to smaller, discrete episodes of change. Taking small risks to achieve a goal is always better than taking a large one. Small failures are easier to remedy than large ones, hence the essential benefit of the Strangler pattern.
