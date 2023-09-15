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

Os-kernel+application Kernal-core interacts with hardware and software

- Size: docker high

- Speed: docker high

- Docker Containers
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

Easy to run different versions of same app without any conflicts
Linux (manual installation)
```bash
$ wget https://raw.githubusercontent.com/ekalinin/github-markdown-toc/master/gh-md-toc
$ chmod a+x gh-md-toc
```
