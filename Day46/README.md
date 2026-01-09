# **DevOps – My Learning Journey**

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 46**

### **Kubernetes RBAC**

---

### **What is RBAC in Kubernetes?**

--> RBAC (Role-Based Access Control) in Kubernetes is a security mechanism that controls **who can do what** in a Kubernetes cluster.

---

### **Why RBAC is needed?**

* Kubernetes has many resources (Pods, Services, Deployments, Secrets, etc.).
* Not every user or application should have full access.
* RBAC helps to:

  * Improve security.
  * Follow least-privilege control.
  * Prevent accidental or unauthorized changes.

---

## **Kubernetes Service Accounts**

### **What is a Service Account?**

--> A Service Account is an identity used by applications running inside Pods to interact with the Kubernetes API.

**Example:**

A Pod that needs to:

* Read ConfigMaps
* List Pods
* Access Secrets

---

## **Roles**

### **What is a Role?**

A Role defines what actions are allowed on which resources within a namespace.

It contains:

* Resources (pods, services, deployments)
* Verbs (get, list, create, delete)

**Note:**

* Roles are namespace-scoped.

---

## **RoleBindings**

### **What is a RoleBinding?**

A RoleBinding connects:

* A Role
* To a User / Group / Service Account

Without RoleBinding → Role does nothing.

---

## **Identity Providers**

### **What is an Identity Provider (IdP)?**

--> An Identity Provider is an external system that:

* Verifies user identity
* Provides authentication tokens to Kubernetes

---
