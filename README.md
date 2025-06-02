# 🚀 Flask K8s App

A simple Flask web application deployed on a local Kubernetes cluster using Minikube.

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [System Requirements](#system-requirements)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Docker Instructions](#docker-instructions)
- [Kubernetes Deployment](#kubernetes-deployment)
- [Project Structure](#project-structure)
- [License](#license)

---

## 📌 Project Overview

This project demonstrates how to:

- Build a Flask app.
- Containerize it with Docker.
- Deploy it to a local Kubernetes cluster using Minikube.

---

## 🧰 System Requirements

Ensure the following are installed:

- Python 3.x
- Flask
- Docker
- Minikube
- kubectl
- Git

### ✅ System Architecture Check

To confirm you're using a compatible CPU architecture (e.g., Intel-based Mac):

```bash
uname -m
Expected Output:

bash
Copy
Edit
x86_64
🏁 Getting Started
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/flask-k8s-app.git
cd flask-k8s-app
2. Set Up Virtual Environment
bash
Copy
Edit
python3 -m venv venv
source venv/bin/activate
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
🐳 Docker Instructions
Build the Docker Image
bash
Copy
Edit
docker build -t flask-k8s-app .
Run Locally with Docker
bash
Copy
Edit
docker run -p 5000:5000 flask-k8s-app
Visit: http://localhost:5000

☸️ Kubernetes Deployment
1. Start Minikube
bash
Copy
Edit
minikube start
2. Use Minikube's Docker Daemon (optional, for rebuilding image)
bash
Copy
Edit
eval $(minikube docker-env)
docker build -t flask-k8s-app .
3. Apply Kubernetes Configs
bash
Copy
Edit
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
4. Access the App via Minikube Service
bash
Copy
Edit
minikube service flask-k8s-app-service
📁 Project Structure
Copy
Edit
flask-k8s-app/
├── app.py
├── Dockerfile
├── requirements.txt
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
└── README.md
📝 License
This project is licensed under the MIT License.

🙋‍♂️ Author
Chimaobi Iberi
GitHub: @your-username