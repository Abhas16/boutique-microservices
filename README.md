# Cloud-Native Boutique Microservices Platform on AWS

## Overview

A cloud-native e-commerce microservices platform deployed on Amazon EKS using Docker, Kubernetes, Terraform, Amazon ECR, Argo CD, PostgreSQL, Prometheus, and Grafana.

The project demonstrates infrastructure provisioning, containerized microservices deployment, GitOps-based continuous delivery, Kubernetes orchestration, and application monitoring.

## Architecture

```text
                         GitHub
                            |
                            v
                    Argo CD / GitOps
                            |
                            v
                     Amazon EKS Cluster
                            |
             +--------------+--------------+
             |              |              |
          Frontend       Gateway      Microservices
                                           |
                    +----------+-----------+----------+
                    |          |           |          |
                   Auth     Products      Orders     Users
                                           |
                                           v
                                      PostgreSQL
                                           |
                                           v
                                      Monitoring
                                           |
                                  Prometheus + Grafana

## Tech Stack

### Cloud & Infrastructure
- AWS
- Amazon VPC
- Amazon EKS
- Amazon ECR
- IAM
- Terraform

### Containers & Orchestration
- Docker
- Kubernetes
- Helm
- kubectl

### GitOps & CI/CD
- GitHub
- Argo CD
- GitOps

### Monitoring
- Prometheus
- Grafana

### Application
- React
- Node.js
- PostgreSQL

## Key DevOps Implementation

- Provisioned AWS infrastructure using Terraform.
- Provisioned an Amazon EKS cluster and managed worker nodes.
- Created Amazon ECR repositories for containerized microservices.
- Containerized frontend and backend services using Docker.
- Deployed frontend and backend microservices on Kubernetes.
- Implemented GitOps-based continuous delivery using Argo CD.
- Configured Argo CD to synchronize Kubernetes manifests from GitHub.
- Deployed PostgreSQL for application data persistence.
- Configured Prometheus for Kubernetes and application monitoring.
- Created Grafana dashboards for Kubernetes and application observability.

## Deployment Flow

```text
Developer
    |
    v
GitHub Repository
    |
    v
Argo CD / GitOps
    |
    v
Amazon EKS
    |
    +--> Frontend
    +--> Gateway
    +--> Auth
    +--> Product Service
    +--> Order Service
    +--> Orders
    +--> User Service
    +--> PostgreSQL
    |
    v
Prometheus
    |
    v
Grafana

## Project Structure

```text
boutique-microservices/
│
├── backend/
│   └── services/
│       ├── auth/
│       ├── gateway/
│       ├── order-service/
│       ├── orders/
│       ├── product-service/
│       └── user-service/
│
├── frontend/
│
├── gitops/
│   ├── k8s/
│   ├── argo-cd.yml
│   └── kustomization.yml
│
├── infrastructure/
│   ├── modules/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── screenshots/
│
└── README.md


---

# Step 10 — Add DevOps Workflow

Then:

```markdown
## DevOps Workflow

1. Application and infrastructure code are maintained in GitHub.
2. Docker images are built for the application services.
3. Container images are stored in Amazon ECR.
4. Terraform provisions the AWS infrastructure.
5. Kubernetes manifests define the application workloads.
6. Argo CD monitors the Git repository and synchronizes the desired state to Amazon EKS.
7. Prometheus collects Kubernetes and application metrics.
8. Grafana provides dashboards for observability.

## Key Learning Outcomes

- AWS infrastructure provisioning with Terraform
- Amazon EKS and Kubernetes workload management
- Docker containerization
- Amazon ECR image management
- GitOps deployment using Argo CD
- Kubernetes networking and service discovery
- PostgreSQL deployment on Kubernetes
- Monitoring with Prometheus and Grafana
- Infrastructure as Code
- Cloud-native microservices architecture