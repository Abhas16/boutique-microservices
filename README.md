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
          +----------------+----------------+
          |                |                |
      Frontend          Gateway        Microservices
                                           |
                  +------------+------------+------------+
                  |            |            |            |
                 Auth       Products      Orders       Users
                                           |
                                           v
                                      PostgreSQL

                    Monitoring
                         |
              Prometheus + Grafana