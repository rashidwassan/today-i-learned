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
- Containers have layered file system.
- It holds the entire packages that are needed to run the applications.

## Image
- Image is snapshot of a container, it is a read only binary for building docker containers.
- You cannot change or modify the image.

## Ways to create an image
    - Take image from docker hub.
    - Create image form docker file.
    - Create image from existing containers. 

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

## Disadvantages:
- Cross platform issues with containers. It is highly recommended to have same OS across different devices to run containers.
- Difficult to manage large number of containers.
- Not a good solution for GUI rich applications.
- Docker is suitable only if development and testing environments are same.

## Docker Ecosystem

### Docker Client
- Where we will code & create a docker file.
- It is used to communicate with docker daemon.
- Communication can be through CLI or REST API.

### Docker Daemon/Server
- Where Docker Engine resides.
- Builds and runs images.
- It runs on the host OS.

### Docker Hub / Docker Registry
- The place where all the images are stored.
- Registeries can be public (AKA Docker Hub) or private.
- Private registeries are only accessible within an entreprise.

### Docker Host
- Sits on a very lower level in docker ecosystem.
- It provides the enviroment to run docker applications.

# Docker Commands
## docker images
- To see all images present in your local machine.

## docker search ubuntu
- Searches for ubuntu package on Docker hub.
- Will display the different versions of imgages of packages as well.

## docker pull ubuntu
- Used to download images from docker hub to local machine.

## docker run -it --name rashid ubuntu
- Here, run means to create and start and -it is flag for interactive mode + terminal.
- The word right after --name flag will be name which will be given to that container.

## service docker status
- Checks if docker is running or not (it didn't work in MacOS).

## docker attach ubuntu
- To go inside that container.

## docker ps
- To see how many containers are currently running.

## docker ps -a
- To see how many containers are currently running or are offline (lists all container available).

## docker stop ubuntu
- To stop a running container.

## docker rm <ContainerName>
- Removes ubuntu container.