# GreenCity Infrastructure Repository

![](https://img.shields.io/github/license/PTarasyuk/greencityinfra)
![](https://img.shields.io/github/commit-activity/w/PTarasyuk/greencityinfra)
![](https://img.shields.io/github/last-commit/PTarasyuk/greencityinfra)
![](https://img.shields.io/github/repo-size/PTarasyuk/greencityinfra)

![Docker Badge](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=fff&style=for-the-badge)
![Kubernetes Badge](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=fff&style=for-the-badge)
![Terraform Badge](https://img.shields.io/badge/Terraform-844FBA?logo=terraform&logoColor=fff&style=for-the-badge)
![OpenTofu Badge](https://img.shields.io/badge/OpenTofu-FFDA18?logo=opentofu&logoColor=000&style=for-the-badge)
![Amazon EKS Badge](https://img.shields.io/badge/Amazon%20EKS-F90?logo=amazoneks&logoColor=fff&style=for-the-badge)
![Amazon RDS Badge](https://img.shields.io/badge/Amazon%20RDS-527FFF?logo=amazonrds&logoColor=fff&style=for-the-badge)

This repository contains the infrastructure configuration for the [GreenCity Project](https://github.com/ita-social-projects/GreenCity).

## Repository structure

It is designed for local development using Docker Compose and deployment to Kubernetes ([minikube](https://minikube.sigs.k8s.io/)).
The structure allows for a smooth transition to Helm charts in the future.

```text
.
├─ docker-compose.yml        # Docker Compose for local development
├─ envs/                     # Environment variables for services
│  ├─ example/               # Example environment variables
│  │  ├─ .db.env.example     # Database
│  │  ├─ .core.env.example   # Core service
│  │  └─ .user.env.example   # User service
│  └─ dev/                   # Development environment variables
│     ├─ .core.env           # Core service (NOT in Git!)
│     ├─ .gitkeep            # Git keep
│     ├─ .db.env             # Database (NOT in Git!)
│     └─ .user.env           # User service (NOT in Git!)
├─ k8s/                      # K8s manifests (plain YAML)
└─ README.md
```

## Prerequisites

- [Docker](https://www.docker.com/)
- [Kubectl](https://kubernetes.io/docs/reference/kubectl/)
- [Minikube](https://minikube.sigs.k8s.io/)
- [Kustomize](https://kustomize.io/)

## Development

### Docker Compose

...

### Minikube

#### Plain Manifests

For information on deploying Kubernetes via simple manifests, see [k8s/README.md](k8s/README.md)

## Architecture Decision Records (ADR)

For insights into the architectural decisions behind this project, refer to the [ADR Documentation](./docs/ADR/index.md).
