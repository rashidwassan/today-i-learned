# Docker
- Docker can be simply explained as advanced version of virtulization.
- Docker is used for containerization.
- Container is just like a virtual machine.
- Docker a set of PaaS (Platform as a Service).
- Docker is an open-source centralized platform designed to build, deploy, and run applications.
- Container is like a virtual machine and docker is the tool which creates this virtual machine.
- Docker is actually an engine (Docker Daemon).
- VMs made easier to move whole project environment with OS.
- Docker is just like an advanced version of virtualisation.
- Docker does containerization. 
- Bare metal hypervisor is type1 hypervisor.
- Like we have ESXi hypervisor from VMware or Xen/Nitro in AWS. Docker on the other hand, has Docker engine sitting on top of host OS.
- Docker is written in GoLang.



### Scenario
Considering the scenario of developer sending the build to tester, and the product refuses to run.

## History

- In early days, the problem of migrating builds with needed plugins was sovled by the virtual machines.
- Being heavyweight, VMs proved to be very inefficient.
- The problems that VMs had we to be addressed.
- This gave birth to the Docker.
- Docker was released in 2013
- Developed by Soloman Hykes and Sebastian Paul.
- Traditionally, a VM sits on top of the hypervisor, which sits on host operating system, which again sits on top of the hardware.
- In containerization, Container sits on top of the Docker engine which then sits on OS sitting on hardware.

## Containers
- Container is 
- Multiple containers run on single kernel unlike VMs. 

## Docker Engine
- Docker engine is responsible for virtualization.
- Docker engine runs natively on Linux. Uses Linux code when installed on Windows system.

## Virtualization
- Docker uses OS level virtualization. VMs use hardware level virtualization.
- In OS level virtualization, the container takes resources from OS rather than hardware.
## Docker Hub
- Dependencies come from Docker hub.

## Memory Save
- Containers have dynamic memory allocation unlike VMs, which saves a lot of memory as we don't have any memory lock.

## Docker & Chef
- Docker creates containers and Chef configures them.

## Docker in Windows
- If docker is running on Windows OS, the code inside containers in of Linux.

## Running Multiple Linux Distros
- As most of the Linux distros have huge similar codebase. We don't need to spearately install them.
- We can use that base codebase and add things on top of that to run multiple different distros without any problem.

## Compatibility
- Docker runs navtively on Linux.
- It supported on Windows 10 and newer versions of OS.
- Docker tool contains necessary Linux files, eliminating the need of whole Linux image for each container on Windows.