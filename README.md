# GitOps Manifests & ArgoCD

This repository contains the Kubernetes manifests and ArgoCD configurations used to deploy the React application.

### How it works
1. **Source of Truth**: This repository holds the desired state of the application in the Kubernetes cluster.
2. **Automated Image Updates**: Whenever the CI pipeline in the app repository builds a new image, Jenkins automatically commits the new image tag into `environments/dev/deployment.yaml`.
3. **ArgoCD Sync**: ArgoCD continuously monitors this repo for changes and automatically syncs the new deployment to the Kubernetes cluster.



