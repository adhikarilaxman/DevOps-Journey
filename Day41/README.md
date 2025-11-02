---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 41**

### **KUBERNETES DEPLOYMENT | REPLICASETS**

---

### **What is the difference between Pod vs Container vs Deployment**

| **Feature**              | **Container**                                                                 | **Pod**                                                                             | **Deployment**                                                                  |
| ------------------------ | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Definition**           | A lightweight, standalone unit that runs an application and its dependencies. | The smallest deployable unit in Kubernetes that can contain one or more containers. | A higher-level object that manages and maintains multiple pods.                 |
| **Purpose**              | Runs a single process or service.                                             | Groups one or more containers that work together and share resources.               | Ensures the desired number of pods are running and handles scaling and updates. |
| **Managed By**           | Docker (or container runtime like containerd).                                | Kubernetes.                                                                         | Kubernetes Controller Manager.                                                  |
| **Lifecycle Management** | Manual — you start/stop containers yourself.                                  | Managed automatically by Kubernetes.                                                | Automates pod creation, deletion, and updates.                                  |
| **Scaling**              | Must run multiple containers manually.                                        | Pods can be replicated, but manual management is hard.                              | Automatically scales pods up or down based on demand.                           |
| **Example Use Case**     | A single NGINX web server container.                                          | A Pod with NGINX + sidecar container for logging.                                   | A Deployment ensuring 3 replicas of the NGINX pod always run.                   |
| **File Example**         | `Dockerfile`                                                                  | `pod.yaml`                                                                          | `deployment.yaml`                                                               |

**Container →** Runs your app.
**Pod →** Wraps one or more containers to make them manageable in Kubernetes.
**Deployment →** Ensures a certain number of pods are always running, handles scaling, and updates.

---

### **What is ReplicaSet in Kubernetes?**

--> A **ReplicaSet** in Kubernetes ensures that a specific number of **identical Pods** are running at all times.

---

### **Purpose of ReplicaSet**

* To maintain **high availability** of your application.
* If a Pod crashes or gets deleted → the ReplicaSet automatically **creates a new one**.
* If you have too many Pods → it will **remove extra ones**.

---

### **Screenshot of Implementation**

![image alt]()

![image alt]()

![image alt]()

---
