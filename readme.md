# Kubernetes (K8)

## What is Kubernetes and Why use it?

- Kubernetes is an open-source **container-orchestration system** for automating computer application deployment, scaling, and management.

- It is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation.

<p align=center>
	<img src=imgs/docker_kubernetes.png>
</p>

- **Advantages**
	- ***Self Healing***: Automatically dealing with containers malfunctioning.
	- ***Load Balancing and Service Discovery***: Balancing resources and traffic to improve efficiency.
	- ***Automated rollouts and rollback***: Being able to rollback to a previous working version of a container.
	- ***Auto Scaling***: Scales containers as the app grows.
	- ***Automatic bin packing***: Kubernetes can fit containers onto your nodes to make the best use of resources.
	- ***Storage orchestration***: Automatically mounts a storage system of your choice (local, cloud, etc).

## When to use or Not use Kubernetes (Use Cases)?

- **When to use**:
	- ***If an application is using a microservice architecture***: It works well in these types of architecture, especially since it's likely that other software like Docker is already being used to containerize the application.
	- ***When suffering from slow development and deployment***: Kubernetes (along with Docker) can effectively manage the development and deployment lifecycle for you so the team can focus their time on other processes.
	- ***To lower infrastructure costs***: Kubernetes uses an efficient resource management model at the container, pod, and cluster level, helping you lower cloud infrastructure costs by ensuring your clusters always have available resources for running applications.

- **When NOT to use**:
	- ***Simple applications***: If your application makes use of a monolithic architecture it may be tough to see the real benefits of containers and a tool used to orchestrate them. That’s because the very nature of a monolithic architecture is to have every piece of the application intertwined, whereas containers are used to separate your application into individual components.
	- ***Difficult Learning-curve***: Your team needs skills, and it is a complex technology with a lot of moving parts. There is an entry barrier to cross. If you don't have the time or resources to learn it, it's probably better if you don't implement it.

<p align=center>
	<img src=imgs/kubernetes_arch.PNG>
</p>

## Kubernetes Competitors

- Kubernetes is extremely powerful, yet difficult to learn and operate. This has given rise to an industry that aims to make Kubernetes easier to adopt and use. 

- The primary options you can choose instead of Kubernetes are:

	- **Container as a Service (CaaS)** — services like AWS Fargate and Azure Container Instances, which allow you to manage containers at scale without the complex orchestration capabilities provided by Kubernetes.
	- **Managed kubernetes services** — including Google Kubernetes Engine (GKE) and Amazon Elastic Kubernetes Service (EKS), which let you run managed, hosted Kubernetes clusters. These services remove much of the complexity of deploying, upgrading and maintaining Kubernetes, but still require expertise to manage.
	- **PaaS using Kubernetes—several providers** — such as OpenShift Container Platform and Rancher, offer complete cloud computing platforms, which have Kubernetes at their core, but offer simpler operation and built-in capabilities like security and networking. 
	- **Lightweight container orchestrators** — Kubernetes is the most popular container orchestrator, but is definitely not the only one. Docker Swarm and Nomad are two examples of capable, mature orchestrators, which are much less complex to use and maintain than Kubernetes

## Kubernetes Managed Services vs Non Managed Services

- **Managed Kubernetes Services** let users run managed, hosted Kubernetes clusters. These services remove much of the complexity of deploying, upgrading and maintaining Kubernetes, but still require expertise to manage.

- Examples are:
	- Google Kubernetes Engine (GKE)
	- Amazon Elastic Kubernetes Service (EKS)
	- Microsoft Kubernetes Azure (AKS)
	- IBM Cloud Kubernetes Service

- **Non Managed Kubernetes Services** let users have full access to the cluster and master all the other related management components. They’ll also have more control over the deployment and administration of their cluster.

- Examples are:
	- Kubespray
	- Kubeadm
	- Kops
	- Kubetail