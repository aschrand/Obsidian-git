---
created: 2023-02-14T15:16:04 (UTC +01:00)
tags: [EA, microservices, IT]
source: https://solace.com/blog/microservices-choreography-vs-orchestration/
author: Jonathan Schabowsky
type: artikel
---
A good analogy for looking at microservices orchestration vs choreography is music and dance; orchestration entails actively controlling all elements and interactions like a conductor directs the musicians of an orchestra, while choreography entails establishing a pattern or routine that microservices follow as the music plays, without requiring supervision and instructions.
![[Pasted image 20230214151302.png]]

The adoption of microservices is growing rapidly, as evidenced by a [study from Dimensional Research on behalf of LightStep](https://siliconangle.com/2018/05/02/new-study-shows-rapid-growth-microservices-adoption-among-enterprises/) which found that almost all the surveyed senior development stakeholders who have deployed microservices expect it to become their default application architecture.

That said, there are many challenges associated with the implementation of microservices – many related to how microservices interact with one another to achieve a business outcome. Choosing between microservices choreography vs orchestration will make a difference in how seamlessly the services function behind the scenes and whether you succeeded in building a microservices architecture or distributed monolith.
[Open Source Durable Execution Platform | Temporal Technologies](https://temporal.io/)

#### Benefits of Microservice Orchestration

-   Easy to maintain and manage as we unify the business process at the center.
-   In synchronous processing, the flow of the application coordinates efficiently.

#### Limitations of Microservice Orchestration

-   Creating dependency due to coupled services. For example, if service A is down, service B will never be called.
-    The orchestrator has the sole responsibility. If it goes down, the processing stops and the application fails.
-   We lose visibility since we are not tracking business process.

#### Benefits of Microservice Choreography

1.  Faster processing as no dependency on central controller.
2.  Easy to add and update. The services can be removed or added anytime from the event stream.
3.  As the control is distributed, there is no _single point failure._
4.  Works well with agile delivery model, as teams work on certain services rather than on entire application.
5.  Several patterns can be used. For example, _Event sourcing_, where events are stored, and it enables event replay. _Command query responsibility segregation (_CQRS) can separate read and write activities.

#### Limitations of Microservice Choreography

1.  Complexity is the concerning issue. Each service is independent to identify the logic and react based on the specific data in the event stream.
2.  Business process is spread out, making it difficult to maintain, manage the overall process.
3.  Mindset change is prerequisite in the asynchronous approach.
