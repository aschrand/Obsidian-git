---
created: 2023-01-19T15:20:50 (UTC +01:00)
tags: []
source: https://www.redhat.com/architect/nonfunctional-requirements-architecture?utm_campaign=refferal&utm_medium=refferal&utm_source=futurecx
author: Love Sharma
type: definitie
---

# Availability
---
Availability is measured as a percentage of uptime and defines the proportion of time that a system is functional and working. Availability is affected by system errors, infrastructure problems, malicious attacks, and system load. Things to consider include:

-   **Deployment stamps**: Deploy multiple independent copies of application components, including data stores.
-   **Geodes**: Deploy backend services into a set of geographical nodes, each of which can service any client request in any region.


See: [[Nonfunctional-requirements]]