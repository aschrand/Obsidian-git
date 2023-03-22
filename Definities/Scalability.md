---
created: 2023-01-19T15:18:57 (UTC +01:00)
tags: []
source: https://www.redhat.com/architect/nonfunctional-requirements-architecture?utm_campaign=refferal&utm_medium=refferal&utm_source=futurecx
author: Love Sharma
type: definitie
---

# Scalability
---
Scalability refers to the systems' ability to perform and operate as the number of users or requests increases. It is achievable with horizontal or vertical scaling of the machine or attaching AutoScalingGroup capabilities.

Here are three areas to consider when architecting scalability into your system:

-   **Traffic pattern**: Understand the system's traffic pattern. It's not cost-efficient to spawn as many machines as possible due to underutilization. Here are three sample patterns:
    -   _Diurnal:_ Traffic increases in the morning and decreases in the evening for a particular region.
    -   _Global/regional:_ Heavy usage of the application in a particular region.
    -   _Thundering herd:_ Many users request resources, but only a few machines are available to serve the burst of traffic. This could occur during peak times or in densely populated areas.
-   **Elasticity**: This relates to the ability to quickly spawn a few machines to handle the burst of traffic and gracefully shrink when the demand is reduced.
-   **Latency**: This is the system's ability to serve a request as quickly as possible. This also includes optimizing the algorithms and using [edge computing](http://www.redhat.com/en/topics/edge-computing?intcmp=7013a0000025wJwAAI) to replicate the system near users to reduce the round-trip time of a request.


See: [[Nonfunctional-requirements]]