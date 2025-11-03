---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 42**

### **KUBERNETES SERVICES | DISCOVERY | LOAD BALANCING | NETWORKING**

---

### **What is a Kubernetes Service?**

* A **Service** in Kubernetes is an abstraction that defines a **stable way to access Pods**.
* Pods in Kubernetes are **temporary** — they can be created, destroyed, or replaced anytime.
* When a Pod dies, a new one may come up with a **different IP address**, making direct communication difficult.
* A **Kubernetes Service** solves this by providing a **permanent IP address and DNS name** that automatically routes traffic to the correct Pods.

---

### **Types of Kubernetes Services**

1. **Cluster IP (Default)**

   * Exposes the Service **only inside the cluster** (internal communication).

2. **Node Port**

   * Exposes the Service on a **static port** on each Node’s IP.
   * Used to **expose the port within the organization**.

3. **Load Balancer**

   * Exposes the Service **externally** using a **cloud provider’s load balancer**.

---

### **What is Service Discovery?**

* **Service Discovery** is the process by which applications (like Pods) **find and communicate** with each other inside a Kubernetes cluster — without needing to know IP addresses manually.

---

### **What is Load Balancing?**

* **Load Balancing** is the process of **distributing network traffic evenly** across multiple Pods so that no single Pod is overloaded.

---

### **How It Works in Kubernetes**

When multiple Pods match a Service’s **selector**, the Service automatically:

* Keeps track of all available Pod IPs.
* Spreads incoming traffic evenly across them.
* Detects and removes Pods that are down or unresponsive.

Kubernetes handles this automatically — you don’t need to set up any external load balancer inside the cluster.

---
