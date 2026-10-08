# Laboratory-06-Cloud-Deployment-Engineer

## Mission Overview

This laboratory activity is part of the Cloud Computing course under **Mission 6: The Cloud Deployment Engineer**. The mission focuses on transitioning from manually deploying single containers to orchestrating multi-container applications using **Docker Compose** — an Infrastructure as Code (IaC) approach.

As a Cloud Deployment Engineer at **CloudNova Technologies**, the goal is to deploy a proof-of-concept private cloud storage system for a university client using **Nextcloud** (web/application tier) and **MariaDB** (database tier). These two containers are linked together through a single `docker-compose.yml` file and deployed with a single command.

The mission reinforces the guiding principle:

> *"Be the pilot of AI, not the passenger."*

---

## Objectives

At the end of this laboratory activity, I should be able to:

- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Use a Linux command-line text editor (`nano`) to create configuration files.
- Deploy a multi-container application (Nextcloud + MariaDB) using Docker Compose.
- Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown.
- Continue expanding my professional GitHub Cloud Computing Portfolio.

---

## Commands Executed

```bash
# Checkpoint 3 - Create project directory
mkdir nextcloud-deployment
cd nextcloud-deployment

# Checkpoint 3 - Create the Compose file using nano
nano docker-compose.yml

# Checkpoint 4 - Deploy the multi-container stack in the background
docker-compose up -d

# Checkpoint 4 - Verify running containers
docker-compose ps

# Checkpoint 5 - Gracefully shut down the infrastructure
docker-compose down
