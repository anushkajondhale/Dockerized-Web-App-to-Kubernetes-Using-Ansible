🚀 Dockerized Web App Deployment with Ansible & Kubernetes
Overview:
A fully automated DevOps pipeline that builds a Python Flask web app, containerizes it with Docker, pushes it to Docker Hub, and deploys it to a Minikube Kubernetes cluster — all using Ansible.

Tech Stack:
1.Frontend: HTML, CSS
2.Backend: Python Flask
3.Containerization: Docker
4.Orchestration: Kubernetes (Minikube)
5.Automation: Ansible

Workflow:
1.Flask app serves pod IP and public IP via /api/info.
2.Dockerfile builds the app image and exposes port 80.
3.Kubernetes manifests define a Deployment and NodePort Service.
4.Ansible playbook:
a.Logs in to Docker Hub
b.Builds & pushes Docker image
c.Applies Kubernetes manifests

Run Steps:
Copy
Edit
minikube start
ansible-playbook playbook.yml
minikube service webapp-service --url

Key Learnings:
Ansible streamlines Docker + Kubernetes workflows.
Minikube is ideal for local testing.
Testing manually before automation improves reliability.
