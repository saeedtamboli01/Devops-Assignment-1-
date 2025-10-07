# 🚀 DevOps Assignment

## 📦 Project Overview
This project demonstrates a complete CI/CD pipeline using GitHub Actions, Docker, and Kubernetes. The application is containerized, pushed to GitHub Container Registry (GHCR), and deployed to a local Kubernetes cluster via Docker Desktop.

## 🛠️ Tech Stack
- Node.js (or your app language)
- Docker
- GitHub Actions
- GitHub Container Registry (GHCR)
- Kubernetes (Docker Desktop)

## ⚙️ CI/CD Workflow
- On every push to `main`:
  - GitHub Actions builds the Docker image
  - Pushes it to GHCR:  
    `ghcr.io/saeedtamboli01/devops-assignment:latest`

## ☸️ Kubernetes Deployment
- `deployment.yaml` defines the app deployment
- `service.yaml` exposes the app via NodePort

## 🔐 Private Registry Access
- Kubernetes uses a secret (`ghcr-secret`) to pull the private image from GHCR

## 🌐 Accessing the App
After applying the YAML files:

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Access the app at:

             http://localhost:30212

✅ Status
✔️ CI/CD working

✔️ Image pushed to GHCR

✔️ Kubernetes deployment successful

✔️ App accessible via NodePort

📁 Files Included
Dockerfile

.github/workflows/docker.yml

deployment.yaml

service.yaml

README.md             