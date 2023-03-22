---
title: Containerization
type: definitie
updated: 2021-03-02 14:07:40Z
created: 2021-01-20 11:57:57Z
tags:
  - EA
  - IT
---

 # What Are Containers?
 Containers sit on top of a physical server and its host OS—for example, Linux or Windows. Each container shares the host OS kernel and, usually, the binaries and libraries, too. Shared components are read-only. Containers are thus exceptionally “light”—they are only megabytes in size and take just seconds to start, versus gigabytes and minutes for a VM [[Containers vs. VM]]
 
Containers also reduce management overhead. Because they share a common operating system, only a single operating system needs care and feeding for bug fixes, patches, and so on. This concept is similar to what we experience with hypervisor hosts: fewer management points but slightly higher fault domain. In short, containers are lighter weight and more portable than VMs.

[[Server Virtualization Definition]]