---

# **DevOps – My Learning Journey**

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 47**

### **Kubernetes Custom Resources**

---

### **What is a Custom Resource (CR)?**

* A **Custom Resource** is a way to extend Kubernetes by adding your own resource types, similar to:

  * Pod
  * Service
  * Deployment

* Kubernetes comes with built-in resources, but sometimes they are **not enough for specific applications**.

* Custom Resources allow you to:

  * Define new objects
  * Make Kubernetes understand application-specific requirements

---

### **Why do you need a Custom Resource in Kubernetes?**

* Built-in Kubernetes resources are **generic**.
* They may not fully represent **complex or application-specific needs**.

#### **Problems without Custom Resources:**

* Application logic is handled manually
* Complex deployments are difficult to automate
* No Kubernetes-native way to manage custom systems

#### **Custom Resources solve this by:**

* Representing application logic as Kubernetes objects
* Enabling automation using controllers
* Making applications Kubernetes-native

#### **Example:**

* Instead of manually managing:

  * MySQL Pods
  * Volumes
  * Backups

* Create a **MySQL Custom Resource** and let Kubernetes manage it.

---

### **What is a Custom Resource Definition (CRD)?**

* A **CRD** is the schema and blueprint that tells Kubernetes:

  * What the Custom Resource is called
  * What fields it has
  * Whether it is namespace-scoped or cluster-scoped

#### **Once a CRD is created:**

* Kubernetes API Server recognizes the new resource
* You can use `kubectl` commands to manage it

---

### **What is a Custom Controller?**

* A **Custom Controller** is a program that:

  * Watches Custom Resources
  * Continuously checks desired state vs actual state
  * Takes action to reconcile the difference

---

### **How to write a Custom Controller in Kubernetes?**

#### **Step 1: Create a CRD**

* Define the custom resource schema

#### **Step 2: Write Controller Logic**

* Watch for:

  * Create events
  * Update events
  * Delete events

* Compare:

  * Desired state
  * Current state

* Perform actions such as:

  * Creating Pods
  * Creating Services
  * Running Jobs

#### **Step 3: Use Controller Frameworks**

* Operator SDK
* Kubebuilder
* Client-Go

#### **Step 4: Run Controller inside the Cluster**

* Usually deployed as a Pod

---

### **Common Languages Used**

* Go (most common)
* Python
* Java

---
