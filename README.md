# 🛠️ Full DevOps CI/CD Pipeline — Jenkins + Ansible + Docker + Kubernetes on EC2

This project demonstrates a complete DevOps CI/CD workflow built from scratch without using Docker Hub or any prebuilt images. It deploys a simple Flask web application inside a Kubernetes cluster (Minikube) running on an AWS EC2 instance.

---

## 🔧 Tech Stack

- **Jenkins**: CI/CD Automation Tool
- **Ansible**: Configuration Management
- **Docker**: Containerization
- **Kubernetes (Minikube)**: Container Orchestration
- **AWS EC2**: Cloud Infrastructure (Ubuntu/CentOS)

---

## 📁 Project Structure

```bash
devops-cicd-pipeline/
├── jenkins/                 # Jenkinsfile and setup
│   └── Jenkinsfile
├── ansible/                 # Ansible Playbooks
│   ├── deploy_k8s.yml
├── k8s/                     # Kubernetes manifests
│   ├── flask-deployment.yml
│   └── flask-service.yml
├── flask-app/              # Flask App Code
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
└── README.md
``` 

🚀 Pipeline Workflow
👨‍💻 Code Push (app.py, Dockerfile, etc.)

🔧 Jenkins triggers build

⚙️ Jenkins executes Ansible playbooks:

- Installs Docker (if not present)

- Builds Docker image locally on EC2

- Deploys app to Kubernetes using Minikube

🧱 Kubernetes creates Pod + Service

🌐 Access app via EC2 IP + NodePort

🧪 How to Run
1️⃣ Prerequisites
- AWS EC2 instance (Ubuntu/CentOS)

- Minikube installed

- Jenkins installed and running

- Ansible installed

- Python 3 installed

- Docker installed

✅ Accessing the App
Once the deployment is done, access your app using:
http://minikube-ip:30036

📎 GitHub Repo
🔗 https://github.com/kunal1601/Jenkins-CI-CD--Ansible-Kubernetes.git


