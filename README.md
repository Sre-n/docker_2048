# docker_2048

A demo project to understand how docker works

Manual
=================

<!--ts-->
   * [Introduction](#introduction)
      * [Why Docker](#why)
      * [Virtual Machine vs Docker](#differences)
      * [Early](#early)
      * [Docker Registry](#docker-registry)
      * [Docker Repository](#docker-repository)
      * [Docker Container](#docker-container)
   * [Installations](#installations)
   * [Dependency](#dependency)
   * [Docker](#docker)
     * [Local](#local)
     * [Public](#public)
<!--te-->


Introduction
============

- Virtualization Software

- Makes developing and deploying applications easier

- Packages application with all necessary dependencies, configuration, system tools and runtime

Why Docker
-----
Before:

▲ Each developer install and configure all services directly on OS in local machine.

▲ Different process for each OS Steps may go wrong

▲ If 10 services, each developer install these 10 services

Deplyments before 

▲ Development (Artifacts)-> Server-> Operation (installation and configurations)
Problems: miscommunication-human errors

Virtual Machine VS Docker
-----
![image](https://github.com/Sre-n/docker_2048/assets/92539781/a6031894-c86f-4b56-ba1a-de7b6f8ca145)
Os-kernel+application Kernal-core interacts with hardware and software

- Size: docker high

- Speed: docker high

Docker Containers
-----

- Own isolated environment

- Each packaged with all dependencies and configure

- start application

- running instance of image
  
- Starts services with just 1 command for all services and OS

- Artifacts include everything app needs: configuration, source code, dependencies

Docker Images
-----

- executable application artifact

- app source code, environment configuration

- immutable template defines how container is realized

Run multiple containers from 1 image

Docker Registry
-----

- storage and distribution system for docker images

- official images maintained in collaboration with docker

- docker hub

Docker Repository
-----

- collection of related images with same name but different versions

![image](https://github.com/Sre-n/docker_2048/assets/92539781/f2606bab-c682-416f-a509-811a26c83910)


PREREQUISITE
============

Easy to run different versions of same app without any conflicts
Linux (manual installation)
```bash
sudo apt install gnome-terminal
```

```bash
rm -r $HOME/.docker/desktop
sudo rm /usr/local/bin/com.docker.cli
sudo apt purge docker-desktop
```

```bash
sudo apt-get update
sudo apt-get install ./docker-desktop-<version>-<arch>.deb
```
2048 Procedure
============

1. Clone the given repository
```bash
git clone https://github.com/Sre-n/docker_2048
```

2. Connect to docker daemon
```bash
sudo systemctl daemon-reload
```

3. Start building
```bash
docker build -t 2048-game .
```

4. Check if an image is created or not
```bash
docker images
```

5. Run in port by providng image id generated from previous command
```bash
docker run -d -p 80 <image-id>
```
REFERENCES
-----------
-----------

https://codeload.github.com/gabrielecirulli/2048
