---
title: 'Explain Docker Containers vs VMs?'
---

Docker vs Virtual Machines (VMs)
================================

**Boot-Time**
-------------

Docker boots in a few seconds. While it takes a few minutes for VMs to
boot.

**Runs on**
-----------

Dockers make use of the execution engine. While VMs make use of the
hypervisor.

**Memory Efficiency**
---------------------

No space is needed to virtualize Docker, hence less memory. While VM
Requires entire OS to be loaded before starting the surface, so less
efficient.

**Isolation**
-------------

Dockers prone to adversities as no provisions for isolation systems. VMs
has iinterference possibility is minimum because of the efficient
isolation mechanism.

**Deployment**
--------------

Deploying Docker is easy as only a single image, containerized can be
used across all platforms. Deployment of VMs is comparatively lengthy as
separate instances are responsible for execution.

**Usage**
---------

Docker has a complex usage mechanism consisting of both third party and
docker managed tools. While VMs tools are easy to use and simpler to
work with.

Explain Docker Architecture?

Docker Architecture
===================

Before learning the Docker architecture, first, you should know about
the Docker Daemon.

What is Docker daemon?
======================

Docker daemon runs on the host operating system. It is responsible for
running containers to manage docker services. Docker daemon communicates
with other daemons. It offers various Docker objects such as images,
containers, networking, and storage. s

Docker architecture
===================

Docker follows Client-Server architecture, which includes the three main
components that are **Docker Client**, **Docker Host**, and **Docker
Registry**.

![](media/image1.png){width="6.283581583552056in"
height="3.7914534120734906in"}

1. Docker Client
----------------

Docker client uses **commands** and **REST APIs** to communicate with
the Docker Daemon (Server). When a client runs any docker command on the
docker client terminal, the client terminal sends these docker commands
to the Docker daemon. Docker daemon receives these commands from the
docker client in the form of command and REST API's request.

### Note: Docker Client has an ability to communicate with more than one docker daemon.

Docker Client uses Command Line Interface (CLI) to run the following
commands -

-   docker build

-   docker pull

-   docker run

2. Docker Host
--------------

Docker Host is used to provide an environment to execute and run
applications. It contains the docker daemon, images, containers,
networks, and storage.

3. Docker Registry
------------------

Docker Registry manages and stores the Docker images.

There are two types of registries in the Docker -

**Pubic Registry -** Public Registry is also called as **Docker hub**.

**Private Registry -** It is used to share images within the enterprise.

Docker Objects
==============

There are the following Docker Objects -

Docker Images
-------------

Docker images are the **read-only binary templates** used to create
Docker Containers. It uses a private container registry to share
container images within the enterprise and also uses public container
registry to share container images within the whole world. Metadata is
also used by docket images to describe the container's abilities.

Docker Containers
-----------------

Containers are the structural units of Docker, which is used to hold the
entire package that is needed to run the application. The advantage of
containers is that it requires very less resources.

In other words, we can say that the image is a template, and the
container is a copy of that template.

![](media/image2.png){width="5.90625in" height="2.2604166666666665in"}

Docker Networking
=================

Using Docker Networking, an isolated package can be communicated. Docker
contains the following network drivers -

-   **Bridge -** Bridge is a default network driver for the container.
    It is used when multiple docker communicates with the same
    docker host.

-   **Host -** It is used when we don't need for network isolation
    between the container and the host.

-   **None -** It disables all the networking.

-   **Overlay -** Overlay offers Swarm services to communicate with
    each other. It enables containers to run on the different
    docker host.

-   **Macvlan -** Macvlan is used when we want to assign MAC addresses
    to the containers.

Docker Storage
==============

Docker Storage is used to store data on the container. Docker offers the
following options for the Storage -

-   **Data Volume -** Data Volume provides the ability to create
    persistence storage. It also allows us to name volumes, list
    volumes, and containers associates with the volumes.

-   **Directory Mounts -** It is one of the best options for
    docker storage. It mounts a host's directory into a container.

-   **Storage Plugins -** It provides an ability to connect to external
    storage platforms.
