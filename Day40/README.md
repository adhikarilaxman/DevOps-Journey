---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 40

### Kubernetes Pods | Deploying First App

---

### **Container vs Pod**

| **Feature**    | **Container**                                                                                | **Pod**                                                                                      |
| -------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| **Definition** | A container is a lightweight, standalone unit that runs an application and its dependencies. | A Pod is the smallest deployable unit in Kubernetes that can contain one or more containers. |
| **Managed By** | Docker (or any container runtime).                                                           | Kubernetes.                                                                                  |
| **Isolation**  | Containers are isolated from each other unless connected manually.                           | Containers inside the same Pod share the same network and storage.                           |
| **IP Address** | Each container gets its own IP (in Docker).                                                  | All containers in a Pod share a single IP.                                                   |
| **Use Case**   | Running a single app or service.                                                             | Grouping tightly coupled containers that work together (e.g., app + sidecar).                |
| **Example**    | A single NGINX web server container.                                                         | A Pod with NGINX + a log collector container.                                                |

 **A Pod = 1 or more containers working together, sharing the same network and storage.**

---

### **What is kubectl?**

* **kubectl** is the command-line tool used to interact with a Kubernetes cluster.
* It allows you to **deploy**, **manage**, and **inspect** applications running on Kubernetes.

---

### **Common kubectl Commands**

| **Command**                                | **Description**                                   |
| ------------------------------------------ | ------------------------------------------------- |
| `kubectl version`                          | Check Kubernetes client and server versions       |
| `kubectl get pods`                         | List all pods in the current namespace            |
| `kubectl get nodes`                        | Show all nodes in the cluster                     |
| `kubectl describe pod <pod-name>`          | Show detailed information about a pod             |
| `kubectl logs <pod-name>`                  | View logs of a specific pod                       |
| `kubectl apply -f <file.yaml>`             | Create or update resources defined in a YAML file |
| `kubectl delete pod <pod-name>`            | Delete a specific pod                             |
| `kubectl exec -it <pod-name> -- /bin/bash` | Access a running container inside a pod           |

---

### **Screenshot of Implementation**

![image alt]()

---
