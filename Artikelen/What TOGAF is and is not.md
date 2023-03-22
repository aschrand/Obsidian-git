---
title: What TOGAF is and is not | LinkedIn
type: artikel
updated: 2022-10-27 12:40:17Z
created: 2021-03-02 13:22:52Z
author: Graham Berrisford
source: https://www.linkedin.com/pulse/togaf-table-graham-berrisford-1c/
tags:
  - EA
  - TOGAF
---

# What TOGAF is and is not

[10 artikelen](https://www.linkedin.com/in/grahamberrisford/detail/recent-activity/posts/)

This article lists ten things that TOGAF is not, introduces four principles that underpin TOGAF, simplifies its EA meta model, and addresses some challenges that make the concepts in it hard to understand.

## Ten things TOGAF is not

1 TOGAF is not an education in architecting. It is a management framework for programs and projects in which architects play a leading role. The core of the framework is a process for architecture-intensive "transformation" projects called the Architecture Development Method (ADM).

- The ADM embodies the "design thinking" principles of Herbert Simon in “The Sciences of the Artificial” (1969). In short, designers spend time up front deciding the fundamental/root issue(s) to be addressed; don't search for a solution until they have determined the real problem; and consider a range of potential solutions before settling on one. The ADM embodies six further "design thinking" ideas. 1 Capture the inspiration, the vision (phase A). 2 Take a human-centric view of business processes (A and B). 3 Manage stakeholders and value propositions (throughout). 4 Treat all design as re-design, as a baseline to target transformation (throughout). 5 Make ideas tangible to facilitate communication. Use visual languages, sketch diagrams and technical drawings to show abstract requirements may be met by concrete systems (A to E). 6 Double loop learning (throughout).

2 TOGAF is not prescriptive. It is a menu of processes and products you can select from, and are expected to tailor .

3 TOGAF is not only about architecture definition. It touches on topics such as stakeholder management and risk management. It addresses architects’ roles in planning change projects (phase F) governance of system development (G) and steering of subsequent change requests (H).

4 TOGAF is not mostly an IT architecture framework. TOGAF versions 1 to 8 were IT architecture frameworks, but in version 9 (2009) the focus shifted to business and applications architectures. It tells you to address business goals, roles and processes (phase B). before business applications (C) before platform technologies (D), and to iterate through those three phases/layers of architecture definition. In each phase you map the deliverable back to the overarching business mission, vision, drivers and goals.

5 TOGAF has never been TOGEAF. Version 9 was generalized for use at three levels: enterprise/strategic architecture, segment architecture and capability/solution architecture. Since the ADM is often used at the lowest level, using it does not imply making radical “enterprise transformation”. It does however imply designing and planning substantial changes to one or more business activity systems.

*See article 6 for an alternative way to map the ADM to enterprise and solution architecture*

6 TOGAF does not differentiate architecture from design. Higher-level architecture is done in phases B, C, D; lower-level is done in phase G. What higher and lower mean depends on the level you are working at. Architects using the ADM, working to different visions, at different levels of abstraction, may produce very different products.

7 TOGAF doesn’t necessarily deliver “an EA”. Unless you do what it suggests, which is to define your EA meta model (see section below) and extend your EA repository incrementally in each ADM cycle. Your CASE tool vendor can advise on that.

8 TOGAF certification is not a passport to a job. Like similar certification schemes, the examination tests your knowledge of TOGAF itself, rather than your experience. The certificate might help you to get an interview, since recruiters use it as a filter.

9 TOGAF certification does not require you to spend a lot. For guidance on self-study try the advice you can find behind a link on the Training Calendar at [http://avancier.website](http://avancier.website/).

10 TOGAF is not entirely consistent and coherent. It is a framework for contributions written by the members of the Architecture Forum hosted by the OG. The quasi-democratic crowd-sourced process for developing content leads to inconsistencies and incoherencies. If you want consistency and coherence, then read my web site and these [Linkedin articles](https://www.linkedin.com/in/grahamberrisford/detail/recent-activity/posts/).

## Four principles that underpin TOGAF

This section outlines four principles using snippets from the ArchiMate 3.1 standard (sections 3.4, 3.6, and 5.4.1). It is not an attempt to explain ArchiMate, and the examples are only illustrations, not exhaustive.

### **From Business to Technology**

ArchiMate’s core framework features three layers, defined thus:

- **“The Business Layer **depicts business services realised by business processes performed by business actors."
- **"The Application Layer **depicts application services that support the business, and the applications that realise them."
- **"The Technology Layer **depicts technology services needed to run the applications.”

Architect training should address the architecture layers above (along with data and software architecture) at two levels, enterprise-level portfolio management and solution-level design.

### **From External to Internal**

*“The distinction between an external (black-box, abstracting from the contents of the box) and internal (white-box) view is common in systems design. The external view depicts what the system has to do for its environment, while the internal view depicts how it does this.” ArchiMate*

The external/internal distinction can be drawn in TOGAF and ArchiMate thus.

- \*\*External: \*\*Business Services, Application Services, Technology Services
- \*\*Internal: \*\*Business Processes and Functions, Application Components, Technology Nodes or Components

External elements (services and interfaces) are realized by internal elements (processes and components). TOGAF defines business and applications services in its Architecture Requirement Specification deliverable as requirements for architecture definition.

A service is definable as a contract for a discrete required behavior. An interface can be thought of as a menu of services from which clients to select. (Note that "service" and "interface" are used with other meanings in IT.)

Architect training should presume a service-oriented approach to architecture definition, since you must know what a system has to do before you can define how it does it. You must know the services required before you can define processes to realize them.

*See article 3.*

### **From Behavior to Structure**

*“Structural elements are assigned to behavioral elements.” “In modeling new systems, it is often useful to start with the behaviors that the system must perform.” ArchiMate*

ArchiMate’s core framework features three aspects, defined as below

- \*\*The Active Structure Aspect: \*\*represents structural elements that display behavior. E.g. organization units, roles, actors, components and devices.
- \*\*The Behavior Aspect: \*\*represents the behavior performed by the actors. E.g. services and processes.
- \*\*The Passive Structure Aspect: \*\*represents objects on which behavior is performed. E.g. data objects and artifacts

Again, the presumption is that architects take service and process-oriented approach to architecture definition. You must know what a business has to do before you can define how it does it.

*See article 3.*

### **From Logical to Physical**

*“More abstract entities are realised by means of more tangible entities.” “\[A common\] distinction is between conceptual, logical, and physical abstraction levels. Logical components are implementation or product-independent encapsulations of data or functionality. Physical components are tangible software components, devices, etc. The distinction within the TOGAF framework between Architecture Building Blocks (ABBs) and Solution Building Blocks (SBBs) is very similar.” ArchiMate*

The logical/physical distinction can be illustrated wrt some concepts in TOGAF and ArchiMate thus.

- \*\*Logical: \*\*Business Functions or Capabilities, Logical Application Components, Logical Technology Components
- \*\*Physical: \*\*Actors, Physical Application Components, Physical Technology Components

Note the concept of a logical component may be aligned with the concept of an interface definition. If a component (business, application or technology) is encapsulated, then it can be defined, at a logical level, in the form of an interface definition.

*See article 5 for a longer discussion of the four principles above.*

## Implications of the principles for TOGAF’s EA meta model

In general activity system theory, actors interact in activities to meet aims by maintaining system state and producing outputs. The graphic below reshapes TOGAF's meta model in line with that, and with the four principles above. I don't promise it is practical as an EA repository structure. I do say it makes more coherent sense of the concepts than the meta model in the TOGAF standard. If you prefer, you can replace function by capability, and process by value stream.

![](1598198787193_e_1620259200_v_bet_32e4333eeee640c0a.png)
A functional decomposition diagram or capability map can be seen as a logical organization structure. Business functions/capabilities can be seen as a logical business components. Functions/capabilities can be mapped to processes/value streams, and to organization units.

If TOGAF and ArchiMate users want to reconcile Capability-Orientation with Service-Orientation, then they can:

1.  present business service contracts as declarative architecture requirement specifications that encapsulate value streams.
2.  present value streams as end-to-end processes – nicely represented in value stream diagrams without overly formality.
3.  present capability maps as equivalent to functional decomposition diagrams in appearance and possible uses.

*See articles 3 and 4*

## **Tricky TOGAF and ArchiMate concepts**

### **The ambiguity of "building block"**

TOGAF's chapter on building blocks defines a building block as a **reusable and portable component**, a "package of functionality", to be defined by its I/O interface. As in component-based design or service-oriented architecture. In other words, a building block is an encapsulated system, subsystem or component.

At some point in TOGAF history, one sentence was oddly inserted into the same chapter, to the effect that every **entity in the meta model** (inc, goals, processes, locations and data entities) is a building block. Despite this inconsistency, architecture and and solution building blocks are mostly discussed (in the rest of TOGAF) as encapsulated subsystems or components.

*See article 3.*

### **Different terms for what are in practice indistinguishable concepts**

Some come at EA concepts from the works of business management gurus rather than general system science. To preserve their vocabulary, they present **capabilities** and **value streams** as higher-level concepts than **functions** and **processes.**

However, the EA tradition is to model functions and processes at the highest possible level of an enterprise. The highest level business processes are end-to-end value streams. The highest level functions are as high as the highest capabilities. A functional decomposition hierarchy stands independently from the organization structure.

*See article 3.*

### **Nesting of systems and concepts**

Almost any concept in an EA meta model can be composed and decomposed. Since systems can be nested, they can be modeled using the same concepts at any and every level of decomposition (subsystem, building block, function, capability or component) .

Neither standard satisfactorily addresses the recursive composition of architectural entity types, and explains the implications of that for mappings between them. E.g.

- One high level process can span/require several lower-level functions/capabilities.
- One high level function/capability can encompass several lower-level processes.

To distinguish *external* and \*internal \*system elements is to imply the scope or boundary of the "system of interest" is recognized and agreed - early in the modelling process. Yet the perspective may change over time. When considering a local problem or requirement, architects may draw the boundary narrowly. When considering the "big picture", architects may draw the boundary wider than the organization that employs them; it might encapsulate a value stream that starts or ends outside that organization.

The multi-level nesting of external/internal boundaries means that the concepts of an external/internal boundary, the external entity or customer, and an “end-to-end” process are open to interpretation.

### **The difference between discrete services and bundles of them**

The service-contract is *the* basis for understanding service-oriented architecture frameworks like IAF and TOFAF. In EA, we model discrete-event-driven systems, the same at every level of nesting. However long or short a process is, its entry conditions and exit conditions can be defined in a service contract. A service contract declaratively defines a process - at any level of composition you care to define (from build a house, to book an appointment).

A discrete service is one thing. A bundle of services (as might be listed in an SLA document) is another thing, is an interface definition.

ArchiMate's definition of "service" says "a behavior", but its definition of "business service" omits the \[a\]. The standard refers to a service as a "unit" of behavior, but it is unclear whether this unit is a discrete event-driven behavior, or a bundle of them (as may be provided by a component or building block) or either.

In UML, a behavior is discrete and event-driven. Similarly, in the EA frameworks IAF and TOGAF , a service appears to be a discrete behavior that leads to a result of benefit/value to an entity outside the system of interest. A service can provide goods (a pizza), information (a train ticket), a state change (shiny shoes), or all of those, to an external entity.

*See article 3.*

### **Value stream concept v diagram**

A value stream is a sequence of stages, each composed of activities, triggered by an event, that terminates in a result of value to some external actor(s). There may be any number of optional, repeated and parallel activities in the stages of a value stream.

There is confusion between concepts and diagram styles. Many terms can be used for a process (e.g. value stream, scenario, procedure, interaction, use case, epic or user story). Many diagram styles can be used to represent a process. Any substantial process, at any level, might be represented in a value stream diagram.

Architect training tends to presume a value stream or scenario-oriented approach to solution architecture definition. You must understand the required behaviours (services, value streams, scenarios) before you can assign or define structures (actors, application and technology components - to be built, hired or bought) to perform those behaviours.

*See article 4*

### **Mapping the capability concept to others**

Whereas value streams \*sequence \*activities into stages, capabilities impose a simple logical composition structure on the resources need to complete value streams.

A capability is the ability or wherewithal to do or achieve something. Here, more specifically, a capability clusters abilities needed to complete activities in value streams.

A capability may represent the wherewithal to perform activities that serve:

- a **goal** (a state business wants to reach) or
- a **principle** ("compliance to privacy legislation" or "minimize data disintegrity")
- an **outcome** (a state a business has reached or might reach) or
- a **function** (what a business can do, could do or should do).

A capability can be associated 1-1 with any of the above.

Almost everything said function hierarchies can be said of capability maps. They usually look the same and are used for the same purposes. The ArchiMate standard ducks the debate about interchangeability of function hierarchies and capability maps by classifying business capabilities under "strategy" and business functions under "business architecture".

*See article 4.*

### **The ambiguity of the structure/behavior distinction**

ArchiMate primarily classifies functions as behaviors. However, functions may also be seen as logical business building blocks. The ArchiMate standard says: "behavior elements such as application and technology functions can be used to model logical components". Similarly, business functions can be used to model logical business components, and appear as swim lanes in a process flow diagram.

*See article 3.*

## Further reading

The references refer to these [related Linkedin articles](https://www.linkedin.com/in/grahamberrisford/detail/recent-activity/posts/).



### Meer van Graham Berrisford

- [<img width="258" height="0" src="../_resources/1612883116494_e_1620259200_v_bet_e844929aeae24e0b8.jpg" class="jop-noMdConv"><br>Enterprise and solution architect roles: things to know<br>Graham Berrisford op LinkedIn](https://www.linkedin.com/pulse/enterprise-solution-architect-roles-things-know-graham-berrisford/)
    
- [<img width="258" height="0" src="../_resources/1606582337713_e_1620259200_v_bet_2d70c98deec24fc6a.jpg" class="jop-noMdConv"><br>A primer in Business Architecture in EA<br>Graham Berrisford op LinkedIn](https://www.linkedin.com/pulse/brief-eaba-history-graham-berrisford/)
    
- [<img width="258" height="0" src="../_resources/1597846839487_e_1620259200_v_bet_aec1c9e1bb0545a29.jpg" class="jop-noMdConv"><br>Must we convert monoliths to microservices?<br>Graham Berrisford op LinkedIn](https://www.linkedin.com/pulse/monolithic-apps-v-microservices-graham-berrisford/)
    
- [<img width="258" height="0" src="../_resources/1604174781553_e_1620259200_v_bet_29e2adf6c5fe40d88.jpg" class="jop-noMdConv"><br>BA in EA: Slide Show<br>Graham Berrisford op LinkedIn](https://www.linkedin.com/pulse/ea-ba-applied-system-theory-graham-berrisford/)
    

[Alle 10 artikelen weergeven](https://www.linkedin.com/in/grahamberrisford/detail/recent-activity/posts/)