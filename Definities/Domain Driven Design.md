---
created: 2023-01-19T15:55:20 (UTC +01:00)
tags: [EA]
source: https://martinfowler.com/bliki/DomainDrivenDesign.html?utm_campaign=refferal&utm_medium=refferal&utm_source=futurecx
author: Martin Fowler
type: definitie
---

# Domain Driven Design

> [!abstract]
> Domain-Driven Design is an approach to software development that centers the development on programming a domain model that has a rich understanding of the processes and rules of a domain. The name comes from a 2003 book by Eric Evans that describes the approach through a catalog of patterns. Since then a community of practitioners have further developed the ideas, spawning various other books and training courses. The approach is particularly suited to complex domains, where a lot of often-messy logic needs to be organized.

---

[evolutionary design](https://martinfowler.com/tags/evolutionary%20design.html)

[domain driven design](https://martinfowler.com/tags/domain%20driven%20design.html)

[application architecture](https://martinfowler.com/tags/application%20architecture.html)


The idea that software systems need to be based on a well-developed model of a domain has been around for at least as long as I've been in the industry. I learned much of this thinking from Jim Odell, who developed this style of thinking with data modeling, information engineering, and object-oriented analysis. Representing the underlying domain was a key part of much work in the database and object-oriented communities throughout the 1980s and 1990s.

Eric Evans's great contribution to this, through his book, was developing a vocabulary to talk about this approach, identifying key conceptual elements that went beyond the various modeling notations that dominated the discussion at the time. At the heart of this was the idea that to develop software for a complex domain, we need to build [Ubiquitous Language](https://martinfowler.com/bliki/UbiquitousLanguage.html) that embeds domain terminology into the software systems that we build. While many folks talked about developing such models, they were often only done on paper, and usually expected to be done up-front. DDD stresses doing them in software, and evolving them during the life of the software product. Eric is a strong proponent of [Extreme Programming](https://martinfowler.com/bliki/ExtremeProgramming.html) and sees Domain-Driven Design as a natural component of an extreme programming approach - a view shared by most XP practitioners I know.

The book introduced the notion of classifying objects into Entities, Value Objects, and Service Objects - what I call the [Evans Classification](https://martinfowler.com/bliki/EvansClassification.html) and identifying the concept of [Aggregates](https://martinfowler.com/bliki/DDD_Aggregate.html). I found these filled an important gap in thinking about objects which eluded both programming languages and diagrammatic notations. A particularly important part of DDD is the notion of Strategic Design - how to organize large domains into a network of [Bounded Contexts](https://martinfowler.com/bliki/BoundedContext.html). Until that point, I'd not seen anyone tackle this issue in any compelling way.

Although Eric's background is rooted in the Object-Oriented community, the core notions of Domain-Driven Design are conceptual, and thus apply well with any programming approach - a fact that's especially true of the strategic design aspects.

Zie ook: [[Domain Driven Design (DDD) in gewoon Nederlands]]