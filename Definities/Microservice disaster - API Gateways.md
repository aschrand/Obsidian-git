---
type: definition
tags: [ea, microservices]
source: https://world.hey.com/joaoqalves/disasters-i-ve-seen-in-a-microservices-world-a9137a51
author: João Alves
---
API Gateways are a typical pattern in service-oriented architectures. They're helpful to decouple the backend from the frontend consumers. They're also beneficial when it comes to implementing endpoint aggregation, rate-limiting or authentication across your system. More recently, the industry has been leaning towards _backend-for-frontend_ architectures, where these gateways are deployed for every single frontend consumer — iOS, Android, web, or desktop apps —, making their evolution decoupled from each other.

As with everything in this world, people start to have new, creative use-cases for it. Sometimes it's a small hack to make the mobile application backwards compatible. Suddenly, you have your "API gateway" being a single-point-of-failure — because people find it easier to handle authentication in a single place — **and** with some unintended business logic inside it. Instead of having a monolith getting all of the traffic, now you have a home-made Spring Boot service getting all of it! What could go wrong? Engineers quickly realize this is a mistake, but as there are many customizations, sometimes they cannot substitute this piece for stateless, scale-friendly ones. 

The culprit of the API gateways disasters comes when it consumes endpoints that are not paginated or return massive responses. Or when you make an aggregation without fallback mechanisms in place, making one single API call burn down your gateway.

[[Microservice disaster]]