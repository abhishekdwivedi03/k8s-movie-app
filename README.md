# 🎬 KubeFlix – Scalable Movie App on Kubernetes

> A demo project that showcases a full-stack movie app (UI + API + DB) deployed on Kubernetes using Terraform, Helm, and GitHub Actions.

## 🔧 Tech Stack

- **Frontend**: Nginx Static Site (public Docker image)
- **Backend**: Echo Server (mock API)
- **Database**: MongoDB
- **Orchestration**: Kubernetes (Minikube or EKS)
- **IaC**: Terraform
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus + Grafana (optional)

## 🚀 Architecture

```
[Frontend] --> [movie-ui-service] --> [movie-ui Pod]
               |
               V
[Backend] --> [movie-api-service] --> [movie-api Pods]
               |
               V
[Database] --> [movie-db-service] --> MongoDB Pod + PVC
```

## 📦 Deploy Locally (Minikube)

```bash
kubectl apply -f k8s-manifests/
kubectl get all -n kubeflix
minikube service movie-ui-service -n kubeflix
```

## 📊 Observability

- Prometheus/Grafana manifests provided in `monitoring/` directory.
- Metrics include pod CPU/memory, request latency, and DB stats.

## 🛠️ Future Enhancements

- Replace echo-server with real Flask/Node backend
- Add secrets manager integration
- Add liveness/readiness probes

## 🙋‍♂️ Author

**Abhishek Dwivedi**  
DevOps/Cloud Engineer — [LinkedIn](https://www.linkedin.com/in/abhishek-dwivedi-290a58119/)
