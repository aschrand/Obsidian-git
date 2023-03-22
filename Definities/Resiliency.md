---
created: 2023-01-19T15:22:49 (UTC +01:00)
tags: []
source: https://www.redhat.com/architect/nonfunctional-requirements-architecture?utm_campaign=refferal&utm_medium=refferal&utm_source=futurecx
author: Love Sharma
type: definitie
---

# Resiliency
---
A system can gracefully handle and recover from accidental and malicious failures. Detecting failures and recovering quickly and efficiently is necessary to maintain resiliency. The primary factor to consider when architecting for resiliency is:

-   **Recoverability**: This is the preparatory processes and functionality that enable services to return to an initial functioning state after an unintended change. Unintended changes include soft or hard deletion or misconfiguration of applications.
    -   _Disaster recovery:_ Disaster recovery (DR) consists of best practices designed to prevent or minimize data loss and business disruption resulting from catastrophic events—everything from equipment failures and localized power outages to cyberattacks, civil emergencies, criminal or military attacks, and natural disasters.

Following are some DR design patterns you might implement to build resiliency into your architecture:

-   **Bulkhead:** This pattern isolates elements of an application into pools so that if one fails, the others will continue to function.
-   [**Circuit breaker:**](https://www.redhat.com/architect/circuit-breaker-architecture-pattern) This pattern handles faults that might take a variable amount of time to fix when connecting to a remote service or resource.
-   **Leader election:** This pattern coordinates the actions performed by a collection of collaborating task instances in a distributed application by electing one instance as the leader that assumes responsibility for managing the other instances.


See: [[Nonfunctional-requirements]]