# 🗳️ Kubernetes Voting App

This is a sample microservices-based voting application deployed on Kubernetes. It demonstrates how to orchestrate a multi-tier application using containers and Kubernetes.

---

## 🧱 Application Components

The app consists of five microservices, each running in its own container:

1. **Vote** – A Python Flask web app for voting between two options (e.g., Cats or Dogs).
2. **Redis** – An in-memory data structure store used as a message queue.
3. **Worker** – A Python background service that moves votes from Redis to PostgreSQL.
4. **PostgreSQL** – A relational database to persist the votes.
5. **Result** – A web app (Node.js or Flask) that displays real-time vote results.

---

## 🚀 Prerequisites

Make sure you have the following installed:

- [Docker](https://www.docker.com/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- A Kubernetes cluster (e.g., [Minikube](https://minikube.sigs.k8s.io/), Kind, GKE, EKS)

---

## 📦 How to Deploy and Use the App

### 📁 step 1: Clone the Repository and Access the App 

```bash
git clone https://github.com/example/k8s-voting-app.git
cd k8s-voting-app
```

### 📁 step 2: Starting minikube service and accessing the application through url
```bash
minikube start
minikube service voting-app-service
minikube service result-app-service
```




