---
type: definition
tags: [ea, microservices]
source: https://world.hey.com/joaoqalves/disasters-i-ve-seen-in-a-microservices-world-a9137a51
author: João Alves
---
As you can imagine, end-to-end tests have similar problems to development environments. Before, it was relatively easy to create a new development environment using virtual machines or containers. It was also fairly simple to create a test suite using Selenium to go through business flows and assert they were working before deploying a new version. After microservices, even if we can solve all the above's problems with setting up environments, we cannot declare that a system is working anymore. At most, we can state that a system with specific versions of the services running and a given configuration is working at a particular point in time. That's a huge difference!

It was extraordinarily tough to convince people that we could not have more than a couple of these tests. And that it wasn't enough to run them in the Continuous Integration flow. They should run continuously. And they should run against production and produce alerts accordingly. I've shared countless times Cindy Sridharan's article "[Testing in production, the safe way](https://copyconstruct.medium.com/testing-in-production-the-safe-way-18ca102d0ef1)" to try to make people understand my points.

[[Microservice disaster]]