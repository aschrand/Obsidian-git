---
type: definition
tags: [ea, microservices]
source: https://world.hey.com/joaoqalves/disasters-i-ve-seen-in-a-microservices-world-a9137a51
author: João Alves
---
**Disaster #1: too small services**

Having the ability to create new services every day came with an explosion of developer's creativity. A new feature? Bam, let's start a service! Suddenly, teams with 20 engineers were maintaining 50 services. That's more than one service per person! The problem with code, in general, is that it rots. Maintaining every service came at a cost. Imagine propagating a library upgrade across your services' fleet. Imagine that these services were started at different time points, with different architectures and some entanglement between the business logic and the frameworks used. That's _bananas_! Of course, there are ways to solve these problems. Most of them weren't available back in those days, and others cost a lot in FTEs work. 

Another smell was when someone told me that deploying a new feature in service A also needed a deployment — at the same time — in service B. Or when people started to write services to generate CSVs. Why would someone introduce network hops to produce a worldwide known file format? Who would maintain that? Some teams were suffering from _servicitis_. Even worse than that, it generated a lot of friction while developing. One could not just look into a project in their IDE, but it required to have multiple projects open simultaneously to make sense of all that mess.

[[Microservice disaster]]