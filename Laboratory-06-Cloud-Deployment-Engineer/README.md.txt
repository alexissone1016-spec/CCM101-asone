# Laboratory 06 – Cloud Deployment Engineer

## Mission Overview

This laboratory activity transitions from manually deploying single containers
to defining and deploying a **multi-tier application** using **Docker Compose**
as Infrastructure as Code (IaC).

The mission simulates a real client engagement at **CloudNova Technologies**,
where a university wants to replace a commercial cloud drive with a
self-hosted, private cloud storage solution. Using Docker Compose, we
deploy **Nextcloud** (web tier) and **MariaDB** (database tier) as one
orchestrated stack with a single command.

## Objectives

By the end of this laboratory, I will be able to:

- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Use a Linux command-line text editor (`nano`) to create configuration files.
- Deploy a multi-container application (Nextcloud + MariaDB) using Docker Compose.
- Document deployment procedures and IaC principles using Markdown.
- Expand my professional GitHub Cloud Computing Portfolio.

## Commands Executed

```bash
# Project setup
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml

# Deploy the stack in detached mode
docker-compose up -d

# Verify running containers
docker-compose ps

# Tear down the stack
docker-compose down