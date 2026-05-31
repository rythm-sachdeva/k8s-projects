# 🗂️ Monorepo

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![NodeJS](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

> A collection of full-stack applications, each self-contained with its own source code and Kubernetes configuration.

---

## 📁 Repository Structure

```
/
├── project-one/
│   ├── frontend/
│   ├── backend/
│   └── k8s/          ← Kubernetes configs for project-one
│
├── project-two/
│   ├── frontend/
│   ├── backend/
│   └── k8s/          ← Kubernetes configs for project-two
│
├── project-three/
│   ├── ...
│   └── k8s/          ← Kubernetes configs for project-three
│
└── README.md
```

> [!IMPORTANT]
> Each project is independent. For Kubernetes configuration of any project, **please refer to the `k8s/` directory within that project's folder.**

---

## ☸️ Kubernetes

Every project in this repo follows the same convention — all Kubernetes manifests (deployments, services, configmaps, etc.) are located inside the project's own `k8s/` folder.

```bash
# Deploy any project by navigating to its k8s folder
kubectl apply -f <project-name>/k8s/

# Example
kubectl apply -f project-one/k8s/
```

To verify everything is running after applying:

```bash
kubectl get pods
kubectl get svc
kubectl get deployments
```

---

## 🚀 Getting Started

### Prerequisites

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Minikube](https://img.shields.io/badge/Minikube-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![kubectl](https://img.shields.io/badge/kubectl-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

- [Docker](https://www.docker.com/)
- [Minikube](https://minikube.sigs.k8s.io/) (for local development)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

### Running a project locally with Minikube

```bash
# Start minikube
minikube start

# Navigate to the project and apply its k8s config
kubectl apply -f <project-name>/k8s/

# Access the frontend service
minikube service <service-name>
```

---

## 📌 Project Index

| Project | Description | K8s Config |
|---|---|---|
| `project-one` | _Short description_ | [`project-one/k8s/`](./project-one/k8s) |
| `project-two` | _Short description_ | [`project-two/k8s/`](./project-two/k8s) |
| `project-three` | _Short description_ | [`project-three/k8s/`](./project-three/k8s) |

> Add a row for each new project you introduce to this repo.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) |
| Backend | ![NodeJS](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) |
| Containerization | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) |
| Orchestration | ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) |

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