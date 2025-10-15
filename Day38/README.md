---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 38

### Architecture of Kubernetes

* Kubernetes architecture is based on a **Master–Worker (Control Plane–Node)** model.
  It manages containerized applications running across multiple machines (called nodes).

* It ensures that your applications are always running, healthy, and scalable.

* The **Control Plane (Master)** is the brain that manages the cluster.

* The **Worker Nodes (Data Plane)** are the hands that run your applications (containers inside pods).

* **Kubernetes cluster = Control Plane (Master Node) + Worker Nodes**

**Example:**
Imagine you have a web app like Amazon:

* Frontend (React)
* Backend (Node.js)
* Database (MongoDB)

Kubernetes runs each part in separate Pods across multiple Worker Nodes, while the Control Plane keeps everything in sync.

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/144bb5f55ab68f69caac7d3b2923d8729d898146/Day38/Day38%2001%20Architecture%20of%20Kubernetes.png)

---

### Kubernetes Control Plane (Master Node)

* The Control Plane manages and monitors the entire cluster.

**Components of Control Plane:**

1. **API Server**

   * Entry point of Kubernetes. Accepts and processes commands (`kubectl`).
   * **Example:** When you run `kubectl create deployment myapp`, the API Server handles it.

2. **etcd**

   * Key-value database that stores cluster configuration and current state.
   * **Example:** Keeps record of running pods, services, and node info.

3. **Controller Manager**

   * Ensures desired state = current state. Restarts failed pods or replaces dead nodes.
   * **Example:** If 1 of 3 replicas goes down, it creates a new one.

4. **Scheduler**

   * Decides which node will run a new pod based on resource availability.
   * **Example:** If Node1 is busy, the Scheduler places the pod on Node2.

---

### Kubernetes Data Plane (Worker Nodes)

* The Data Plane (Worker Nodes) is where the actual workloads (applications) run.
* Each worker node runs multiple Pods, and each Pod has one or more containers.

**Example:**
A Node might run:

* Pod 1 → React frontend
* Pod 2 → Node.js backend
* Pod 3 → MongoDB database

**Components of Data Plane:**

1. **Kubelet**

   * Agent that ensures containers described in Pod specs are running.
   * **Example:** If a container crashes, Kubelet restarts it.

2. **Kube Proxy**

   * Manages network traffic and load balancing between pods/services.
   * **Example:** Routes frontend requests to backend pods.

3. **Container Runtime**

   * The engine that actually runs containers.
   * **Example:** Docker, containerd, or CRI-O are used here.

---
