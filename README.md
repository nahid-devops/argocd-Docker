# CI/CD Pipeline with GitHub, Docker, Kubernetes, and ArgoCD

This repository serves as a guide to understanding a complete CI/CD pipeline utilizing GitHub, Docker, Kubernetes, and ArgoCD. 
The pipeline consists of two main parts.

## Application Overview

The primary focus of this repository is to build a simple Python Flask application (`app.py`), 
create a Docker image, and automate the tagging and pushing of this image to Docker Hub.

## GitHub Actions

The `.github/workflows` folder contains GitHub Actions workflows that automate the Docker image build and push process using GitHub Actions default runners.

## Integration with ArgoCD

Upon a new commit in this repository, an automated process is triggered to clone repository. 
This process edits the image tag automatically and pushes the changes to the `argocd-k8s-deploy` repository.

## ArgoCD Deployment

ArgoCD continuously monitors the repository. Upon detecting a new commit, 
it initiates the deployment of a new container to the Kubernetes cluster.

This setup ensures seamless integration and automation throughout the CI/CD pipeline, facilitating efficient development and deployment processes.
