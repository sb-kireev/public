Project Overview
The project consists of:

A Flask-based Python application (app/main.py) that connects to a PostgreSQL database.
PostgreSQL database initialized with a custom script (db/init.sql).
Nginx as a reverse proxy for the application.
Kubernetes manifests for deploying the application in a cluster.
CI/CD pipeline for automated builds and deployments.
Prerequisites
Before running the project, ensure you have the following installed:

Docker and Docker Compose
Kubernetes (Minikube or a cloud-based cluster)
kubectl CLI
Azure DevOps account (for CI/CD)

Local Setup with Docker Compose
Clone the repository:
    git clone https://github.com/yourusername/devops-task.git
    cd devops-task

Build and start the services using Docker Compose:
    chmod +x run.sh
    ./run.sh

Access the application:
Open your browser and navigate to http://localhost.
You should see the PostgreSQL version displayed.

Stop the services:
    docker-compose down

Kubernetes Deployment
Install Minikube (if not already installed):
    minikube start
    minikube addons enable ingress

Apply the Kubernetes manifests:
    chmod +x deploy.sh
    ./deploy.sh

Access the application:
Open your browser and navigate to http://app.local.

Clean up:
    kubectl delete -f k8s/