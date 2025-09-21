---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 20

### Infrastructure as Code (IaC)

**Definition**: Infrastructure as Code means managing and provisioning infrastructure (servers, networks, databases, etc.) using code instead of doing it manually.

* Example:
  Normally, to create 5 servers, you would log in to the AWS console and click 5 times.
  With IaC, you just write a code file (e.g., Terraform file) that says “create 5 servers” and it will automatically do it for you.

---

### Benefits of IaC in DevOps

* Saves time – No manual clicks, everything automated.
* Avoids mistakes – Reduces human errors.
* Version control – Infrastructure code is stored in Git, so changes are tracked.
* Reproducible – Same setup can be deployed in development, testing, and production environments.

---

### Uses of IaC in DevOps

* Fast provisioning – Spin up servers and networks in minutes.
* Scalability – Quickly add or remove infrastructure when needed.
* Consistency – Same code works everywhere (no "it works on my machine" issue).
* CI/CD integration – Applications and infrastructure can be deployed together.

---

### Terraform

**Definition**: Terraform is an Infrastructure as Code tool developed by HashiCorp.

* What it does:

  * Defines infrastructure in simple code files (HCL – HashiCorp Configuration Language).
  * Automates infrastructure setup, modification, and destruction.

* Why Terraform?

  * Works across multiple cloud platforms (AWS, Azure, GCP, etc.).
  * Easy to scale, change, or destroy infrastructure.
  * Improves automation and consistency in infrastructure management.

---

### API (Application Programming Interface)

**Definition**: An API is a way for two applications or systems to communicate with each other.

* Example:

  * A weather app uses a Weather API to fetch live temperature data.
  * Payment apps (like PhonePe) use Bank APIs to check balances or process transactions.

---

### Hybrid Cloud

**Definition**: A Hybrid Cloud is a combination of Public Cloud (AWS, Azure, GCP) and Private Cloud/On-premises servers.

* Example:

  * A bank stores sensitive customer data in its private cloud.
  * It runs its mobile app and website on AWS (public cloud) for scalability.

* Advantages:

  * Security – Sensitive data stays in private infrastructure.
  * Scalability – Extra workloads can run on the public cloud.
  * Cost saving – Reduces the need for too many physical servers.
  * Flexibility – Allows choosing where to run which workload.

---
