---
type: definition
tags: [ea, microservices]
source: https://world.hey.com/joaoqalves/disasters-i-ve-seen-in-a-microservices-world-a9137a51
author: João Alves
---
I've lost count of the number of times someone approached me saying:    

> Hey, João. Do you have a minute? We need to fix our development environments! People are complaining about them all the time, and this isn't working!

The problem crossed different dimensions. Mobile developers not developing a feature before it was in a development environment or backend developers who wanted to try their service didn't break any business flow. It was also problematic if someone wanted to test the whole flow in a mobile app before production. 

There are several issues with development environments across distributed systems, especially at scale:

1.  How much does it cost to spin 200 services in a cloud provider? Can you do it? Can you also spin up the infrastructure needed to run them?
2.  How much time does it cost to do so? What if, when a mobile engineer starts to develop a feature, there's a set of services in a given version, and when they finish, there are ten new versions deployed into production?
3.  What about test data? Do you have test data for all your services? Is it coherent across the fleet, so users and other entities match?
4.  If you're developing a multi-tenant, multi-region application, what about configuration and feature flags? How do you stay in sync with production? What if the defaults change meanwhile?

That is the tip of the iceberg. One can think of throwing engineering power into this problem. It might work. But I'd challenge that most organizations have the scale to do it. Doing it right is astoundingly tricky and expensive.

[[Microservice disaster]]