# Kubernetes & CI/CD Pipeline Automation (Experiment 8)

This repository contains the declarative Kubernetes manifest, Dockerfile, and GitHub Actions CI/CD pipeline for **Experiment 8: Deploying Applications, CI/CD Pipeline, and Cluster Monitoring**.

## 🚀 Repository Contents
- `.github/workflows/ci-cd.yml` - Automated CI/CD pipeline triggered on pushes to `main`.
- `deployment.yaml` - Kubernetes declarative deployment manifest for `sample-web-app` (replicas, resource requests & limits).
- `Dockerfile` - Container build definition based on `nginx:alpine`.
- `index.html` - Static web application deployed across the cluster.

---

## 🔐 Required GitHub Secrets
Before pushing, ensure the following repository secrets are configured under **Settings > Secrets and variables > Actions**:
1. `DOCKERHUB_USERNAME`: Your Docker Hub username.
2. `DOCKERHUB_TOKEN`: Your Docker Hub Personal Access Token.

---

## 🛠️ Kubernetes Commands
```bash
# Apply the deployment manifest
kubectl apply -f deployment.yaml

# Verify deployments and running pods
kubectl get deployments
kubectl get pods -l app=web

# Scale up replicas
kubectl scale deployment sample-web-app --replicas=5
```
