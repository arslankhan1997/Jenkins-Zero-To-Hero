# CI/CD Pipeline Setup

## Tools Used
- Jenkins (CI)
- SonarQube 9.9 LTS (Code Quality)
- Docker (Containerization)
- ArgoCD (CD)
- Kubernetes/Minikube (Orchestration)

## Architecture
Code Push → Jenkins → Maven Build → SonarQube Scan → Docker Build → Push to DockerHub → ArgoCD → Kubernetes

## Infrastructure
- EC2 Instance (Ubuntu 24) - Jenkins + SonarQube
- Minikube - Kubernetes cluster (local)
- DockerHub - Container registry (arslan690/ultimate-cicd)

## Jenkins Pipeline Stages
1. Checkout
2. Build and Test (Maven)
3. Static Code Analysis (SonarQube)
4. Build and Push Docker Image
5. Update Deployment File

## Key Fixes Applied
- SonarQube downgraded to 9.9 LTS for Java 11 compatibility
- Docker private IP used for SonarQube connectivity
- ArgoCD installed via standard manifests
```

5. Click **Commit changes**

---

## Your completed work is already on GitHub at:
```
https://github.com/arslankhan1997/Jenkins-Zero-To-Hero
