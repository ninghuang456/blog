---
layout: post
title: Kubernetes Interview Questions and Answers
categories: Cloud
description: Kubernetes Interview Questions and Answers
keywords: cloud, k8s, Kubernetes
---
## 1. What is Kubernetes?
This is one of the most basic Kubernetes interview questions yet one of the most important ones! Kubernetes is an open-source container orchestration 
tool or system that is used to automate tasks such as the management, monitoring, 
scaling, and deployment of containerized applications. It is used to easily manage several containers 
(since it can handle grouping of containers), which provides for logical units that can be discovered and managed.

## 2. Why you need Kubernetes and what it can do 
Containers are a good way to bundle and run your applications. In a production environment, you need to manage the containers that run the applications and ensure that there is no downtime. For example, if a container goes down, another container needs to start. Wouldn't it be easier if this behavior was handled by a system?

That's how Kubernetes comes to the rescue! Kubernetes provides you with a framework to run distributed systems resiliently. It takes care of scaling and failover for your application, provides deployment patterns, and more. For example, Kubernetes can easily manage a canary deployment for your system.

Kubernetes provides you with:

### Service discovery and load balancing 
Kubernetes can expose a container using the DNS name or using their own IP address. If traffic to a container is high, Kubernetes is able to load balance and distribute the network traffic so that the deployment is stable.
### Storage orchestration 
Kubernetes allows you to automatically mount a storage system of your choice, such as local storages, public cloud providers, and more.
### Automated rollouts and rollbacks 
You can describe the desired state for your deployed containers using Kubernetes, and it can change the actual state to the desired state at a controlled rate. For example, you can automate Kubernetes to create new containers for your deployment, remove existing containers and adopt all their resources to the new container.
### Automatic bin packing 
You provide Kubernetes with a cluster of nodes that it can use to run containerized tasks. You tell Kubernetes how much CPU and memory (RAM) each container needs. Kubernetes can fit containers onto your nodes to make the best use of your resources.
Self-healing Kubernetes restarts containers that fail, replaces containers, kills containers that don't respond to your user-defined health check, and doesn't advertise them to clients until they are ready to serve.
### Secret and configuration management 
Kubernetes lets you store and manage sensitive information, such as passwords, OAuth tokens, and SSH keys. You can deploy and update secrets and application configuration without rebuilding your container images, and without exposing secrets in your stack configuration.

## 3. What is orchestration when it comes to software and DevOps? 
Orchestration refers to the integration of multiple services that allows them to automate processes or synchronize information in a timely fashion. Say, for example, you have six or seven microservices for an application to run. If you place them in separate containers, this would inevitably create obstacles for communication. Orchestration would help in such a situation by enabling all services in individual containers to work seamlessly to accomplish a single goal. 

## 4. How are Kubernetes and Docker related?
This is one of the most frequently asked Kubernetes interview questions, where the interviewer might as well ask you to share your experience working with any of them. Docker is an open-source platform used to handle software development. Its main benefit is that it packages the settings and dependencies that the software/application needs to run into a container, which allows for portability and several other advantages. Kubernetes allows for the manual linking and orchestration of several containers, running on multiple hosts that have been created using Docker. 

## 5. What are the main differences between the Docker Swarm and Kubernetes?
Docker Swarm is Docker’s native, open-source container orchestration platform that is used to cluster and schedule Docker containers. Swarm differs from Kubernetes in the following ways:

Docker Swarm is more convenient to set up but doesn’t have a robust cluster, while Kubernetes is more complicated to set up but the benefit of having the assurance of a robust cluster
Docker Swarm can’t do auto-scaling (as can Kubernetes); however, Docker scaling is five times faster than Kubernetes 
Docker Swarm doesn’t have a GUI; Kubernetes has a GUI in the form of a dashboard 
Docker Swarm does automatic load balancing of traffic between containers in a cluster, while Kubernetes requires manual intervention for load balancing such traffic  
Docker requires third-party tools like ELK stack for logging and monitoring, while Kubernetes has integrated tools for the same 
Docker Swarm can share storage volumes with any container easily, while Kubernetes can only share storage volumes with containers in the same pod
Docker can deploy rolling updates but can’t deploy automatic rollbacks; Kubernetes can deploy rolling updates as well as automatic rollbacks

## 6. What is the difference between deploying applications on hosts and containers?
Deploying Applications consist of an architecture that has an operating system. The operating system will have a kernel that holds various libraries installed on the operating system needed for an application.

Whereas container host refers to the system that runs the containerized processes. This kind is isolated from the other applications; therefore, the applications must have the necessary libraries. The binaries are separated from the rest of the system and cannot infringe any other application.

## 7. What are the features of Kubernetes?
Kubernetes places control for the user where the server will host the container. It will control how to launch. So, Kubernetes automates various manual processes. 
Kubernetes manages various clusters at the same time. 
It provides various additional services like management of containers, security, networking, and storage. 
Kubernetes self-monitors the health of nodes and containers. 
With Kubernetes, users can scale resources not only vertically but also horizontally that too easily and quickly.
## 8. What are the main components of Kubernetes architecture?
There are two primary components of Kubernetes Architecture: the master node and the worker node. Each of these components has individual components in them.

## 9. Explain the working of the master node in Kubernetes?
The master node dignifies the node that controls and manages the set of worker nodes. This kind resembles a cluster in Kubernetes. The nodes are responsible for the cluster management and the API used to configure and manage the resources within the collection. The master nodes of Kubernetes can run with Kubernetes itself, the asset of dedicated pods.

## 10. What is the role of Kube-apiserver?
This kind validates and provides configuration data for the API objects. It includes pods, services, replication controllers. Also, it provides REST operations and also the frontend of the cluster. This frontend cluster state is shared through which all other component interacts.

## 11. What is a node in Kubernetes?
A node is the smallest fundamental unit of computing hardware. It represents a single machine in a cluster, which could be a physical machine in a data center or a virtual machine from a cloud provider. Each machine can substitute any other machine in a Kubernetes cluster. The master in Kubernetes controls the nodes that have containers. 

## 12. What does the node status contain?
The main components of a node status are Address, Condition, Capacity, and Info.

## 13. What process runs on Kubernetes Master Node? 
The Kube-api server process runs on the master node and serves to scale the deployment of more instances.

## 14. What is a pod in Kubernetes?
In this Kubernetes interview question, try giving a thorough answer instead of a one-liner. Pods are high-level structures that wrap one or more containers. This is because containers are not run directly in Kubernetes. Containers in the same pod share a local network and the same resources, allowing them to easily communicate with other containers in the same pod as if they were on the same machine while at the same time maintaining a degree of isolation.

## 15. What is the job of the kube-scheduler?
The kube-scheduler assigns nodes to newly created pods.

## 16. What is a cluster of containers in Kubernetes? 
A cluster of containers is a set of machine elements that are nodes. Clusters initiate specific routes so that the containers running on the nodes can communicate with each other. In Kubernetes, the container engine (not the server of the Kubernetes API) provides hosting for the API server.

## 17. What is Minikube?
With the help of Minikube, users can Kubernetes locally. This process lets the user run a single-node Kubernetes cluster on your personal computer, including Windows, macOS, and Linus PCs. With this, users can try out Kubernetes also for daily development work.

## 18. What is a Namespace in Kubernetes?
Namespaces are used for dividing cluster resources between multiple users. They are meant for environments where there are many users spread across projects or teams and provide a scope of resources.

## 19. Name the initial namespaces from which Kubernetes starts?
Default
Kube – system
Kube – public
## 20. What is the Kubernetes controller manager?
The controller manager is a daemon that is used for embedding core control loops, garbage collection, and Namespace creation. It enables the running of multiple processes on the master node even though they are compiled to run as a single process.

## 21. What are the types of controller managers?
The primary controller managers that can run on the master node are the endpoints controller, service accounts controller, namespace controller, node controller, token controller, and replication controller.

## 22. What is etcd?
Kubernetes uses etcd as a distributed key-value store for all of its data, including metadata and configuration data, and allows nodes in Kubernetes clusters to read and write data. Although etcd was purposely built for CoreOS, it also works on a variety of operating systems (e.g., Linux, BSB, and OS X) because it is open-source. Etcd represents the state of a cluster at a specific moment in time and is a canonical hub for state management and cluster coordination of a Kubernetes cluster.

## 23. What are the different services within Kubernetes?
Different types of Kubernetes services include: 

Cluster IP service
Node Port service
External Name Creation service and 
Load Balancer service
## 24. What is ClusterIP?
The ClusterIP is the default Kubernetes service that provides a service inside a cluster (with no external access) that other apps inside your cluster can access. 

## 25. What is NodePort? 
The NodePort service is the most fundamental way to get external traffic directly to your service. It opens a specific port on all Nodes and forwards any traffic sent to this port to the service.

## 26. What is the LoadBalancer in Kubernetes? 
The LoadBalancer service is used to expose services to the internet. A Network load balancer, for example, creates a single IP address that forwards all traffic to your service. 

## 27. What is the Ingress network, and how does it work?
 An ingress is an object that allows users to access your Kubernetes services from outside the Kubernetes cluster. Users can configure the access by creating rules that define which inbound connections reach which services.

How does it work- This is an API object that provides the routing rules to manage the external users' access to the services in the Kubernetes cluster through HTTPS/ HTTP. With this, users can easily set up the rules for routing traffic without creating a bunch of load balancers or exposing each service to the nodes.

## 28. What do you understand by Cloud controller manager?
You must have heard about Public, Private and hybrid clouds. With the help of cloud infrastructure technologies, you can run Kubernetes on them. In the context of Cloud Controller Manager, it is the control panel component that embeds the cloud-specific control logic. This process lets you link the cluster into the cloud provider's API and separates the elements that interact with the cloud platform from components that only interact with your cluster. 

This also enables the cloud providers to release the features at a different pace compared to the main Kubernetes project. It is structured using a plugin mechanism and allows various cloud providers to integrate their platforms with Kubernetes.

## 29. What is Container resource monitoring?
This refers to the activity that collects the metrics and tracks the health of containerized applications and microservices environments. It helps to improve health and performance and also makes sure that they operate smoothly.

## 30. What is the difference between a replica set and a replication controller?
A replication controller is referred to as RC in short. It is a wrapper on a pod. This provides additional functionality to the pods, which offers replicas. 

It monitors the pods and automatically restarts them if they fail. If the node fails, this controller will respawn all the pods of that node on another node. If the pods die, they won't be spawned again unless wrapped around a replica set. 

Replica Set, on the other hand, is referred to as rs in short. It is told as the next-generation replication controller. This kind of support has some selector types and supports the equality-based and the set-based selectors. 

It allows filtering by label values and keys. To match the object, they have to satisfy all the specified label constraints.

## 31. What is a headless service?
A headless service is used to interface with service discovery mechanisms without being tied to a ClusterIP, therefore allowing you to directly reach pods without having to access them through a proxy. It is useful when neither load balancing nor a single Service IP is required. 

## 32. What are federated clusters?
The aggregation of multiple clusters that treat them as a single logical cluster refers to cluster federation. In this, multiple clusters may be managed as a single cluster. They stay with the assistance of federated groups. Also, users can create various clusters within the data center or cloud and use the federation to control or manage them in one place. 

You can perform cluster federation by doing the following: 

Cross cluster that provides the ability to have DNS and Load Balancer with backend from the participating clusters. 

Users can sync resources across different clusters in order to deploy the same deployment set across the various clusters.

## 33. What is Kubelet?
The kubelet is a service agent that controls and maintains a set of pods by watching for pod specs through the Kubernetes API server. It preserves the pod lifecycle by ensuring that a given set of containers are all running as they should. The kubelet runs on each node and enables the communication between the master and slave nodes.

## 34. What is Kubectl?
Kubectl is a CLI (command-line interface) that is used to run commands against Kubernetes clusters. As such, it controls the Kubernetes cluster manager through different create and manage commands on the Kubernetes component

## 35. Give examples of recommended security measures for Kubernetes.
Examples of standard Kubernetes security measures include defining resource quotas, support for auditing, restriction of etcd access, regular security updates to the environment, network segmentation, definition of strict resource policies, continuous scanning for security vulnerabilities, and using images from authorized repositories.

## 36. What is Kube-proxy? 
Kube-proxy is an implementation of a load balancer and network proxy used to support service abstraction with other networking operations. Kube-proxy is responsible for directing traffic to the right container based on IP and the port number of incoming requests.

## 37. How can you get a static IP for a Kubernetes load balancer? 
A static IP for the Kubernetes load balancer can be achieved by changing DNS records since the Kubernetes Master can assign a new static IP address.

## 38 kubectl command
### Get commands with basic output
kubectl get services                          # List all services in the namespace
kubectl get pods --all-namespaces             # List all pods in all namespaces
kubectl get pods -o wide                      # List all pods in the current namespace, with more details
kubectl get deployment my-dep                 # List a particular deployment
kubectl get pods                              # List all pods in the namespace
kubectl get pod my-pod -o yaml                # Get a pod's YAML

### Describe commands with verbose output
kubectl describe nodes my-node
kubectl describe pods my-pod

### List Services Sorted by Name
kubectl get services --sort-by=.metadata.name

### List pods Sorted by Restart Count
kubectl get pods --sort-by='.status.containerStatuses[0].restartCount'

### List PersistentVolumes sorted by capacity
kubectl get pv --sort-by=.spec.capacity.storage

### Link
[kubectl Cheat Sheet]: https://kubernetes.io/docs/reference/kubectl/cheatsheet/