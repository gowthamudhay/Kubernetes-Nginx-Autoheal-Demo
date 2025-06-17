# 🚀 Kubernetes Nginx Auto-Heal Demo

This project shows how to use **Kubernetes** to deploy a simple web app (Nginx) with **auto-healing** using a `livenessProbe`.

## ✅ Features

- Deploy Nginx web server on Kubernetes
- Add liveness probe to auto-restart on crash
- Expose service via NodePort
- Health check script to monitor pods

## 🛠 Tools Used

- Minikube (local Kubernetes)
- kubectl
- YAML (for K8s manifests)
- Bash (for health check script)

## 📂 Files

| File                  | Description                         |
|-----------------------|-------------------------------------|
| `nginx-deployment.yaml` | Defines deployment & liveness probe |
| `service.yaml`         | Exposes app via NodePort            |
| `healthcheck.sh`       | Basic health script for monitoring  |

## 🔁 How to Simulate Crash

```bash
kubectl exec -it <pod-name> -- /bin/sh
kill 1
