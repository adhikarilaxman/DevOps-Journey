---
 
# **DevOps – My Learning Journey**  
 
This repository contains my notes and understanding of **DevOps concepts**. 

---

## **Day 43**

### **KUBERNETES INTERVIEW QUESTIONS PART - 1**

---

### **Q1. What is the difference between Docker and Kubernetes?**

→ Docker is a container platform, whereas Kubernetes is a container orchestration environment that offers capabilities like **Auto Healing**, **Auto Scaling**, **Clustering**, and **Enterprise-level features** such as **Load Balancing**.

---

### **Q2. What are the main components of Kubernetes architecture?**

→ On a broad level, Kubernetes components are divided into two parts:

1. **Control Plane** – API Server, Scheduler, Controller Manager, Cloud Controller Manager (C-CM), ETCD
2. **Data Plane** – Kubelet, Kube-proxy, Container Runtime

---

### **Q3. What are the main differences between Docker Swarm and Kubernetes?**

→ Kubernetes is better suited for large organizations as it offers **more scalability**, **advanced networking capabilities** (like network policies), and a **vast third-party ecosystem** for integrations.

---

### **Q4. What is the difference between a Docker container and a Kubernetes Pod?**

→ A **Pod** in Kubernetes is a runtime specification of a **container** in Docker.
A Pod provides a **declarative way of defining** containers using YAML and can **run multiple containers together** within the same Pod.

---

### **Q5. What is a Namespace in Kubernetes?**

→ In Kubernetes, a **Namespace** is a logical isolation of resources, networks, and RBAC policies.
For example:
If two projects share the same Kubernetes cluster —

* Project 1 can use **ns1**,
* Project 2 can use **ns2**,
  both without any overlap or authentication issues.

---

### **Q6. What is the role of Kube-Proxy?**

→ **Kube-Proxy** is a networking component that runs on each node in a Kubernetes cluster.
Its main job is to **manage network communication between Pods and Services** inside the cluster.
It ensures that traffic is **correctly routed and load-balanced** to the right Pods — even when Pods are added or removed dynamically.

---

### **Q7. What are the different types of Services in Kubernetes?**

→ There are three different types of Services that a user can create:

1. **Cluster IP Mode**
2. **Node Port Mode**
3. **Load Balancer Mode**

---

### **Q8. What is the difference between NodePort and LoadBalancer type Service?**

→

* **NodePort:** Exposes a Service on a **static port** (NodePort) on each Node’s IP (used for internal/external limited access).
* **LoadBalancer:** Exposes a Service **externally** using a **cloud provider’s Load Balancer** (used for public access).

---

### **Q9. What is the role of Kubelet?**

→ The **Kubelet** is the primary agent that runs on each **worker node** in a Kubernetes cluster.
It is responsible for **managing the lifecycle of Pods and containers** on that node — ensuring containers are healthy and running as defined in Pod specs.

---

### **Q10. Day-to-Day Activities on Kubernetes**

→

1. Managing Deployments
2. Monitoring Pods and Nodes
3. Scaling Applications
4. Managing Configurations and Secrets
5. Troubleshooting and Debugging
6. Resource Monitoring and Optimization

---
