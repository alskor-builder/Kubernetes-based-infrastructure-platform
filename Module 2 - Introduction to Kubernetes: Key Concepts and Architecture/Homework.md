- **Objective**: Learn to deploy your own Kubernetes cluster using Minikube for practice and testing purposes.
- **Tasks**:
  - Deploy a Kubernetes cluster with two virtual nodes using Minikube.
  - Use kubectl to check the version of the cluster and client.
  - Practice with various kubectl commands. (The most curious can practice with various kubectl commands using a cheat sheet. https://kubernetes.io/docs/reference/kubectl/quick-reference/)


## Homework Objective

Pods are the fundamental building blocks of Kubernetes, and a significant portion of a DevOps engineer's work involves their deployment, update, and troubleshooting. Therefore, the objective of this homework is to consolidate knowledge about pods and practice basic operations with them: creation, update, and troubleshooting. This will lay the foundation for further learning, as nearly all other Kubernetes objects are related to pods.

## Tasks

**NB**: All tasks are to be performed in a Minikube cluster version 1.0.0 or higher.

### Task 1

1. Create a file named `pod.yaml` and copy the following manifest into it:

    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: my-nginx
    spec:
      containers:
          name: nginx-container
          image: nginx:1.10
    ```

2. Try to create a pod from this manifest using the command:

    ```bash
    kubectl create -f pod.yaml
    ```

3. `kubectl` cannot apply the YAML file. What is the error? Enter your answer in the homework submission form.

**Evaluation Criteria**
- The edited manifest should be applicable in the cluster without errors.

### Task 2

1. Launch a Redis pod in the cluster using the command:

    ```bash
    kubectl run redis --image=redis:5.0 -n default
    ```

2. Verify that Redis has started and is in the Running status using the command:

    ```bash
    kubectl get pods -n default
    ```

3. Ensure that the Docker image version is `redis:5.0` using the command:

    ```bash
    kubectl get pod redis -n default -o jsonpath="{..image}"
    ```

4. Edit the Redis pod using the command:

    ```bash
    kubectl edit pod redis -n default
    ```

   Change the Docker image version to `redis:6.0`.

   Note: You can change the default text editor used by the `kubectl edit` command with the environment variable `KUBE_EDITOR`, for example:

    ```bash
    export KUBE_EDITOR=nano
    ```

    or

    ```bash
    export KUBE_EDITOR=vim
    ```

5. Save the changes and check the container logs using the command:

    ```bash
    kubectl logs redis -n default
    ```

   Has the container version changed?

**Evaluation Criteria**
- The Redis version should be updated from 5.0 to 6.0.
