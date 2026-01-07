# **DevOps – My Learning Journey**

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 44**

### **KUBERNETES SERVICES – DEEP DIVE**

### What is a Kubernetes Service?

A Kubernetes Service is used to provide a **stable way to access Pods**.

Pods are temporary in nature:

* Pods can be created, deleted, or replaced.
* Their IP addresses keep changing.

A Service solves this problem by providing a **stable IP address and DNS name** to access Pods.

---

## **1. Load Balancing**

### What is Load Balancing?

Load Balancing means **distributing traffic evenly across multiple Pods**.

### How Kubernetes Service Helps:

* A Service groups multiple Pods using **labels**.
* When a request comes:

  * It automatically sends traffic to any healthy Pod.
  * Traffic is distributed evenly across Pods.

---

## **2. Service Discovery**

### What is Service Discovery?

Service Discovery means **how Pods find and communicate with each other without knowing IP addresses**.

### Problem Without Service:

* Pod IP addresses change frequently.
* It is hard to manually update IPs.

### How Kubernetes Solves This:

Every Service gets:

* A **DNS name**
* A **stable IP address**

This allows Pods to communicate using the Service name instead of IPs.

---

## **3. Expose (Making Application Accessible)**

### What Does “Expose” Mean?

Expose means making your application accessible:

* Inside the cluster
* Outside the cluster

---

## **Kubernetes Service Types for Exposing Applications**

### **1. ClusterIP (Default)**

* Accessible only inside the cluster.
* Used for internal communication (frontend → backend).

### **2. NodePort**

* Exposes the application using:

  ```
  NodeIP:NodePort
  ```
* Useful for testing or internal access.

### **3. LoadBalancer**

* Exposes the application to the internet.
* Uses a cloud provider load balancer (AWS, Azure, GCP).

---

## **Screenshots**

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2001.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2002.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2003.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2004.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2005.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2006.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2007.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2008.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2009.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2010.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2011.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2012.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2013.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/55ceda94ee60db2b23e7de24980f92fd66c0a706/Day44/Day44%2014.png)

---
