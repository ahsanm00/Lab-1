EXPLAIN DOCKER CONTAINERS VS VMS? 



||||
| :- | :- | :- |
||**DOCKER** ||**VIRTUAL MACHINES (VMS)** ||
||Boots in a few seconds. ||It takes a few minutes for VMs to boot. ||
|**BOOT-TIME** |||||
||||||
||Dockers make use of the execution engine. ||VMs make use of the hypervisor. ||
|**RUNS ON** |||||
||||||
||No space is needed to virtualize, hence less memory. ||Requires entire OS to be loaded before starting the surface, so less efficient. ||
|**MEMORY EFFICIENCY** |||||
||||||
||Prone to adversities as no provisions for isolation systems. ||Interference possibility is minimum because of the efficient isolation mechanism. ||
|**ISOLATION** |||||
||||||
||Deploying is easy as only a single image, containerized can be used across all platforms. ||Deployment is comparatively lengthy as separate instances are responsible for execution. ||
|**DEPLOYMENT** |||||
||||||
||Docker has a complex usage mechanism consisting of both third party and docker managed tools. ||Tools are easy to use and simpler to work with. ||
|**USAGE** |||||
||||||
EXPLAIN DOCKER ARCHITECTURE? 

DOCKER ARCHITECTURE ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.001.png)

Before learning the Docker architecture, first, you should know about the Docker Daemon. 

WHAT IS DOCKER DAEMON? ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.002.png)

Docker daemon runs on the host operating system. It is responsible for running containers to manage docker services. Docker daemon communicates with other daemons. It offers various Docker objects such as images, containers, networking, and storage. s 

DOCKER ARCHITECTURE ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.003.png)

Docker follows Client-Server architecture, which includes the three main components that are **Docker Client**, **Docker Host**, and **Docker Registry**. 

![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.004.png)

1. DOCKER CLIENT ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.005.png)

Docker  client  uses **commands** and **REST  APIs** to  communicate  with  the  Docker Daemon (Server). When a client runs any docker command on the docker client terminal, the client terminal sends these docker commands to the Docker daemon. Docker daemon receives these commands from the docker client in the form of command and REST API's request. ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.006.png)

NOTE: DOCKER CLIENT HAS AN ABILITY TO COMMUNICATE WITH MORE THAN ONE DOCKER DAEMON. 

Docker Client uses Command Line Interface (CLI) to run the following commands - 

- docker build 
- docker pull 
- docker run 
2. DOCKER HOST ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.007.png)

Docker Host is used to provide an environment to execute and run applications. It contains the docker daemon, images, containers, networks, and storage. 

3. DOCKER REGISTRY ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.008.png)

Docker Registry manages and stores the Docker images. 

There are two types of registries in the Docker - 

**Pubic Registry -** Public Registry is also called as **Docker hub**. **Private Registry -** It is used to share images within the enterprise. DOCKER OBJECTS ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.009.png)

There are the following Docker Objects - 

DOCKER IMAGES ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.010.png)

Docker images are the **read-only binary templates** used to create Docker Containers. It uses a private container registry to share container images within the enterprise and also uses public container registry to share container images within the whole world. Metadata is also used by docket images to describe the container's abilities. 

DOCKER CONTAINERS ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.007.png)

Containers are the structural units of Docker, which is used to hold the entire package that is needed to run the application. The advantage of containers is that it requires very less resources. 

In other words, we can say that the image is a template, and the container is a copy of that template. 

![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.011.png)

DOCKER NETWORKING ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.003.png)

Using Docker Networking, an isolated package can be communicated. Docker contains the following network drivers - 

- **Bridge -** Bridge is a default network driver for the container. It is used when multiple docker communicates with the same docker host. 
- **Host  -** It  is  used  when  we  don't  need  for  network  isolation  between  the container and the host. 
- **None -** It disables all the networking. 
- **Overlay -** Overlay offers Swarm services to communicate with each other. It enables containers to run on the different docker host. 
- **Macvlan -** Macvlan is used when we want to assign MAC addresses to the containers. 

DOCKER STORAGE ![](Aspose.Words.91046703-e3e1-41ee-bc64-9a18ef1f251d.012.png)

Docker Storage is used to store data on the container. Docker offers the following options for the Storage - 

- **Data Volume -** Data Volume provides the ability to create persistence storage. It also allows us to name volumes, list volumes, and containers associates with the volumes. 
- **Directory Mounts -** It is one of the best options for docker storage. It mounts a host's directory into a container. 
- **Storage  Plugins  -** It  provides  an  ability  to  connect  to  external  storage platforms. 
