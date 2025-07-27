# 🧰 DevSecOps-In-A-Box

*A Lightweight, Containerized, Hands-on Learning Platform for Full Stack DevSecOps.*

---

## 🌟 Project Goal

To build a **portable Linux VM** that simulates the **full DevSecOps lifecycle** — from app development to CI/CD, security scanning, Kubernetes deployment, and monitoring.

Ideal for IT professionals, students, and cloud/security learners looking to get practical, end-to-end experience.

---

## 🧱 Architecture Overview

### 🔧 Base VM Setup

- OS: **Lubuntu** (desktop or server mode)
- Network: **VirtualBox Host-Only + NAT**
- Tools: Docker, Docker Compose, Minikube/K3s, Git, VS Code (optional)

### 🐳 Containerized App Stack

| Tier     | Container   | Description                    |
| -------- | ----------- | ------------------------------ |
| Frontend | React       | Simple note-taking UI          |
| Backend  | Python Flask| REST API (CRUD + Auth)         |
| Database | PostgreSQL  | Encrypted notes storage        |
| Tools    | Trivy, ZAP  | Security testing containers    |

➡️ Managed using `docker-compose` in local development.

---

### ☸️ Kubernetes (Minikube/K3s)

| Component   | Description                          |
| ----------- | ------------------------------------ |
| `frontend`  | React app + Service + Deployment     |
| `backend`   | Flask API + Service + Deployment     |
| `database`  | StatefulSet or Pod with PVC          |
| `tools`     | Falco, Prometheus, Grafana pods      |

➡️ Namespace: `simple-note`

---

### 🔁 CI/CD Pipeline

- GitHub Actions: Lint, Test, Build, Push Images, Deploy via `kubectl`
- Optional: Jenkins in Docker or Pod

---

## 🔐 DevSecOps Toolchain

| Tool           | Purpose                          |
| -------------- | -------------------------------- |
| OWASP ZAP      | Dynamic web app scanning         |
| Trivy          | Image vulnerability scanning     |
| Falco          | K8s runtime security alerts      |
| Prometheus     | Metrics scraping                 |
| Grafana        | Dashboards + Alerting            |
| Auditd         | Linux event auditing             |

---

## 🧪 Key Features

- User Auth (JWT + bcrypt)
- Notes CRUD API (via Flask)
- Input sanitization + rate limiting
- Encrypted secrets
- Monitoring dashboards
- Full security toolchain

---

## 📂 Project Structure

devsecops-in-a-box/
├── docker/
│ ├── frontend/
│ ├── backend/ # Flask app code + Dockerfile
│ ├── database/
│ └── tools/
├── kubernetes/
│ ├── *.yaml (deployments, services, PVC)
├── terraform/
│ └── local-k8s-config.tf
├── .github/
│ └── workflows/
│ └── deploy.yaml
├── README.md
└── SECURITY.md

yaml
Copy
Edit

---

## 🚀 Getting Started

> Setup instructions coming soon. Meanwhile, here’s what to expect:

1. Boot your Lubuntu VM (VirtualBox)
2. Clone this repo
3. Run the Docker Compose environment
4. Open your browser on host at `http://10.0.2.15:3000`
5. Start hacking, testing, deploying, and monitoring 💥

---

## 📚 Learning Outcomes

| Area         | Learnings                                |
| ------------ | ---------------------------------------- |
| Web Dev      | React, Flask, Auth, REST API, DB         |
| Docker       | Containerization + Compose Networking    |
| Kubernetes   | Deployments, Services, Volumes, Logs     |
| Security     | OWASP, runtime scanning, image security  |
| DevOps       | CI/CD pipelines, GitHub Actions          |
| IaC          | Terraform basics + Kubernetes objects    |
| Monitoring   | Prometheus, Grafana, Alerting            |

---

## 📌 License

MIT License — Feel free to use, fork, and contribute!

---

## 🙋‍♂️ Author

**Ajeesh Mathai**  
💼 Cloud Security & Infrastructure Engineer | Student | Cybersecurity | Hobbyists
🌐 [GitHub](https://amathew0.github.io/CyberSec/) | [LinkedIn](https://www.linkedin.com/in/ajeesh-mathai3)
