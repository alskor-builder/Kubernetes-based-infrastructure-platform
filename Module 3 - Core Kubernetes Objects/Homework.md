Pods and Applications
- **Objective**: Understand and practice creating, updating, and troubleshooting pods, the basic building blocks of Kubernetes.
- **Tasks**:
  - Create and apply a pod manifest using YAML.
  - Launch a pod with Redis and update its Docker image version.
  - Perform basic operations with pods such as creation, update, and troubleshooting.

## Homework Objective

In this module, we covered the basic Kubernetes objects for creating and managing pods. The objective of this homework is to consolidate knowledge about Kubernetes objects such as Deployments, Services, and Jobs, and to practice managing and troubleshooting them. This will lay the foundation for further learning, as more advanced Kubernetes entities and features are usually based on or depend on the objects discussed in this module.

## Tasks

### Task 1

**Objective**: Your company is launching a new WordPress site. You want to deploy the database separately and run three replicas of the site. However, the WordPress site containers should only start after the database is available. To achieve this, you plan to use an init-container in the WordPress pod that should run before the main container and check that the database is accessible. You have written all the manifests, but the main container does not start after the init-container. What is the issue?

**Steps to complete**:
1. Navigate to GitLab via the provided button.
2. Create deployment and service objects for the database in the cluster by applying the `database-deployment.yaml` and `database-service.yaml` manifests from the `module-3/Homework/task1` directory:

    ```
    devops.kubernetes
    ├── logo.png
    ├── module-2
    │   ├── Homework
    │   │   ├── task1
    │   │   │   ├── database-deployment.yaml
    │   │   │   ├── database-service.yaml
    │   │   │   └── webapp.yaml
    ```

3. Launch the webapp by applying the `webapp.yaml` manifest from the same directory in the cluster.
4. The webapp deployment pods cannot proceed past the init-containers. Identify the error in the manifests and fix the application.
    - **Hint**: The command `kubectl logs deployment/webapp -c check-db-ready` will show you the logs of the init-container from the webapp deployment.

**Evaluation Criteria**:
- The webapp init-container successfully completes, and the main application starts.

**Submission Instructions**:
- Write a text description through the homework submission form explaining what needs to be fixed and how to make the application work in its current state.

### Task 2

**Objective**: Create a CronJob that writes the current date and external IP address to the log every minute.
- **Hint**: To find the external address, you can use the command `curl ipinfo.io/ip`.

**Evaluation Criteria**:
- The CronJob runs every minute, and the logs contain the current date and external IP address.
