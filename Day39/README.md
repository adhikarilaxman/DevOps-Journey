---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 39

### How to Manage Hundreds of Kubernetes Clusters?

---

### **Popular Kubernetes Distributions**

* A Kubernetes distribution is a packaged version of Kubernetes that includes additional tools, pre-configured settings, and integrations to make installation, management, and scaling easier.

**Kubernetes Distributions:**

1. Minikube
2. K3S
3. MicroK8s
4. OpenShift (by Red Hat)
5. EKS (Elastic Kubernetes Service)
6. Rancher

---

### **Managing Hundreds of Kubernetes Clusters**

* When organizations grow, they often need to manage hundreds of clusters — across different clouds, teams, and environments.
* Manually managing them is difficult, so we use **centralized management tools and strategies**.

**Tools and Platforms Used:**

1. Rancher
2. Anthos (by Google Cloud)
3. Red Hat Advanced Cluster Management (ACM)
4. Azure Arc
5. Fleet / Argo CD / Flux CD
6. Kops
7. Kubectl

---

### **Kubernetes Installation Using KOPS on EC2**

**Step 1:** Launch an EC2 Instance on AWS (Ubuntu)

**Step 2:** Install Dependencies on EC2

```bash
sudo apt update
sudo apt install -y curl jq awscli git
```

**Step 3:** Install Kops

1. Download the latest Kops release:

   ```bash
   KOPS_VERSION=$(curl -s https://api.github.com/repos/kubernetes/kops/releases/latest | jq -r .tag_name)
   ```
2. Download the Kops binary:

   ```bash
   curl -LO https://github.com/kubernetes/kops/releases/download/${KOPS_VERSION}/kops-linux-amd64
   ```
3. Make the binary executable:

   ```bash
   chmod +x kops-linux-amd64
   ```
4. Move it to `/usr/local/bin` for global access:

   ```bash
   sudo mv kops-linux-amd64 /usr/local/bin/kops
   ```
5. Verify Kops Installation:

   ```bash
   kops version
   ```

**Step 4:** Configure AWS CLI

---
