## This repo contains the scripts and small NodeJS app to demonstrate GitOps example using Jenkins, Argocd & Kustomize

In this example, we will be using a simple NodeJS app to demonstrate the GitOps workflow. The app is a simple NodeJS app that returns the simple hello world. The app is deployed in a Kubernetes cluster and the deployment is managed by ArgoCD. The ArgoCD deployment is managed by Jenkins. The Jenkins pipeline is triggered by a commit to the GitOps repo. The GitOps repo contains the Kubernetes manifests and the Kustomize files to deploy the app.

### Kustomize

This directory contains the Kustomize files to deploy the app. The Kustomize files are used by ArgoCD to deploy the app. This directory is automatically updated by the Jenkins pipeline which we use in <a href="https://github.com/dinushchathurya/gitops-demo-deployment">this repository</a>.

