---
layout: post
title: Understanding Virtual Machine
author: Nilesh Sharma
---

What is a virtual machine, What are it's uses ?

## Understanding Virtual Machine
-----

A virtual machine is a software computer that, like a physical machine, runs an operating system and applications. It adds software to a physical machine to give it the appearance of a different platform or multiple platforms.

It uses the physical resources of the physical machine on which it runs, which is called the host system. Virtual machines have virtual devices that provide the same functionality as physical hardware.

Some of the benefits of virtual machines are:

- Cross platform compatibility
- Increase Security
- Enhance Performance
- Simplify software migration

A virtual machine has an operating system and virtual resources that you manage in much the same way that you manage a physical computer. For example, you install an operating system in a virtual machine in the same way that you install an operating system on a physical computer.

Your virtual machine’s operating system is stored on a virtual hard drive — a big, multi-gigabyte file stored on your hard drive. The file is presented to the operating system as a real hard drive. This means you won’t have to mess around with partitioning.

Ideally virtual machines won’t be as fast as if you had installed the operating system on real hardware.

Virtual machines are also “sandboxed” from the rest of your system, which means that software inside a virtual machine can’t escape the virtual machine and tamper with the rest of your system. A virtual machine can be a good place to rest out programs you don’t trust and see what they do.

For creating virtual machine and resource allocation to it we generally use a device or software which we call Hypervisor.

## Hypervisor
-----
The hypervisor also called as virtual machine manager is the device or software which runs the virtual machine. It's typically responsible for allocating the resources, providing the interface between the virtual machine (the "guest") and the host system as well as any management software. It also makes sure that virtual machines cannot disrupt each other.

So if you're using VMware Workstation to run a Windows 7 virtual machine, VMware Workstation is the hypervisor.

The overall architecture of virtual machines looks something like this:

![virtual-machine-architecture](https://2.bp.blogspot.com/_AXUmwddhdfA/TP1-XWhvypI/AAAAAAAAAzg/3x7aEDsiqu4/s1600/Virtual+Machines.png)

