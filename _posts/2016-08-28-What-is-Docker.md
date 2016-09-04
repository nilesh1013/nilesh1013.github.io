---
layout: post
title: What is Docker ?
author: Nilesh Sharma
---
Docker is an open-source project which automates the deployment of Linux applications inside software containers.

## What is Docker ?
-----
From the Docker website: Docker containers wrap up a piece of software in a complete filesystem that contains everything it needs to run: code, runtime, system tools, system libraries – anything you can install on a server. This guarantees that it will always run the same, regardless of the environment it is running in.


![docker-machine-architecture](https://www.docker.com/sites/default/files/WhatIsDocker_3_Containers_2_0.png)

## Some good things about Docker is:
-----
- Rapid application deployment – containers include the minimal runtime requirements of the application, reducing their size and allowing them to be deployed quickly.

- Portability across machines – an application and all its dependencies can be bundled into a single container that is independent from the host version of Linux kernel, platform distribution, or deployment model. This container can be transfered to another machine that runs Docker, and executed there without compatibility issues.

- Version control and component reuse – you can track successive versions of a container, inspect differences, or roll-back to previous versions. Containers reuse components from the preceding layers, which makes them noticeably lightweight.

- Sharing – you can use a remote repository to share your container with others for example: DockerHub. For this purpose, and it is also possible to configure your own private repository.

- Lightweight footprint and minimal overhead – Docker images are typically very small, which facilitates rapid delivery and reduces the time to deploy new application containers.

- Simplified maintenance – Docker reduces effort and risk of problems with application dependencies.



