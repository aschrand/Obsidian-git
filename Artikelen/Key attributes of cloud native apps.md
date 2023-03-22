---
created: 2023-01-26T16:47:19 (UTC +01:00)
tags: [IT, EA, microservices]
source: https://thenewstack.io/10-key-attributes-of-cloud-native-applications/
author: Janakiram MSV
type: artikel
---

# 10 Key Attributes of Cloud Native Applications - The New Stack

> [! Abstract]
> What is Cloud Native computing? What are the tools and platforms needed for running workloads completely in the cloud. All the answers will be found here.
> 

---
## 10 Key Attributes of Cloud Native Applications

 1. **Packaged as lightweight containers:** [Cloud native applications](https://thenewstack.io/what-are-cloud-native-patterns-and-how-should-you-use-them/) are a collection of independent and autonomous services that are packaged as lightweight containers. Unlike virtual machines, containers can scale-out and scale-in rapidly. Since the unit of scaling shifts to containers, infrastructure utilization is optimized.
 2. **Developed with best-of-breed languages and frameworks:** Each service of a cloud native application is developed using the language and framework best suited for the functionality. Cloud native applications are polyglot; services use a variety of languages, runtimes and frameworks. For example, developers may build a real-time streaming service based on WebSockets, developed in Node.js, while choosing Python and Flask for exposing the API. The fine-grained approach to developing microservices lets them choose the best language and framework for a specific job.
 3. **Designed as loosely coupled microservices:** Services that belong to the same application discover each other through the application runtime. They exist independent of other services. Elastic infrastructure and application architectures, when integrated correctly, can be scaled-out with efficiency and high performance.
 4. **Centered around APIs for interaction and collaboration:** Cloud native services use lightweight APIs that are based on protocols such as representational state transfer (REST), Google’s open source remote procedure call (gRPC) or NATS. REST is used as the lowest common denominator to expose APIs over hypertext transfer protocol (HTTP). For performance, gRPC is typically used for internal communication among services. NATS has publish-subscribe features which enable asynchronous communication within the application.
 5. **Architected with a clean separation of stateless and stateful services:** Services that are persistent and durable follow a different pattern that assures higher availability and resiliency. Stateless services exist independent of stateful services. There is a connection here to how storage plays into container usage. Persistence is a factor that has to be increasingly viewed in context with state, statelessness and — some would argue — micro-storage environments.
 6. **Isolated from server and operating system dependencies:** Cloud native applications don’t have an affinity for any particular operating system or individual machine. They operate at a higher abstraction level. The only exception is when a microservice needs certain capabilities, including solid-state drives (SSDs) and graphics processing units (GPUs), that may be exclusively offered by a subset of machines.
 7. **Deployed on self-service, elastic, cloud infrastructure:** Cloud native applications are deployed on virtual, shared and elastic infrastructure. They may align with the underlying infrastructure to dynamically grow and shrink — adjusting themselves to the varying load.
 8. **Managed through agile DevOps processes:** Each service of a cloud native application goes through an independent life cycle, which is managed through an agile DevOps process. Multiple continuous integration/continuous delivery (CI/CD) pipelines may work in tandem to deploy and manage a cloud native application.
 9. **Automated capabilities:** Cloud native applications can be highly automated. They play well with the concept of infrastructure as code. Indeed, a certain level of automation is required simply to manage these large and complex applications.
 10. **Defined, policy-driven resource allocation:** Finally, cloud native applications align with the governance model defined through a set of policies. They adhere to policies such as central processing unit (CPU) and storage quotas, and network policies that allocate resources to services. For example, in an enterprise scenario, central IT can define policies to allocate resources for each department. Developers and DevOps teams in each department have complete access and ownership to their share of resources.
