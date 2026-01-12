---

# **DevOps – My Learning Journey**

This repository contains my notes and understanding of **DevOps concepts**.

---

## **Day 49**

## **Kubernetes Monitoring Using Prometheus and Grafana**

---

## **What is Prometheus?**

Prometheus is an **open-source monitoring and alerting tool** used to **collect, store, and query metrics** from applications, servers, and Kubernetes clusters.

---

## **What does Prometheus monitor?**

* CPU usage
* Memory usage
* Disk usage
* Network traffic
* Pod and Node health
* Application-specific metrics

---

## **How Prometheus works (Simple Flow)**

1. Applications / systems expose metrics using HTTP `/metrics`
2. Prometheus **pulls (scrapes)** metrics at regular intervals
3. Metrics are stored in a **time-series database**
4. Alerts are triggered if predefined thresholds are crossed

---

## **What is Grafana?**

Grafana is an **open-source visualization tool** used to **create dashboards and graphs** from metrics collected by tools like Prometheus.

---

## **What Grafana does**

* Connects to Prometheus (and other data sources)
* Displays metrics as:

  * Graphs
  * Charts
  * Tables
  * Dashboards
* Helps teams **understand system health easily**

---

## **Why Grafana is needed?**

Prometheus data is:

* Text-based
* Query-driven (PromQL)

Grafana makes it:

* Visual
* Easy to understand
* Presentable for teams & management

---

## **Installation of Helm in Linux (Ubuntu / Debian)**

### **Step 1: Install Helm**

```bash
sudo apt-get update
sudo apt-get install -y helm
```

### **Step 2: Verify Helm installation**

```bash
helm version
```

---

## **Installation of Prometheus in Linux (Ubuntu / Debian)**

### **Step 1: Add Helm repository**

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
```

### **Step 2: Update Helm repository**

```bash
helm repo update
```

### **Step 3: Install Prometheus**

```bash
helm install prometheus prometheus-community/prometheus
```

### **Step 4: Expose Prometheus Service**

This is required to access **prometheus-server** using your browser.

```bash
kubectl expose service prometheus-server \
--type=NodePort \
--target-port=9090 \
--name=prometheus-server-ext
```

---

## **Installation of Grafana in Linux (Ubuntu / Debian)**

### **Step 1: Add Helm repository**

```bash
helm repo add grafana https://grafana.github.io/helm-charts
```

### **Step 2: Update Helm repository**

```bash
helm repo update
```

### **Step 3: Install Grafana**

```bash
helm install grafana grafana/grafana
```

### **Step 4: Expose Grafana Service**

This is required to access **Grafana UI** using your browser.

```bash
kubectl expose service grafana \
--type=NodePort \
--target-port=3000 \
--name=grafana-ext
```

---

## **Screenshot of Implementation**

![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()

---
