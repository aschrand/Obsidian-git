---
created: 2023-01-19T15:27:28 (UTC +01:00)
tags: [Virtualization, IT]
type: definitie
--- 

# Three Kinds of Server Virtualization
There are three ways to create virtual servers: **full virtualization**, **para-virtualization** and **OS-level virtualization**. They all share a few common traits. The physical server is called the host. The virtual servers are called guests. The virtual servers behave like physical machines. Each system uses a different approach to allocate physical server resources to virtual server needs.

Full virtualization uses a special kind of software called a **hypervisor**. The hypervisor interacts directly with the physical server's CPU and disk space. It serves as a platform for the virtual servers' operating systems. The hypervisor keeps each virtual server completely independent and unaware of the other virtual servers running on the physical machine. Each guest server runs on its own OS -- you can even have one guest running on Linux and another on Windows.

The para-virtualization approach is a little different. Unlike the full virtualization technique, the guest servers in a para-virtualization system are aware of one another. A para-virtualization hypervisor doesn't need as much processing power to manage the guest operating systems, because each OS is already aware of the demands the other operating systems are placing on the physical server. The entire system works together as a cohesive unit.

[[Serverless]]
[[Server Virtualization Definition]]
[[Containers vs. VM]]
[[Why Virtualization]]
