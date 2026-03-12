# Coursey On-Premise

**Coursey** is a web platform designed for real-time learning, where users can access courses and materials instantly and interactively. This repository contains the on-premise Kubernetes deployment version, migrating from an AWS managed services architecture to a fully self-hosted environment.

![System Overview](img/main_page.png)

## System Overview

![System Overview](img/overview_system.png)

## Detailed Documentation & Migration Guide

> **IMPORTANT:**
> The complete, step-by-step deployment guide, environment setup, and the entire process of how this project was migrated from AWS to On-Premise have been thoroughly documented in the report.
> 
> 📄 **Please refer to the `Coursey-migration-report.pdf` file for all instructions on how to build, deploy, and manage the system.**

## Prerequisites

To run and manage this on-premise environment, you will need the following prerequisites and basic knowledge (detailed setup instructions are in the migration report):

- **Kubernetes Cluster**: A running Kubernetes cluster (e.g., Minikube, K3s, kubeadm, or EKS/AKS/GKE).
- **Core CLI Tools**:
  - `kubectl` for cluster interaction.
  - `helm` for package management.
  - `docker` for building container images.
- **Infrastructure Components** (Covered in the report):
  - **Argo CD** for GitOps-based continuous delivery.
  - **HashiCorp Vault** for centralized secret management.
  - **Cert-Manager** for managing TLS certificates.
  - **Nginx Ingress Controller** to route external traffic.
  - **Cloudflare Tunnel** to securely expose local services securely to the internet.
  - **SonarQube** for static code analysis.
  - **Self-hosted GitHub Runner** to execute CI/CD workflows inside the local network.
  - **Harbor** for private container image registry.

## Contributing

We welcome contributions to Coursey. Please submit a pull request with your changes.

## License

Coursey is licensed under the [MIT License](https://opensource.org/licenses/MIT).

