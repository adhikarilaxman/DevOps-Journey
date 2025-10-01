---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 28

Introduction to Docker Containers

### What is a Docker Container?

--> A Docker container is like a lightweight box that contains everything your application needs to run:

* Code
* Libraries
* Dependencies
* Configuration

It ensures your app will run the same way on any computer (developer’s laptop, test server, cloud).

---

### Container vs Virtual Machine (VM)

| Feature        | **Container**                                             | **Virtual Machine (VM)**                                   |
| -------------- | --------------------------------------------------------- | ---------------------------------------------------------- |
| **Definition** | Lightweight environment to run apps with all dependencies | Full OS running on top of another OS                       |
| **Size**       | MBs (small, fast to start)                                | GBs (large, slow to start)                                 |
| **Speed**      | Starts in seconds                                         | Takes minutes to boot                                      |
| **Isolation**  | Shares the resources from the host OS                     | Runs a full OS for each VM                                 |
| **Efficiency** | Very efficient (low memory/CPU usage)                     | Heavy on resources                                         |
| **Use Case**   | Microservices, CI/CD pipelines, cloud apps                | Running multiple OS on one machine (e.g., Linux + Windows) |

---

### Docker Deployment Models
 ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/45ef285779294e1529c871afa455156676fe8f94/Day28/Day%2028%20Docker%20Deployment%20Models.png)

**Model 1: Docker on a Physical Server**

* Here, Docker is installed directly on the host operating system of a physical machine (bare-metal server).
* Containers run directly on top of the OS without any extra virtualization layer.

**Pros:**

* Very efficient → no overhead of virtual machines.
* Better performance because containers talk directly to the OS.

**Cons:**

* Less flexibility (bound to that physical server).
* Harder to scale if you need more servers.

---

**Model 2: Docker on a VM (e.g., EC2 Instance)**

* Here, you first create a Virtual Machine (like on AWS EC2, VMware, VirtualBox).
* Inside that VM, you install Docker.
* Then containers run inside that VM.

**Pros:**

* More flexible → you can spin up multiple VMs in the cloud.
* Each VM can run Docker containers independently.
* More isolation (VM boundaries).

**Cons:**

* Extra overhead because VM itself needs CPU, memory, and storage.
* Slightly slower than Model 1.

---
