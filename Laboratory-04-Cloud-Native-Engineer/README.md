# Laboratory Activity 04: The Cloud-Native Engineer

**Course:** CCM 101 - Cloud Computing Architecture & System Administration  
**Author:** Larenz A. Guillarte  
**Section:** BSIT 4F  
**Institution:** University of Eastern Pangasinan  

---

## Mission Overview
This laboratory activity introduces cloud-native containerization principles by transitioning from traditional Virtual Machine (VM) infrastructure to lightweight container deployments using Docker on the KillerCoda platform. 

## Objectives
* Differentiate the architecture, performance, and resource utilization between Virtual Machines and Containers.
* Access and navigate a Docker-enabled cloud playground environment using KillerCoda.
* Execute fundamental Docker CLI (Command Line Interface) commands.
* Pull, deploy, test, and manage an Nginx containerized web server.
* Create structured technical documentation and expand the cloud computing portfolio on GitHub.

---

## Technical Reports & Documents
* **VMs vs. Containers:** [`virtualization-vs-containers.md`](./virtualization-vs-containers.md)
* **Docker Deployment & Lifecycle:** [`docker-deployment.md`](./docker-deployment.md)
* **Mission Reflection:** [`reflection.md`](./reflection.md)

---

## Docker Commands Executed

### 1. Environment Verification
* `docker --version` — Displayed the installed Docker client version.
* `docker info` — Verified the operational status of the Docker system engine and daemon.

### 2. Deployment & Testing
* `docker pull nginx` — Downloaded the official Nginx container image from Docker Hub.
* `docker run -d -p 8080:80 --name my-nginx-server nginx` — Deployed an Nginx container instance in detached mode (`-d`), mapping host port `8080` to container port `80`.
* `curl http://localhost:8080` — Verified local network connectivity and confirmed successful web server initialization.

### 3. Lifecycle Operations
* `docker ps` — Listed active, running container processes.
* `docker stop my-nginx-server` — Gracefully stopped the running Nginx container.
* `docker ps -a` — Listed all container instances (including stopped ones) to verify container shutdown.
* `docker rm my-nginx-server` — Permanently deleted the container instance from the system.

---

## Evidence Screenshots
All command output screenshots are documented and available inside the [`screenshots/`](./screenshots) directory:
* **Docker Verification:** `screenshots/docker-version.png`
* **Nginx Deployment Output:** `screenshots/nginx-running.png`
* **Container Lifecycle Execution:** `screenshots/container-lifecycle.png`

---

## Skills Learned
* Container orchestration basics using the Docker Command Line Interface.
* Network Address Translation (NAT) and port binding mechanics between host and isolated container environments (`host_port:container_port`).
* Managing application lifecycle states (Pull, Run, Inspect, Stop, Remove).
* Writing structured Markdown documentation for cloud system administration tasks.

## Challenges Encountered
* Understanding port mapping mechanics and ensuring host ports correctly route traffic into isolated container namespaces in a web-based terminal.
