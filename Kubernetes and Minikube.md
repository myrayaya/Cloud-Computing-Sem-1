# Kubernetes
- It is an open source container orchestration platform that automates many of the manual processes involved in deploying, managing, and scaling containerized applications.
- It was originally developed by Google and is now maintained by the Cloud Native Computing Foundation.

### Key Features of Kubernetes include:

- <b> Container Management: </b> Simplifies running and managing containers across clusters.
- <b> Scaling: </b> Automatically adjusts the number of active containers based on demand
- <b> Load Balancing: </b> Distributes traffic to ensure no single is overwhelmed
- <b> Self-Healing: </b> Automatically restarts failed containers and replaces or reschedules them as needed
- <b> Service Discovery: </b> Allows containers to communicate with each other and external services seamlessly.
- <b> Configuration Management: </b> Manages applications' configurations and secrets securely

## Kubernetes Cluster:
- A working Kubernetes deployment is called a cluster, which is a group of hosts running Linux containers. You can visualize a Kubernetes cluster as two parts: a) The control plane and b) The computer machines, or nodes
- Each node is its own Linux environment, and could be either a physical or virtual machine. Each node runs pods, which are made up of containers.

## Docker vs Kubernetes
- Docker can be used as a container runtime that Kubernetes orchestrates. When Kubernetes schedules a pod to a node, the kubelet (the service that makes sure each container is running) on that node will instruct Docker to launch the specified containers.
- The difference when using Kubernetes with Docker is that an automated system asks Docker to do those things instead of the admin doing so manually on all nodes for all containers.

## Minikube
- Minikube is a one-node Kubernetes cluster where master processes and work processes both run on one node.
- Minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.

## Pros of Minikube
- Ease of Installation and Setup
- Cost-Effective Learning Environment
- Fast Development Cycle
- Experimentation Without Risk
- Portable Environment

## Installation of Minikube
Step - 1: Open PuTTY
- Enter the Hostname or IP Address.
- Click Open.
- Login to the server by writing ubuntu.

Step - 2: Install docker using the following command
```
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```

Step - 3: Add your local user to docker group so that your local user run docker commands without sudo.
```
sudo usermod -aG docker $USER
```

Step - 4: Enter the following command
```
$ newgrp docker
```

Step - 5: Install the Kubernetes command-line tool, kubectl, via the Snap package management system
```
sudo snap install kubectl --classic
kubectl version --client
```

Step - 6: Download and install Minikube Binary
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

Step - 7: Verify Minikube version by this command
```
minkube version
```

Step - 8: Install Kubectl tool 
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

Step - 9: Start Minkube Cluster
```
minikube start --driver=docker
```

Step - 10: Verify the status of your cluster
```
minikube status
```

Step - 11: Grant permission with the following:
```
kubectl cluster-info
Kubectl config view
kubectl get nodes
kubectl get pods
```

Step - 12: Start the Kubernetes dashboard and run the command
```
minikube dashboard
```

Step - 13: Use the following url on the browser and use the public IP address
```
http://public_ip:8001/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/
```
