# CI-CD-Project

# CI/CD Pipeline for Cafe App Deployment

This repository contains the source code and configuration files for setting up a CI/CD pipeline to deploy the Cafe App using Kubernetes.

## Overview

The CI/CD pipeline automates the deployment process for the Cafe App:

- **GitHub Repository**: Stores the source code of the Cafe App and CI/CD configuration files.
- **Jenkins Server**: Manages the CI/CD workflow and triggers deployments.
- **Docker Hub**: Hosts Docker images of the Cafe App.
- **Kubernetes Cluster**: Orchestrates the deployment of the Cafe App containers.
- **Ansible**: Configures and manages the infrastructure components required for deployment.

## Components

### Cafe App

The Cafe App is a sample application that simulates a cafe management system. It provides features for managing orders, menus, and customer data.

### CI/CD Workflow

1. **Code Commit**: Push changes to the GitHub repository.
2. **Jenkins Pipeline**: Jenkins monitors the repository for changes. Upon detecting new commits, Jenkins triggers a build process.
3. **Build**: Jenkins pulls the source code, builds a Docker image, and pushes it to Docker Hub.
4. **Deployment**: Jenkins applies the updated deployment configuration to the Kubernetes cluster, triggering a rolling update of the Cafe App.

## Configuration Files

- `cafe-app-deploy.yml`: Kubernetes Deployment configuration file for the Cafe App.
- `cafe-app-service.yml`: Kubernetes Service configuration file for exposing the Cafe App.
- `ansi-kube-deploy.yml`: Ansible playbook automates the deployment of the Cafe App on a Kubernetes cluster. It consists of tasks that execute commands to deploy the Cafe App and manage its lifecycle.
- `create-img-cafe-app.yml`: Ansible playbook automates the process of building a Docker image for the Cafe App, tagging it, and pushing it to Docker Hub.

## Usage

To set up this CI/CD pipeline for the Cafe App:

1. Fork this repository to my GitHub account.
2. Configure Jenkins to monitor my forked repository for changes.
3. Set up Docker Hub integration for automated image builds.
4. Configure Kubernetes access on Jenkins for deployment.
5. Run the Ansible playbook to configure the necessary infrastructure components.

## Prerequisites

- Jenkins installed and configured with necessary plugins.
- Docker installed on the Jenkins server.
- Access to a Kubernetes cluster for deployment.
- Docker Hub account for image hosting.
- Ansible installed on the deployment server.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

