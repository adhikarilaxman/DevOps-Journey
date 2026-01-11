---

# **DevOps – My Learning Journey**

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 48**

### **Kubernetes ConfigMaps & Secrets**

---

## **ConfigMaps**

A **ConfigMap** is a Kubernetes object used to store **non-sensitive configuration data** in key-value format.

### **Used for storing:**

* Environment variables
* Application configuration files
* Command-line arguments

### **Examples of data stored in ConfigMaps:**

* Database host
* Application port
* Feature flags
* Log levels

---

## **Secrets**

A **Secret** is a Kubernetes object used to store **sensitive data securely**.

### **Used for storing:**

* Passwords
* API keys
* Tokens
* Certificates

### **Why Secrets are needed?**

* Prevents sensitive data from being exposed in plain text
* Improves security
* Allows secure configuration management

---
