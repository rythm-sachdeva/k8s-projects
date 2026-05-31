# 🚀 Project Name

> A full-stack web application built with **React** and **Node.js**, containerized and orchestrated with Kubernetes.

---

## 📁 Project Structure

```
├── frontend/          # React application
├── backend/           # Node.js API server
├── k8s/               # ← Kubernetes configurations (see below)
└── README.md
```

> [!IMPORTANT]
> For Kubernetes configuration of **every directory**, please refer to the [`k8s/`](./k8s) folder.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React |
| Backend | Node.js |
| Containerization | Docker |
| Orchestration | Kubernetes |

---

## 📦 Kubernetes Configuration

All Kubernetes manifests live in the [`k8s/`](./k8s) folder. This includes services, deployments, and any other configuration needed to run the app in a cluster.

```
k8s/
├── frontend-deployment.yaml
├── frontend-service.yaml
├── backend-deployment.yaml
└── backend-service.yaml
```

### Running with Kubernetes (Minikube)

```bash
# Start minikube
minikube start

# Apply all manifests
kubectl apply -f k8s/

# Verify pods are running
kubectl get pods

# Access the frontend service
minikube service frontend
```

---

## 🧑‍💻 Local Development

### Prerequisites

- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [Minikube](https://minikube.sigs.k8s.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

### Frontend

```bash
cd frontend
npm install
npm start
```

### Backend

```bash
cd backend
npm install
npm run dev
```

---

## 🐳 Docker

Each service has its own `Dockerfile`. Build and run them individually:

```bash
# Build frontend
docker build -t frontend ./frontend

# Build backend
docker build -t backend ./backend
```

---

## ☸️ Deploying to Kubernetes

> For all Kubernetes configuration, refer to the [`k8s/`](./k8s) folder.

```bash
# Apply all configs at once
kubectl apply -f k8s/

# Check services
kubectl get svc

# Check deployments
kubectl get deployments

# View logs for a service
kubectl logs -l app=backend
kubectl logs -l app=frontend
```

---

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License.