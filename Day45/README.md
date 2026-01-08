---

# **DevOps – My Learning Journey**

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 45**

### **KUBERNETES SERVICES – DEEP DIVE**

## **KUBERNETES INGRESS**

---

### **Static IP**

--> A static IP address is fixed and does not change over time.

**Key Characteristics**

* Manually assigned by a network administrator or ISP
* Remains the same every time the device connects
* Easy to locate and manage

---

### **Dynamic IP**

--> A dynamic IP address is automatically assigned and can change over time.

**Key Characteristics**

* Assigned by a DHCP server
* Changes periodically or when reconnecting
* Common for home and mobile users

---

### **Problems**

1. **Enterprise & TLS Load Balancing**

   * Sticky
   * TLS
   * Path-based routing
   * Host-based routing
   * Ratio-based load balancing

2. **Load Balancers**

   * Cloud provider dependent

---

### **Kubernetes Ingress**

--> Kubernetes Ingress is an API object that manages external access to services inside a Kubernetes cluster, mainly HTTP and HTTPS traffic.

--> Kubernetes Ingress is a way to control how outside users access applications running inside a Kubernetes cluster.

---

### **Why Ingress is needed?**

**Without Ingress**

* We must expose every service using NodePort or LoadBalancer
* This increases cost and becomes hard to manage

**With Ingress**

* Only one external IP
* Traffic is sent to many applications
* Easy to manage and cheaper

---

### **How Ingress works (Step by Step)**

1. User opens a website
2. Request reaches the Ingress Controller
3. Ingress checks rules like:

   * `/login` → Frontend Service
   * `/api` → Backend Service
4. Traffic is sent to the correct Service
5. Service sends it to the right Pod

---

### **Note**

* LoadBalancer exposes one service directly, while Ingress exposes multiple services using a single external entry point with smart routing.

---

### **Screenshots**

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/327315911b4a91f93dfffabc46a1d6d266a482e1/Day45/Day45%2001.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/327315911b4a91f93dfffabc46a1d6d266a482e1/Day45/Day45%2002.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/327315911b4a91f93dfffabc46a1d6d266a482e1/Day45/Day45%2003.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/327315911b4a91f93dfffabc46a1d6d266a482e1/Day45/Day45%2004.png)


![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/327315911b4a91f93dfffabc46a1d6d266a482e1/Day45/Day45%2005.png)

---
