---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 17 Notes

### AWS Services for DevOps

---

### 1. **EC2 (Elastic Compute Cloud)**

* Virtual servers in the cloud.
* Used to run applications, just like a computer but hosted on AWS.

---

### 2. **VPC (Virtual Private Cloud)**

* Your own private network inside AWS.
* You control connectivity and security of your servers.

---

### 3. **EBS (Elastic Block Store)**

* Storage that works like a hard disk for EC2.
* Data remains safe even if the instance stops or restarts.

---

### 4. **S3 (Simple Storage Service)**

* Cloud storage for files, backups, images, or logs.
* Highly durable, secure, and scalable.

---

### 5. **IAM (Identity and Access Management)**

* Manages users, groups, and permissions.
* Ensures only the right people or services can access resources.

---

### 6. **CloudWatch**

* Monitoring and logging tool.
* Tracks metrics like CPU, memory, logs, and alerts.

---

### 7. **Lambda**

* Serverless computing service.
* Run code without managing servers.
* Pay only for execution time.

---

### 8. **Cloud Build Services**

* Tools for automating CI/CD pipelines:

  * **CodePipeline** → Automates build, test, and deployment workflows.
  * **CodeBuild** → Compiles and tests code.
  * **CodeDeploy** → Deploys apps automatically to EC2, Lambda, or on-premise servers.

---

### 9. **AWS Config**

* Tracks and records configurations of AWS resources.
* Useful for auditing and compliance.

---

### 10. **Billing and Cost Management**

* Dashboard to track AWS usage and spending.
* Helps set budgets and receive alerts.

---

### 11. **AWS KMS (Key Management Service)**

* Manages encryption keys.
* Secures sensitive data using cryptography.

---

### 12. **CloudTrail**

* Records all AWS API calls.
* Helps in monitoring **who did what, when, and where**.
* Critical for security auditing.

---

### 13. **EKS (Elastic Kubernetes Service)**

* Managed Kubernetes service.
* Makes it easier to run containerized applications.

---

### 14. **ECS (Elastic Container Service) & Fargate**

* **ECS** → Run and manage Docker containers.
* **Fargate** → Run containers without worrying about servers.

---

### 15. **ELK Stack (Elasticsearch, Logstash, Kibana)**

* Used for log management and analysis.
* Collects, stores, and visualizes logs for troubleshooting and monitoring.

---

These services together help in **automation, deployment, monitoring, scaling, and security**, which are key pillars of **DevOps on AWS**.
