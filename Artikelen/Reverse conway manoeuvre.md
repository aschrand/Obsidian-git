---
created: 2023-02-10T14:37:24 (UTC +01:00)
tags: [EA]
source: https://www.zensoftware.nl/nieuws/2022/6/team-topologies-the-reverse-conway-manoeuvre
author: Arjan Franzen
type: artikel
---

# Team Topologies - The Reverse Conway Manoeuvre | ZEN Software

> [!abstract]
> Optimise your software architecture and delivery for optimal flow by performing the Reverse Conway Manoeuvre.

---

From the book [“Team Topologies”](https://partner.bol.com/click/click?p=2&t=url&s=1228221&f=TXL&url=https%3A%2F%2Fwww.bol.com%2Fnl%2Fnl%2Ff%2Fteam-topologies%2F9200000104858740%2F&name=Team%20Topologies) by Matthew Skelton and Manuel Pais comes an interesting fix to [[Conways-law]]:

# The Reverse Conway Manoeuvre

To increase an organisation’s chances of building effective software systems optimised for end-to-end flow, a _“Reverse Conway Manoeuvre”_ (or Inverse Conway Manoeuvre) can be undertaken to reconfigure the team intercommunications before the software is finished.

Nicole Forsgren wrote about this first, back in 2015, in her excellent book [Accelerate](https://partner.bol.com/click/click?p=2&t=url&s=1228221&f=TXL&url=https%3A%2F%2Fwww.bol.com%2Fnl%2Fnl%2Fp%2Faccelerate%2F9200000080652224%2F&name=Accelerate).

> Our research lends to support to what is sometimes called the 'inverse Conway maneuver,” which states that organizations should evolve their team and organizational structure to achies the desired architecture. The goal is for your architecture to support the ability of teams to get their work done - from design through to deployment - without requiring high-bandwidth communication between teams

Before: Organisation (figure 1)

Let’s look at a deliberate simplification of Conway’s law in an organisation that develops software. In the first (out of 4) figure, you see four teams each comprised of front-end and back-end developers. They work on different parts of a system and then hand them over to a central database administrator (DBA) for database changes. The flow of changes may look like Figure 1.

![[Pasted image 20230210144038.png]]
Figure 1: Organisation Pre-Manoeuvre

# Before: Architecture (figure 2)

According to Conway’s law, the software architecture that naturally emerges from such a team design would have separate front-end and back-end components for each team and a single, shared core database (Figure 2). In other words, the use of a shared DBA team is likely to drive the emergence of a single shared database; the same goes, in the opposite direction, for Front-end and Back-end developers: it will lead to separate UI and app tiers, see figure 2.


![[Pasted image 20230210144109.png]]
Figure 2: Architecture Pre-Manoeuvre

After: Organisation (figure 3)

We now apply the Reverse Conway Manoeuvre and design our teams to match the required software architecture by having a separate developer for the client applications and the API, and a database developer within the team rather than separate it, see figure 3.

![28fc8ed1-d943-401c-867f-a15190502af9.webp](https://www.zensoftware.nl/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fzensoftwaresite-media-zen-platform%2F28fc8ed1_d943_401c_867f_a15190502af9_1d359122ad%2F28fc8ed1_d943_401c_867f_a15190502af9_1d359122ad.webp&w=3840&q=75)

Figure 3: Organisation using Microservices

# After: Architecture (figure 4)

According to Conway’s law, this team design in the organisation will most ‘naturally’ produce the desired software architecture. Each of the separate teams has a self-sustaining system, no central database, and by having end-to-end capabilities using client and API developers in the team and datastore knowledge handy, the team and architecture are optimised for end-to-end flow! see figure 4.

![[Pasted image 20230210144145.png]]
Figure 4: Architecture, microservices and post Conway Manoeuvre

# Software Delivery

Conway’s law is not exclusively applicable to Software development: software delivery and software deployment can suffer from Conway’s Law.

If we consider the following pipeline with a centralised QA and Operations (pre-DevOps) you will get ‘interesting’ releases of your product.
![[Pasted image 20230210144253.png]]

Optimising for end-to-end flow and changing the organisation because of this optimisation has been a standard practice since Continuous Delivery gained popularity in 2012. We make QA and Ops part of the new ‘delivery teams’ in this scenario. We transform the central QA and central Ops into a distributed team that operates inside the different end-to-end optimised teams. (DevOps, BizDevOps etc.)

![[Pasted image 20230210144318.png]]
What remains are the platforms: these are maintained by the platform teams. We’ve written a good article about this here on our site: [How to setup a successful Cloud Platform Team](https://zensoftware.nl/en/news/2022/6/how-to-setup-a-successful-cloud-platform-team).

# Conclusion

For software architecture and software delivery, the organisation and communication lines in it are best explained by ‘Conway’s Law'. By performing the **Reverse Conway Manoeuvre**, you change the organisation to optimise your software architecture and delivery for optimal flow.

Observing and managing end-to-end flow is at the core of our product. Agile Analytics provides critical insights into your organisation’s software development operation.
