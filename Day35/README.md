---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 35

### Docker Compose

**What is Docker Compose?**

--> Docker Compose is a tool that helps you define and manage **multi-container Docker applications** easily.

Instead of running multiple `docker run` commands manually, Docker Compose lets you describe your entire application (services, networks, and volumes) in **one YAML file** (usually named `docker-compose.yml`) and start everything with a **single command**.


![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/6666e7acb04212c070de5ec96c6aaa730a766ded/Day35/Day%2035%2001.png)

---

### **Example**

A simple setup with:

* A **web application** (built with Node.js or Python Flask)
* A **database** (like MySQL)

You can define both in one file — **docker-compose.yml**

```yaml
version: "3"
services:
  web:
    image: mywebapp:latest
    ports:
      - "8080:80"
    depends_on:
      - db

  db:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: example
```

---

### **Command to Run Docker Compose**

```bash
docker-compose up
```

---

### **Why Use Docker Compose?**

1. **Multi-container management:**
   Easily handle multiple containers (like app + database + cache) together.

2. **Single configuration file:**
   Everything (network, volumes, services) is described in one YAML file.

3. **Simplifies development:**
   Makes it easy to set up local development environments identical to production.

4. **Reusable and portable:**
   The same file can be used across different environments (dev, test, prod).

---

### **In Short**

**Docker Compose = One file + One command → Multiple Containers Working Together**

---
