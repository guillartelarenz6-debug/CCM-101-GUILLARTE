
# Laboratory Activity 04: The Cloud-Native Engineer

## Mission Overview
This laboratory activity introduces cloud-native containerization principles by transitioning from traditional virtual machine infrastructure to lightweight container deployments using Docker on the KillerCoda platform.

## Objectives
* Differentiate the architecture and performance differences between VMs and Containers.
* Access and navigate a Docker-enabled cloud environment.
* Execute fundamental Docker CLI commands.
* Pull, deploy, manage, and remove an Nginx containerized web server.
* Create structured technical documentation and update the cloud computing portfolio on GitHub.

## Docker Commands Executed
* `docker --version` & `docker info` — Verified the Docker installation status and system runtime details.
* `docker pull nginx` — Downloaded the official Nginx web server image from Docker Hub.
* `docker run -d -p 8080:80 --name my-nginx-server nginx` — Deployed the Nginx container in detached mode and mapped host port 8080 to container port 80.
* `curl http://localhost:8080` — Tested local web server response and confirmed successful deployment.
* `docker ps` — Listed all actively running containers.
* `docker stop my-nginx-server` — Safely stopped the running Nginx container.
* `docker ps -a` — Verified that the container was stopped.
* `docker rm my-nginx-server` — Permanently removed the container from the host system.

## Screenshots Evidence
* **Docker Version:** `screenshots/docker-version.png`
* **Nginx Running:** `screenshots/nginx-running.png`
* **Container Lifecycle:** `screenshots/container-lifecycle.png`

## Skills Learned
* Managing application execution using Docker CLI.
* Configuring port mapping and Network Address Translation (NAT) between host and container environments.
* Hands-on application lifecycle operations (Pull, Run, Inspect, Stop, Remove).

## Challenges Encountered
* Understanding port binding concepts (`host_port:container_port`) and verifying background processes in a cloud terminal playground.
