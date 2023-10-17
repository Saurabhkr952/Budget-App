
# Application Deployment with Kubernetes

This repository includes Kubernetes manifest files and instructions for deploying a Ruby on Rails application in Kubernetes. Below are the key components and steps involved in the deployment process.

## Manifest Files

### 1. app.yaml

- **Purpose:** This file defines the deployment and service for the Ruby on Rails application.
- **Usage:** Apply this configuration to deploy and expose your application.

### 2. database.yaml

- **Purpose:** Contains configuration for StatefulSets and Persistent Volume Claims (PVC) related to the database.
- **Usage:** Apply this configuration to set up the database for your application.

### 3. secrets

- **Purpose:** This directory holds sensitive information such as PostgreSQL secrets, database username and password, and the Rails master key.
- **Usage:** Securely manage these secrets to ensure the security of your application.

### 4. configmap

- **Purpose:** Defines environment variables, including the production environment and the database host.
- **Usage:** Configure your application's environment with these settings.

### 5. ingress

- **Purpose:** Provides ingress configuration to allow external access to your application.
- **Usage:** Access application securely with url `budget-app.com`(needs to be added in hosts file)

### Setup nginx ingress controller
Set up this nginx ingress controller to enable access to your deployed application.

## Additional Instructions

### Database Initialization Instructions
- manually need to run the command "rails:prepare" inside application-pod

### Minikube Ingress Controller

Make sure you have Ingress Nginx Controller enabled for Minikube to access the application via url: budget-app.com(also need to add budget-app.com in hosts file)

```shell
minikube addons enable ingress
```




