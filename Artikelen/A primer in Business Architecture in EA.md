---
title: A primer in Business Architecture in EA | LinkedIn
updated: 2021-03-02 14:38:00Z
created: 2021-03-02 14:36:41Z
type: artikel
author: Graham Berrisford
source: https://www.linkedin.com/pulse/brief-eaba-history-graham-berrisford/
tags:
  - EA
---
![](assets/1606582337713_e_1620259200_v_bet_8d0fc557a7f647548.jpg)

http://avancier.website

# A primer in Business Architecture in EA

- Gepubliceerd op 20 juli 2020

[10 artikelen](https://www.linkedin.com/in/grahamberrisford/detail/recent-activity/posts/)

## Preface (extended)

This preface has grown to be more than a quarter of the article, because to forestall misunderstandings of what follows, it seem necessary to discuss first:

- External and internal views of a business
- Activity system definition
- Service-orientation
- Purposes of this article
- The historical context for EA
- BA as business system planning

### External and internal views of a business

As Groucho Marx might have said: "An enterprise that is simple enough to understand without a model of it is one that doesn't need an enterprise architect." Like all system design methods, a business modelling method should start by looking at the business from the outside, then look at the internal structures and behaviors.

- The **external** view might include goals/objectives, products, services, inputs, outputs, customers, suppliers and other external actors.
- The **internal** view might include processes or value streams, functions or capabilities, roles, data flows, data stores, locations and organization units.

In ArchiMate's generic meta model for EA, external behaviors (services) encapsulate internal behaviors (processes or activities). And external structures (interfaces) encapsulate internal structures (components or actors) and passive structures (notably, data objects created and used).

All of these things must be managed or governed in some sense, and are relevant to BA in EA. We'll come back to them. First, let us look at some of the system theory that underpins IAF, TOGAF and ArchiMate. EA is underpinned by two generic approaches to modelling a business that have *nothing to do technology;* one is activity system definition, the other is service orientation. Understanding them helps you make sense of what you read out there.

### Activity system definition

It is said that "enterprise architecture regards a business as a system, or a system of systems". More accurately, a business is a social entity in which countless activity systems may be identified - some nested, some overlapping and some conflicting - some coordinated well, some not. In operation, a business activity system is a set of actors and resources that is coherently organized and interconnected so as to perform required activities. It is orderly; it is dynamic; and characterized by the regular activities performed by actors.

Business Architecture inherits from 1950s Operational Research which modelled regular business activities that create create and use business data according to the principles of general system theory. E.g. the supply chain operations reference (SCOR) model (which helps businesses evaluate and perfect supply chain management) has two notations for inter-node flows, one for material + information flows, one for information-only flows. In those days the data was not digitized. You'll not find anything below that implies or requires data to be digitized. However, since the 1960s, most business have been striving digitize their data, so in practice, today, most BA is done in an IT-supported context.

In general system theory:

- A system has an internal \*\*state. \*\*The current state of things (people, processes, materials and machines of interest) can be remembered in the values of state variables and communicated in messages.
- A system is bounded, and can be closed or open. An **open** system interacts with its environment by consuming **inputs** and producing \*\*outputs. \*\*The outputs change the state of things in the environment of the system.
- A system's structural elements or actors play roles in activities. \*\*Actors \*\*are active structures (people, other organisms, organs, computers, software components, other machines) that occupy some space. \*\*Activities \*\*are regular behaviors performed over time by actors, which advance the internal state of the system.

Some call a business a "complex adaptive system". In reality, an enterprise is better seen as one purposeful socio-technical entity with a *mess of systems*. You can find countless activity systems in a business - large and small, nested and overlapping, more and less connected by flows, synchronized and out of step, cooperative and competitive.

EA is a never-ending battle to improve, synchronize and extend an enterprise's activity systems to make it more efficient and effective as whole. At any one time, architects focus on what is called "the system of interest", or a relationship between systems. To scope a system of interest, architects may draw a boundary around a physical entity, such as a farm, a factory, a shipyard, or some part thereof. Perhaps more often, they draw a legal or logical boundary around actors distributed in space and connected by information flows.

Traditionally (for example, in Checkland's "soft systems methodology") a system is seen as a set of regular activities that transform inputs into outputs. The diagram below encapsulates the processes of an activity system and connects it to actors in its environment. The context, and usually the requirements, for the system of interest are found outside the system.

![](1604067179597_e_1620259200_v_bet_7e872031aa0a45e89.jpg)

The processes of the system are bounded within a wider environment. What this SIPOC diagram doesn't show is that the outputs of a business system (say invoices) can influence its future inputs (say, payments). In other words, there are feedback loops between a business system and actors in its environment.

The boundary of a system depends on the perspective of the observer(s). What one sees as a system (say, a boiler transforming water into steam) may be seen by others as a subsystem inside a wider system (a steam engine).

Having encapsulated an activity system as shown above, you may go on to encapsulate each subsystem or component inside it. You can decompose the system into subsystems that interact with each other. Then decompose each subsystem, and so on, until you reach what you regard as atomic actors and activities.

System decomposition is a simple idea; it is important and useful today. Remember that systems and system description concepts can be composed and decomposed. However, in the likes of IAF, TOGAF, BIZBOK, ArchiMate and UML we have a wider variety of techniques for modelling a complex, multi-faceted business.

### Service-orientation

The term "service" reflects the economic shift from the physical to the abstract. From the industrial age to the information age. From material processing to information processing.

A service is a time-bound activity that provides a result of value to a consumer. The result can be material (food, clothing), information (money, music) or other (social care, shiny shoes). In scientific terms, the result is an output of or state change in the system of interest. In business terms, a service is Specific, Measurable, Actionable, Reality and Time-bound.

Services can be coarse-grained or fine-grained. Macro service examples include, build a house, complete a project, place all this year's applicants in universities.

In TOGAF 9.1: "A service is a logical representation of a repeatable business activity that has a specified outcome". In ArchiMate 3.1: "A business service represents explicitly defined behavior that a business \[role, actor, or collaboration\] exposes to its environment."

The definition in this article is compatible with those above. **Service (1)** the external or declarative view of an activity or process that produces a result (output or state change) of use to some external actor(s).

Beware the term service is used with many other meanings, including: Service (2) a Service Level Agreement: as in services management, a contract covering many discrete services of type 1. Service (3) an interface definition: as in UML, again covering many discrete services of type 1. Service (4) ensuring the availability of one or more applications: as in IT operations "keeping the lights on". Service (5) an application or application component: as in software architecture.

### Purposes of this article

The aim is not define what all EAs must or should do. It is to help EAs understand the BA in EA concepts, principles and tool kit out there. So EAs can not only build some models/views but make them consistent and coherent as a whole.

Sadly, sources use terms in a way that are not internally consistent, let alone consistent with each other. Consultants post articles using words like "service", "value" and "capability" in various ways. Even ArchiMate users interpret its terms in different ways. This article draws concepts from IAF, TOGAF, BIZBOK, ArchiMate and UML into a coherent and consistent whole. It updates decades-old business architecture concepts and techniques by clarifying:

- the service-oriented approach to business architecture in IAF and TOGAF.
- the nature of the “Service Contracts” in TOGAF's “Architecture Requirements Specification”
- how qualities of service, including performance measures, are captured in service contacts
- that the same business activities are specifiable from two viewpoints – processes and functions - independent of an organization's management structure
- that the term capability is usually identified with a goal, outcome or function of a business or a system.

In picking through the word salad, this article turned into a primer in the science of business activity modelling. It addresses the terminology torture, with a particular focus on "capability" and "value stream". It presents a holistic view of terms and concepts you will find out there. The idea being to help you choose and use them more consistently and with more confidence. This [slide show](https://www.linkedin.com/pulse/ea-ba-applied-system-theory-graham-berrisford) illustrates much of what this article goes on to say.

### The historical context for EA

Business directors are responsible for business planning. They respond to business drivers by declaring strategic directions and top-level goals/objectives. Business planning may involve predicting demand and directing changes to any of the following.

- Constitution: mergers, acquisitions and divestments, opening/closing outlets.
- Market: industry domain/sector/segment, customers and suppliers.
- Products and services: sales and service channels, prices.
- Relationships: partners, in-sourcing and out-sourcing of operations.
- Resources: people, wages, machines, locations/buildings and other physical asset types.
- Management structure: sacking or appointing CxOs and restructuring the organisation.

Enterprise architects may both stimulate and contribute to business planning (above). But their primary responsibility is business system planning (below).

### **BA as business system planning**

There is a myth that enterprise architecture (EA) started as IT Architecture. In fact, EA grew out of concerns that the continual pressure for local IT solutions to local problems was disconnected from business planning (above) and/or sub-optimal to the enterprise as a whole.

Enterprise-wide efforts to model the data created and used by business processes started years before Zachman proposed an information systems architecture framework in 1982. And ever since, EA has involved taking a holistic, cross-organizational view of activities in business roles and processes that create and use data that is or could be digitized. See for example, the popular "EA as Strategy" published in 2006.

This article says little about the **business data** that must be captured to perform roles in processes both inside and outside the business. Let us simply assume enterprise data architects maintain a catalog of "kernel" data entities created and used by business activities.

This article focuses more on **business activity** modelling. IT people did not invent it. In the 1970s, "operational researchers" modeled workflows in business systems. Their techniques were adapted and absorbed into SADT, HIPO and related methods (promoted by Yourdon, Constantine, DeMarco, Gane and Sarson) and influenced subsequent EA modelling.

## **Core BA in EA concepts**

Science has been defined as "encompassing the systematic study of the structure and behavior of the... world". Here the study is of the structures and behaviors of business systems. The definitions below are compatible with the definitions found in IAF, ArchiMate and TOGAF. Here, the concepts are defined in relation to activities.

EA starts from the aims of system sponsors and other stakeholders, and identifies the desired outcomes that currently or should emerge from business activity.

- \*\*Goal/objective: \*\*target aim for activities, a desired effect of outputs being used by external actors.
- **Outcome:** an actual effect of outputs being used by external actors.

EA identifies the products and services that currently or should emerge from business activity - to meet the aims of sponsors and other stakeholders.

- **Product:** an information or material structure output from a system
- **Service:** the external view of an activity or process that produces outputs or state changes (results) of value to some external actor(s).

EA sees a business as a holistic network of activities, which are sequenced in deterministic, probablistic and possibilistic processes (or value streams).

- **Process** (cf. value stream): activities sequenced to complete a service.

You may define a system in two ways: internally in terms of activities performed and state variables maintained, and externally (from the outside) in terms of input-to-output transformations made. The inputs and outputs connect a business system to actors in its environment, in feedback loops

- **Input:** an information or material product consumed by a system, supplied by some external actor(s)
- **Output**: an information or material product provided by a system to some external actor(s)
- **External actor**: a player of customer, supplier, user or observer roles.

EA is largely* not *about the design of physical structures (buildings, hardware, vehicles and human bodies) but it does assign activities to logical structures - capabilities and roles.

- **Function** (cf. Capability): activities grouped for understanding and assignment.
- \*\*Role: \*\*activities grouped for assignment to one or more actors.

EA is about business roles and processes in which active structures - human and computer - create and use passive data structures to store and convey information. Businesses operations depend on business information systems that monitor and direct actors and activities (people and processes, machines and materials) in the business.

- **Data Flow **or** Data Store: **information encoded in a message or memory.

EA requires some social entity thinking. Logical capabilities and roles must be mapped to physical organization units and actors.

- **Organization unit:** groups activities and/or actors for management.
- \*\*Actor: \*\*an individual that plays roles in the systems of interest.

One more concept, which has more or less importance, depending the nature of the business.

- **Location**

To make sense of a whole business, EA often catalogs entity types of a kind mentioned above, and imposes a hierarchy on that catalog. Some oft-drawn hierarchies are discussed later.

## **A simple service-oriented method**

Given that a business system of interest features actors performing regular activities to meet aims, systems analysis and design typically proceeds by defining elements as follows. This [slide show](https://www.linkedin.com/pulse/ea-ba-applied-system-theory-graham-berrisford) illustrates much of what this section discusses.

Remember I'm not urging you to use every concept and draw every model/view discussed below.

The sequence is flexible. The choice between robot or human actors might lead you to modify the roles or the processes. But in general, you can't or don't want to acquire actors with no regard to their roles, define roles with no regard to activities and processes they are responsible for, or define processes and services with no regard to their goals.

### **Step 1. Goals, and other precursors to architecture definition**

Architects start by talking to sponsors and other stakeholders about their aims and concerns. They talk to actors who want changes to how the business works, actors who play roles in regular business activities, and anybody else affected by proposed changes. Alongside aims, they must consider risks and constraints (time, budget, resources, legislation etc.).

Architects start by looking at a system from the outside. They analyze the system's environment, identify what a system should achieve (its goals) and perhaps what it currently achieves in operation (its outcomes).

ArchiMate speaks of *goals* and *outcomes*. TOGAF speaks of *goals, objectives* and *architecture requirements*.

- Some goals are more functional. E.g. A retailer wants to fill an identified gap in the market. A tank must be designed to traverse rough terrains.
- Some goals are more non-functional. E.g. Double sales volume this year. Make a bigger profit. Resolve 90% of complaints to the satisfaction of customers.
- Some goals combine functionality and non-functional qualities. E.g. an army wants to put a thousand boots on the ground anywhere within 24 hours.

### **Step 2. Map services/products to goals**

The meaning of service here is compatible with IAF, TOGAF and ArchiMate.

- In TOGAF 9.1: "A \*\*service \*\*is a logical representation of a repeatable business activity that has a specified outcome, e.g., check customer credit, provide weather data, consolidate drilling reports, etc." TOGAF 9.1
- In ArchiMate 3.1: "A **business service** represents explicitly defined behavior that a business \[role, actor, or collaboration\] exposes to its environment."

Architects can define a system from the outside - define how it meets the aims of external actors and system sponsors by providing discrete services or products. This principle underpins service-oriented architecture frameworks and modelling languages.

Services are things a system or subsystem does for external actors. They are discrete event-driven behaviors that terminate in results or products of value to customers, clients or users. They can be coarse-grained (e.g. build a house) or fine-grained (e.g. book an appointment). A service contract contains:

- Name (e.g. build a house, or book an appointment).
- Entry conditions (inputs and other preconditions)
- Exit conditions (outputs and other post conditions, inc, perhaps "value delivered")
- Qualities of service (speed, volume and other measures, inc. perhaps price).

Note that the customer (client or user) who gets value from a service might or might not initiate the service. A service can be triggered by a request from a customer, or a third party, or some other external event, or a time event, or an internal state change of any kind.

Note that the service contract here is not an SLA document. An SLA is legal or quasi legal contract. Like an interface definition, an SLA may cover many discrete services, which may be listed in "schedule A" or not itemized at all. An SLA may average or aggregate some service qualities (e.g. all services to be available 24 * 7).

Note that services can be decomposed. In ArchiMate and TOGAF, the external behavior of a system is defined by the services it provides to actors its environment. Where a system is divided into subsystems (aka components or building blocks), each is encapsulated by an external/internal interface. So, to complete a coarse-grained service at the highest level of system definition may require many subsystems to provide finer-grained services.

*Defining a system's performance in the qualities of services*

Service-oriented architecture approaches (e.g. IAF, TOGAF and ArchiMate) hide the internal structures and behaviors of systems and subsystems behind interfaces.

The system's performance characteristics are primarily specified as "qualities of service" in service contracts. E.g. speed, volume, availability, security, scalability, usability, integrity, price and cost.

The system specification may be simplified by rolling up some service qualities to the system level. E.g. all the many services offered by one system are available for the same hours each day.

The qualities can be measured at run-time against what is declared in service contracts.

### Step 3. Map processes (or value streams) to services/products

"A business process represents a *sequence* of business behaviors that achieves a specific result.... ArchiMate 3.1

A service contract encapsulates a process by which a system (if successful) proceeds from the service’s entry conditions to its exit conditions.

Services and processes are often named as imperative phrases. E.g. Advertise a product. Accept a payment. Receive and stock a product. Deliver a product to a customer. Bid for a specialist contract.

A process (at least roughly) sequences what can or should be done – the activities that lead to a result or product of value to one or more actors. It may be divided into parallel processes and decomposed into shorter processes.

Alongside defining a process, architects should define roles, data and other structural resources needed to perform the activities.

*Mapping activities to roles*

Activities can be related roles or organization units. One (somewhat clunky) way to do this is to place the activities in a process flow diagram in different "swim lanes" for different roles or organization units. Functions can also be shown in swim lanes. (See step 4.)

*Mapping activities to data*

A tradition in EA is to map the activities in a process (and/or 3rd level functions) to the data entities they create and use. The data entities may be defined in some kind of enterprise data model or catalog. This begs questions (not addressed here) about whether named data entities (customer, supplier, employee, product, policy, asset) are the same or different in different business contexts.

### On "value"

The term is used with different meanings in different contexts. Here, the **value** is delivered at the end of a regular process, to some actor, by a service or product. That value might be expressed qualitatively, or as the maximum price the customer is willing to pay for the service.

(Like other qualities, one may strive to quantify value, but the quantification may be questionable. Given the formula: net return = gross benefit - cost, some say value = net return. However, value = benefit to a customer who pays the maximum price they are willing to pay for a service, or to other stakeholders who pay nothing for the service.)

### Step 4. Map functions (or capabilities) to processes

First, note that some people skip function definition, and directly map organization units and/or roles to processes.

Processes and functions are orthogonal views of the same activities.

- A process sequences what can or should be done by way of activities.
- A function names what can or should be done (a group of cohesive activities).

In the ArchiMate standard: "A business function represents a collection of business behavior based on a chosen set of criteria."

Functions are often named as gerunds. E.g. Advertising goods. Accepting payments. Handling goods-in. Logistics. Bidding for contracts.

*Mapping functions to goals, services etc.*

You may relate a function 1-to-1 with another BA concept, such as a goal, a service/product, or a data store; but in general the inter-concept relationships are many-to-many. E.g. one coarse-grained function may be encapsulated by many discrete services.

*Mapping functions to processes*

Since any core BA concept can be composed or decomposed, the relationships between them depend on the granularity at which they are defined. For example:

- One end-to-end process can span several fine-grained functions, and be supported or enabled by several roles.
- One coarse-grained function may encapsulate several fine-grained processes.

*Mapping functions to functions*

One function may depend on other functions, with which it exchanges one or more messages or data flows. Document inter-function dependencies or data flows. In ArchiMate, you can represent inter-function dependencies at an abstract level by a serves arrow between boxes, or, at a more detailed level, by data flow arrows.

(Discrepancies between languages used in different functions, or "bounded contexts" may be resolved by standardization, or by transformers or adapters applied to the data structures in data flows between senders and receivers.)

For mapping business functions to microservices read article 9.

### On "capability"

Generally speaking, a capability is the ability or wherewithal to do or achieve something. In many practical examples, a capability represents the ability to perform a core business function. For example, to perform the invoicing and payroll functions, actors need the corresponding invoicing and payroll capabilities. In other examples, a capability is in 1-1 correspondence with another business architecture concept.

A **capability** is an ability possessed by an actor (person, organization or system) to

- *do* something: to perform or realize some **process** or **function,** or
- *achieve* something: to meet some **goal** or produce some **outcome.**

Consider this example: “The capability to fight and win two major wars at the same time.” What does the actor (the US DoD) need to meet that goal or produce that outcome? In the abstract, the capability may be defined in terms of the goal, then whatever processes, roles and resource types are needed to meet the goal – an abstract system. What realizes the capability, produces the outcome, is a concrete system in which actors and resource instances are deployed.

A 30 year old EA tradition for functional decomposition is to limit it to three levels or one page. For 15 years people have been manufacturing reasons to justify the using the term "capability" instead of or as well as "function". Some say capabilities are "core" rather than support. Some say functions are more numerous or fine-grained than capabilities. Some say functions are baseline architecture and capabilities are target architecture.

The plain fact is, there is no use for capability hierarchy that a function hierarchy cannot be used for. All the rest is babble that obscures the underlying activity system theory. Why? Because if your business must perform an activity, then you need the capability to do it. If your business problems lie in high staff turnover and recruitment, then your business strategy must address your HR function/capability. If you insist your business strategy is limited to improving or changing core business services/products, then first, that doesn't necessarily mean you have to change your function/capability hierarchy. And second, if your strategy is indeed limited in that way, then simply omit support functions/capabilities from your hierarchical "map" of them.

The flexibility of the capability *term* is both useful and problematic. It is useful in conversation, but including both function and capability in a general EA meta model usually makes a mess of it. Read the appendix for further discussion of capabilities.

### **Step 5. Map organization units to** functions (or capabilities)

A function hierarchy is drawn to show what a business does (not how it does it), and independently of the organization or reporting structure. To realize a function one must add resources to processes, to make a complete system. A function is typically realized by an organization of:

- human and computer **actors** (people and technologies) that play roles in
- **activities** (in processes or value streams) that create and use **data** to meet
- **aims** (aka goals or objectives).

*Mapping an activity structure to an organisation structure*

ArchiMate says a business function is “closely aligned to an organization, but not necessarily explicitly governed by the organization." Beware that many confuse "function" with "organization unit". Sometimes, managers choose to align the two hierarchies by defining what is called a "functional organization" structure. But that alignment may be only short term. Other times, a function can be mapped to the several organization units (in or outsourced) that are formed and managed to realize it.

A management/reporting hierarchy clusters human actors into organization units according to some criteria - such as location, goal, service type, skill, resource, customer type etc. By using different criteria, and applying different criteria at different levels, countless different hierarchies can be imposed on the network of inter-communicating actors in a large business. Directors manipulate the reporting hierarchy according to which criteria they think most effective, and other factors such as which managers they trust.

Functions may be mapped to organization units in a matrix. You can map any required function to one or more organization units with the resources and authority to realize it. the matrix can include supplier organizations. A function or sub function can be implemented within one organization, outsourced to one or more external organizations, acquired from the market, or any combination of those.

## **More about hierarchical composition/decomposition**

A purposeful business can be seen as a network of actors interacting in a network of activities to meet a network of inter-related aims. To make sense of a business, and manage it, people impose hierarchies (below) on those networks. Sometimes one hierarchy corresponds closely to another; sometimes they differ.

### **Aim or goal decomposition**

This decomposes grand aims or goals into finer-grained objectives. It may be decomposed in line with the organization structure (below) as in a “balanced score card”.

### **Actor or organization hierarchy**

This organization or reporting structure is usually defined by business managers. It decomposes large actor assemblies into finer-grained ones. It is a dominance and/or competence hierarchy and/or /reporting hierarchy, in which some actors direct other actors to act and/or report the progress of activities.

An organization’s management structure is often volatile/fluid. It may be restructured (say by region, customer type or product type). Usually, the nature of the business (services, processes and data) is more stable.

### **Activity or process decomposition**

This decomposes a process into shorter, finer-grained processes or activities.

A process is a sequence of activities, triggered by an event, that terminates in a result or product of value to some actor(s). There may be any number of optional, repeated and parallel activities in the end-to-end process.

- (There is no universally agreed distinction between process and procedure. Scientists define a process as a procedure that terminates in the delivery of a result. Some define a procedure as a process with only one thread, no parallel paths. )

Processes can be hierarchically composed and decomposed. From the bottom up, a sequential process may be compressed into one activity in a longer process. From the top down, one activity may be elaborated as a sequence of shorter activities.

Traditionally, process decomposition stops at One Person One Place One Time (OPOPOT) activities. That is the level at which you may identify application use cases (called application services in TOGAF, or epics in agile software development).

- (Some gurus name the same concept differently at different levels of granularity. E.g. in process decomposition, one might decompose value streams into procedures into activities. And some suggest different documentation styles at different levels. In practice, the level of process granularity is variable, because the breadth of the system of interest is variable.)

### **Ability or function decomposition**

Decomposition divide an ability or a function into narrower, finer-grained ones. Whereas a process orchestrates activities into a more or less formally defined sequence, a function does not. A function clusters activities using one or more cohesion criteria (e.g. goals, data or resources needed).

- (As discussed later, a capability is the ability or wherewithal to do or achieve something. So, a capability is always defined in 1-1 association with something that is doable or achievable. And very often, that thing is a function.)

A function hierarchy gives you a logical overview of a business that is independent of an organization’s physical management structure.

So, business architects often start by building a logical organization structure, called a functional decomposition diagram (or a capability map) which decomposes broad-ranging activities or abilities into finer-grained ones. Sometimes it resembles the management structure, but it is independent of it and usually more stable.

Note that when naming a function (or a capability) the traditional advice is to name it as a gerund (xxx ing), and after its purpose, and not to tag "management" onto the end of the name.

### Uses?

This logical picture of what a business is able to do helps architects to

- Show and describe the scope of a business, or of a specific initiative
- Highlight where problems or opportunities exist and where changes are to be made
- Categorize other EA elements to facilitate impact analysis when changes are agreed.. E.g. to structure an enterprise's application portfolio or catalog.

Nobody can take in the hierarchy all at once. EAs often post it on a wall. As they study different parts of the business, they grow increasingly comfortable they understand the business and how its parts integrate (or don't). They use the chart now and then to help them put some problem or requirement into context, and explain it to others. They also use it as "shock and awe" diagram when newcomers ask what the business does or is able to do.

(Solution architects, working on specific projects, may not find it useful.)

### Technique?

From the top down, you separate activities that are loosely coupled. From the bottom up, you **cluster activities** that are cohesive in some way.

The cohesion criterion for a function could be an aim/goal. It might be a directive/principle such as "compliance to privacy legislation" or "minimize data disintegrity". It might instead be a cohesive set of data, knowledge, skills and resources.

By clustering on different cohesion criteria, any number of different function trees (a "function forest") can be drawn for one business. Most people draw only one.

Following the **strict hierarchy principle**, no activity is duplicated under different branches of a function hierarchy. To achieve that, you must stop decomposition when you reach a common function and document it separately, or else in a "common functions" leg of the hierarchy.

Following the **consistency principle**: functions and processes come together at the bottom level where "activities" are defined.

You must stop decomposing function/capabilities at some level. Most hierarchies stop at the 3rd level of decomposition, but see the next section.

*How many atomic nodes in a function or capability hierarchy?*

A function hierarchy is typically decomposed to a 3rd level of decomposition. A baseline function hierarchy defines the scope of what a business can do in a regular manner. A target hierarchy defines the scope of what it could and should do.

Supposing the decomposition ratio in a hierarchy is 1-to-7, then two levels of decomposition is about 50 atomic nodes, three levels is about 350 atomic nodes and four levels could be 2,500 atomic nodes. You stop at any level you choose; few decompose to a fourth level, but it depends on what you use the hierarchy to do.

- Suppose you are using the hierarchy to analyse which activities create and use 1,000 data entities listed in your enterprise/business data catalog, then you might want a function/capability hierarchy with as many as 200 elementary functions.
- Suppose you are using the hierarchy to impose a meaningful structure on the content of your enterprise's 5,000 strong application portfolio (the largest reported to me), you might want a function/capability hierarchy with as many as 1,000 elementary functions.
- If you are using the hierarchy to impose a meaningful structure on the activities in your process models, then the **consistency principle** says function and process hierarchies come together at the bottom level where "atomic activities" aka elementary business processes (EBP) aka elementary business functions (EBF) are defined.

In practice, it seems nobody has the time and resources to complete both functional and process decompositions; but still, the principle holds - every activity in a process should be locatable under a function - else the function hierarchy is incomplete.

### A graphic

The graphic below is simplistic; a complete meta model would be considerably more complex. It doesn't show one activity can appear in several processes. And while an activity should not be repeated in one function hierarchy, it can appear in different ones.

![](1606945039503_e_1620259200_v_bet_9b8c214d1d404fd7a.jpg)
Note the two sub-types of process in the graphic. The passage of time can turn such mutually exclusive sub-types of an entity into states in its life history. Given a process or function decomposition, you might further decompose the bottom level, or else remove it. And you can decompose one view more than the other. Still, the principle that you could join the two views at the atomic activity level holds true.

## Concluding remark

This article shows the scope of what can be done to define business activity systems. But to model all the systems of a large enterprise from all these viewpoints is surely impossible. I don't find people have the time and budget to complete and maintain large enterprise-wide models outside of some particular initiative that they serve to illuminate.

Again, I'm not urging you to use all the terms and draw all the models/views discussed above. The aim here to present a holistic view of the terms and concepts you will find out there - to help you make sense of them, and select what you need.

There are no rules to say which views should be drawn in every particular situation you may find yourself in, or how detailed your models should be. E.g. For a particular application development project, it might enough to define a goal, model a process or two and model the data created and used by the activities in those processes.

[[A value stream for architects]]

## Further reading

This [slide show](https://www.linkedin.com/pulse/ea-ba-applied-system-theory-graham-berrisford) illustrates much of what this article says.

In [these related Linkedin articles](https://www.linkedin.com/in/grahamberrisford/detail/recent-activity/posts/)

- For more on systems thinking, read articles 1 and 2.
- For mapping business functions to microservices read article 9.

Some of this material appears in our [architect training courses](http://avancier.website/).

## APPENDIX 1: Where do capabilities fit?

Read [this other article](https://www.linkedin.com/pulse/Capability-oriented-business-architecture-graham-berrisford) for a capability-oriented variation of general method above, featuring value streams and capabilities, and a wider exploration of how the term capability is used.

### Capabilities in general

As explained earlier. a capability is always in 1-to-1 correspondence with another business architecture concept. A **capability** is an ability possessed by an actor (person, organization or system) to

- *do* something: to perform or realize some **process** or **function,** or
- *achieve* something: to meet some \*\*goal \*\*or produce some **outcome.**.

ArchiMate 3.1. says: A capability represents an ability that an active structure element, such as an organization, person, or system, possesses. In general system theory, you might say a capability is the ability of one or more actors to complete one or more activities and/or meet one or more aims.

Here, for compatibility with value stream modelling, we narrow the definition to this: a capability is the ability or wherewithal of one or more actors to complete one or more activities in one or more value streams.

### Every function needs to the capability to perform it

Function and capability are different concepts. Like other EA concepts, they could be related many-to-many, because both are composable and decomposable, and people may use different cohesion criteria when drawing function and capability hierarchies.

However, logically-speaking, as soon as you define a function, you necessarily require the corresponding capability to perform it, so the concepts can be, and often are, related in 1-to-1 correspondence.

A function hierarchy is a structured overview of the business activities needed to meet business aims. Since a capability hierarchy is an overview of the abilities or resources needed to perform the same activities to the same aims, the two hierarchies are often indistinguishable in appearance and possible uses (as the definition of "functional decomposition diagram" in TOGAF 9.2 implies). And if you remove the symbols from a capability map or a functional decomposition diagram you cannot be sure which it is.

### Processes recast as value streams

It is possible rewrite the general method above, replacing process by value stream, and replacing function by capability.

Since the early 1980s, EA has involved taking a holistic, cross-organizational view of value streams. A challenge for enterprise architects, in modelling business activities, is to model at cross-organization level. Architects may build abstract models of value streams (end to end processes) and capabilities (what is needed to complete value streams).

In BA in EA, a **value stream** is a sequence of stages, each composed of activities, triggered by an event, that terminates in a result or product of value to some external actor(s). There may be any number of optional, repeated and parallel activities in the stages of a value stream.

### Functions recast as capabilities

In BA in EA, since most use the concept to define what is required to complete the regular value streams (end-to-end processes) that a business performs, a **capability** is the ability or wherewithal to complete one or more activities in one or more value streams.

Whereas value streams sequence activities into stages, capabilities impose a simple logical composition structure on the resources need to complete value streams.

Following the **strict hierarchy** principle, no capability is duplicated under different branches of a capability hierarchy. To achieve that, you must stop decomposition when you reach a common capability and document it separately, or else in a "common capabilities" leg of the hierarchy.

Following the c**onsistency principle**: capability maps and value streams come together at the bottom level where "activities" are defined.

## APPENDIX 2: A little methodology history

### Structured Analysis and Design

From c1980, the UK government's structured analysis and design method included data flow diagrams (functions, data flows and data stores), entity-attribute-relationship models for the data stores, entity life histories (cf. state charts) for the entities, and process outlines for the events. Yourdon's structured analysis method also combined process, entity and state-oriented models to design business information systems.

Some structured methods were problem-solution specific. As the decade progressed, James Martin and others took a more enterprise-wide view of business processes and data. Tools include enterprise-wide functional decomposition alongside data flow diagrams and cross-organisational data entity-function matrices.

### Object-Oriented Analysis and Design

Around 1990, the fashion/hysteria surrounding OO obscured the business activity system modelling of the 1980s. OOAD was supposed to sweep away all before it. Jumping on the bandwagon, Yourdon announced “The data flow diagram is dead”. This diversion of attention from business activity modelling to software object modelling helps to explains the widespread ignorance today of business function and process modelling principles.

### Service-oriented business architecture (SOBA)

A service is a declarative and external view of a behavior required from a system. It can be defined in a service contract that identifies entry conditions, exit conditions and non-functional qualities.

How a service works internally (presumed irrelevant to a service requester or consumer) can be specified in one or more processes, along with the roles of internal actors in those processes.

### Microservices architecture

If you cluster the activities that maintain a cohesive, tightly related, set of data entities, then the resulting function is what Martin Fowler calls a "business capability", which may be supported by a *microservice*. For more on microservices, read article 9.

The term capability has long been used in other connections. Read appendix 1 above for further discussion of capabilities.