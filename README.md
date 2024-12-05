# Cosmocloud Helm Chart

This Helm chart deploys a backend, frontend, and Redis database application stack on Kubernetes.

## Prerequisites
- Kubernetes cluster
- Helm v3 or above

## Components
- Backend: Handles core application logic.
- Frontend: User interface.
- Redis: Caching layer.

## Installation
1. Navigate to the Helm chart directory:
    cd cosmocloud-deploy
2. Install the chart:
    helm install testapp . --atomic --timeout 30s
