---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 37

### Kubernetes

What is Kubernetes?


--> Kubernetes (also called K8s) is an open-source container orchestration platform developed by Google.
It helps you automate the deployment, scaling, and management of containerized applications (like Docker containers).


Key Features of Kubernetes

1. Container Orchestration – Manages multiple containers across many machines.

2. Self-Healing – Restarts or replaces failed containers automatically.

3. Load Balancing – Distributes traffic evenly across containers.

4. Auto-Scaling – Increases or decreases containers based on demand.

5. Rolling Updates – Updates apps without downtime.

6. Resource Management – Efficiently uses CPU, RAM, and storage across the cluster

Difference Between Docker and Kubernetes
| Feature             | **Docker**                                      | **Kubernetes**                                                       |
| ------------------- | ----------------------------------------------- | -------------------------------------------------------------------- |
| **Definition**      | Platform to build, run, and manage containers.  | System to manage and orchestrate multiple containers across servers. |
| **Main Purpose**    | Containerization (creates containers).          | Orchestration (manages containers).                                  |
| **Scope**           | Works on a single host.                         | Works across multiple hosts (cluster).                               |
| **Scaling**         | Manual – you have to start containers yourself. | Automatic – scales pods based on load.                               |
| **Fault Tolerance** | If a container crashes, it stops running.       | Automatically restarts or reschedules failed pods.                   |
| **Networking**      | Basic networking on a single machine.           | Advanced multi-node networking (service discovery, load balancing).  |
| **Load Balancing**  | Manual setup needed.                            | Built-in load balancing.                                             |
| **Use Case**        | Best for building and running containers.       | Best for managing and scaling containers in production.              |


Problems with Containers 

1. Single Host
- Containers on a single machine (host) cannot easily communicate or share workloads with containers on other machines.
- If that machine fails, all containers on it go down.

2. Auto Healing
- If a container crashes, Docker doesn’t automatically restart or replace it.
- You have to manually restart containers or use custom scripts.

3. Auto Scaling
- Containers don’t automatically scale up or down based on traffic or CPU usage.
- You must manually start or stop additional containers when demand changes.

4. Simple Platform 
- Docker alone provides a simple container runtime — not a full platform for managing many containers.
- It lacks features like orchestration, monitoring, and service discovery.
















