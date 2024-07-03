# Kubernetes Infrastructure Platform

Welcome to the Kubernetes Infrastructure Platform course by Me(aka alskor/). This repository contains practical exercises and assignments to help you master Kubernetes and its components.

## Course Overview

This course covers the following key topics:

### 1. Cluster Setup
- **Objective**: Learn to deploy your own Kubernetes cluster using Minikube for practice and testing purposes.
- **Tasks**:
  - Deploy a Kubernetes cluster with two virtual nodes using Minikube.
  - Use kubectl to check the version of the cluster and client.
  - Practice with various kubectl commands. (The most curious can practice with various kubectl commands using a cheat sheet. https://kubernetes.io/docs/reference/kubectl/quick-reference/)

### 2. Pods and Applications
- **Objective**: Understand and practice creating, updating, and troubleshooting pods, the basic building blocks of Kubernetes.
- **Tasks**:
  - Create and apply a pod manifest using YAML.
  - Launch a pod with Redis and update its Docker image version.
  - Perform basic operations with pods such as creation, update, and troubleshooting.

### 3. Deployments and Services
- **Objective**: Manage Kubernetes objects like Deployments, Services, and Jobs.
- **Tasks**:
  - Deploy a WordPress site with an init-container to ensure the database is available before starting the main container.
  - Create a CronJob that logs the current date and external IP address every minute.

### 4. Security and Policies
- **Objective**: Secure your Kubernetes cluster with RBAC (Role-Based Access Control) and Pod Security Policies.
- **Tasks**:
  - Create roles and role bindings to grant necessary permissions to service accounts.
  - Implement Pod Security Policies to restrict running containers as root.

### 5. Networking
- **Objective**: Learn to expose pods outside the cluster using NodePort and Ingress services, and restrict pod communication with Network Policies.
- **Tasks**:
  - Expose a PostgreSQL database using a NodePort service.
  - Configure an Ingress to expose a web service externally.
  - Apply Network Policies to restrict and allow specific traffic to and from pods.

### 6. Storage
- **Objective**: Connect persistent storage to pods using StorageClass and PersistentVolumeClaim, and see the benefits of StatefulSet for stateful applications.
- **Tasks**:
  - Create a StorageClass and PersistentVolumeClaim for a PostgreSQL database.
  - Use StatefulSet to manage stateful applications with persistent storage.

### 7. Helm and Kustomize
- **Objective**: Use Helm for managing Kubernetes packages and Kustomize for environment-specific configurations.
- **Tasks**:
  - Modify Helm templates to conditionally create resources.
  - Use Kustomize to generate environment-specific configurations for dev and prod environments.

### 8. Resource Management
- **Objective**: Set resource requests and limits for applications, and configure horizontal pod autoscaling based on CPU usage.
- **Tasks**:
  - Set resource requests and limits for a billing application to ensure it receives the necessary resources.
  - Configure LimitRange and ResourceQuota to control resource usage within a namespace.
  - Implement HorizontalPodAutoscaler to scale the application based on CPU utilization.

### 9. Monitoring and Logging
- **Objective**: Set up monitoring with Prometheus and Grafana, and log parsing with Loki.
- **Tasks**:
  - Configure Grafana dashboards to monitor cluster metrics.
  - Use Loki to parse and analyze logs from the Ingress controller.

### 10. Service Mesh
- **Objective**: Install and configure Istio for traffic management and service mesh functionalities.
- **Tasks**:
  - Create rules for traffic balancing using pod labels.
  - Use request headers for routing traffic to specific versions of a service.

### 11. CI/CD and Health Checks
- **Objective**: Integrate GitLab CI/CD pipelines and configure health checks for applications.
- **Tasks**:
  - Set up liveness and readiness probes to ensure application availability and performance.
  - Configure GitLab pipelines for continuous integration and delivery.


