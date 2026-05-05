# Todo List App - Azure DevOps CI/CD with AKS

A full-stack Todo List application deployed to Azure Kubernetes Service (AKS) using Azure DevOps CI/CD pipelines.

## Tech Stack
- **Frontend:** React + Nginx
- **Backend:** Node.js + Express
- **Database:** MongoDB
- **Container Registry:** Azure Container Registry (ACR)
- **Orchestration:** Azure Kubernetes Service (AKS)
- **CI/CD:** Azure DevOps Pipelines

## Project Structure
```
todo-list-app/
├── backend/              # Node.js Express API
├── frontend/             # React app with Nginx
├── k8s/                  # Kubernetes manifests
├── azure-pipelines.yml   # CI/CD pipeline definition
└── README.md
```

## Setup Steps

### 1. Push this repo to GitHub
### 2. Create Azure resources via Azure Portal:
   - Resource Group
   - Azure Container Registry (ACR)
   - Azure Kubernetes Service (AKS) - attach ACR
### 3. Configure Azure DevOps:
   - Create project
   - Create service connections (GitHub, ACR, AKS)
   - Update `azure-pipelines.yml` with your ACR name
   - Create pipeline from existing YAML
### 4. Run pipeline & approve deployment

## Access the App
After deployment, get the LoadBalancer IP from AKS:
```
kubectl get svc frontend-service
```

Open the EXTERNAL-IP in your browser.

## License
MIT
