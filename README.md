# 🏦 Banking Platform on Kubernetes

A production-style three-tier banking application deployed on Kubernetes from scratch.

## 🏗️ Architecture
Internet → NGINX Ingress → Dashboard (nginx)
                        → Banking API (Node.js) → PostgreSQL

## 🛠️ Tech Stack
- API: Node.js + Express
- Dashboard: nginx + HTML
- Database: PostgreSQL 15
- Orchestration: Kubernetes (Minikube)
- Networking: Calico CNI

## 📦 Kubernetes Objects Used
- Namespace, ConfigMap, Secret
- StatefulSet + PVC (persistent storage)
- Deployments, Services, Ingress
- HPA (auto-scaling on CPU 60%)
- VPA, Node Affinity, Taints & Tolerations
- RBAC, NetworkPolicy (7 rules)
- DaemonSet (Fluentd logging)

## 🚀 Project Phases
- Phase 1 — It Works
- Phase 2 — It Is Secure
- Phase 3 — It Scales
- Phase 4 — It Survives

## 🔒 Security Features
- Non-root containers
- NetworkPolicy deny-all
- RBAC least-privilege
- Secrets for sensitive data

## 📈 Key Features
- Auto-scaling (HPA min:2 max:10)
- Data persistence after pod deletion
- Zero-downtime rolling updates & rollback
- Log collection on every node
