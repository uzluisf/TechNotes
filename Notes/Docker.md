# Docker

## High Level Definition of a Container
A **container** is a way to package applications with all the necessary dependencies and configuration.
	- A container is a portable artifact, that can be easily shared and moved around between development teams or development team and operations team.
	- Make development and deployment easy.

## Where Do Containers Live?
Containers live in a container repository. Containers live either in:
- **Private repositories.** Many companies have private repositories where they keep their containers.
- **Public repository.** [DockerHub](https://hub.docker.com/) is a public repo for Docker containers, where you can browse and get containers from.

## How Have Containers Improved the Application Development Process?
**Without containers**, every developer in a team needed to install all the binaries and configure them in their local development environment. 
- Depending on their operating system, the installation process looked different. 
- Since each developer needed to configure the binaries independently, there was a chance for many things to go wrong due to the number of steps.

**With containers**, the developer doesn't need to install any of the binaries and/or services directly in his operating system because the container is its own isolated environment, with everything packaged with all needed configuration for the application to work. 
- Configuration, binaries, and start script is packaged into a container.
- All is needed is to fetch the container and run it. Thus, only one single command to install the app.
- You can run 2 different versions of the same application running in your local environment without conflicts.

## Technical Definition of a Container
- A container is made-up of images. Think of them as layers of images stacked on top of one another.
- At the base of a container, there's mostly a **Linux Base Image**. Some version of Alpine Linux is used, because of its small size since it's advantageous to keep the container small in size.
- On top of the Linux Base Image, there are **Application Image**. There are intermediate images that sit between the Linux Base Image and the Application Image.
- On top of the Application Image, you've the configuration data.

## Docker Image vs Docker Container

Although people use these terms interchangeably, there's fine difference between the two terms:
- A **docker image** is the actual package: the application, the configuration, and start script all packaged together. This is the artifact that's moved around.
- A **docker container** is when you pull an image in your local machine, run it, and start the application inside of it. This creates the container environment for the application.

Thus,
* **not running**, then it's an image.
* **running**, then it's a container.

## Docker vs Virtual Machine (VM)
- Docker virtualizes the applications layer of an OS, and it uses the kernel of the host machine it runs on.
- A VM virtualizes both the applications layer and the OS kernel (the VM has its own kernel), and communicate directly with the hardware.

The main differences between Docker and a VM are:
- **Size:** A Docker image is much smaller.
- **Speed.** A Docker container starts and runs much faster.
- **Compatibility.** VM of any OS can run on any OS host. You cannot do this with Docker. This is the reason why Docker doesn't work with machines running Windows versions below 10, i.e., the Linux-based Docker image isn't compatible with the Windows kernel.

## Docker Installation
### Mac

### Linux

## Main Docker Commmands

|Command| Meaning |
|:------------|:----------|
|`docker images`| List all the docker images in the machine|
|`docker ps`|List all the running containers in the machine. Run with `-a` to list running and stopped containers.|
|`docker run`| Run with `-d` to run container in detached mode|
|`docker stop <id>`|Stop container with `id`|
|`docker start <id>`|Start container with `id`|

Tags: #fleeting

