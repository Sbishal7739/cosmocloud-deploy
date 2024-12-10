Cosmocloud Helm Chart
This repository contains the Helm chart cosmocloud-deploy, which deploys a complete application stack (frontend, backend, and Redis) in a Kubernetes cluster.
Folder Structure
cosmocloud-deploy/  
├── Chart.yaml          # Metadata for the Helm chart  
├── values.yaml         # Default values for the chart  
├── templates/          # Kubernetes manifests for resources  
└── charts/             # (Optional) Subcharts can be placed her
Application Components
Frontend

. Image: shreybatra/sample-frontend
. Exposed via NodePort on port 31000
. Environment variable: BACKEND_URL = http://backend-svc:8000 

Backend

. Image: shreybatra/sample-backend
. Exposed via ClusterIP on port 8000
. Environment variable: REDIS_URI = redis://redis-svc:6379

Redis

. Image: redis
. Exposed via ClusterIP on port 6379

Prerequisites
. A running Kubernetes cluster
. Helm installed

cd cosmocloud-deploy
helm install testapp cosmocloud-deploy --atomic --timeout 30s
kubectl get all

