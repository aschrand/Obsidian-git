---
created: 2023-01-19T15:16:25 (UTC +01:00)
tags: [IT, EA]
source: https://www.redhat.com/architect/nonfunctional-requirements-architecture?utm_campaign=refferal&utm_medium=refferal&utm_source=futurecx
author: Love Sharma
type: artikel
---

# 10 nonfunctional requirements to consider in your enterprise architecture | Enable Architect

> [!abstract]
> Nonfunctional requirements define how a system is supposed to operate, rather than what it's supposed to do, but they still play a vital role in meeting end-users' needs.

---
Briefly, _functional requirements_ define what a system is supposed to do. In the case of a car, that's taking a person from A to B. _Nonfunctional requirements_ stipulate how a system is supposed to be.

Here is a cheat sheet for understanding nonfunctional requirements:

Image

![Architectural Characteristics chart](https://www.redhat.com/architect/sites/default/files/styles/embed_large/public/2022-07/ArchitecturalCharacteristics.png?itok=4Ueyyn9Z)

(Image by Love Sharma, click [here](https://imgur.com/a/HzPp8s0) for a larger view)
These top 10 architectural characteristics cover most aspects of a large-scale project. You don't need to accommodate all of them in your project; pick the most essential and knock it out. This article does not provide solutions to meeting these NFRs but instead explains areas to consider when designing a system.

[[Scalability]]
[[Availability]]
[[Extensibility]]
[[Consistency]]
[[Resiliency]]
[[Usability]]
[[Observability]]
[[Security]]
[[Durability]]
[[Agility]]


Now that you are familiar with the architectural characteristics or NFRs, you may be wondering which ones will fit your project needs. Or maybe all of them are required in your project. So how can you adapt these characteristics to your needs?

Once you understand the functional requirement, try to find any bottlenecks in the system that may add obstacles to primary functions. How do you find the bottleneck? Try answering a few of these questions:

-   Will the system perform in a 100M/1B userbase?
-   Will the system handle 10,000 concurrent requests?
-   Am I handling the data securely?
-   Can I add more features easily without impacting the existing working features?

There are many other similar questions to help you determine the characteristics that will aid your project. Some of these questions can help identify a bottleneck or lower-performing areas, which are potential starting points to improving the system's overall reliabil