---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 29

### Docker

**Why are containers lightweight?**

--> Containers are lightweight because they share the host operating system (OS) kernel instead of running their own full OS like a Virtual Machine.

Here’s the difference:

**Virtual Machine (VM):**

* Needs a full OS (Linux, Windows, etc.) for each VM.
* Each OS takes GBs of storage and lots of RAM/CPU.
* Boots slowly (like starting another computer inside your computer).

**Container:**

* Does not need a full OS.
* Uses the host OS kernel and just brings along the app + libraries + dependencies.
* Much smaller (MBs in size) and faster to start (seconds).

---

**What is a Docker Image?**

--> A Docker Image is like a blueprint or template for creating containers.

It contains:

* Application code
* Dependencies (libraries, packages)
* Environment settings (config, OS layers)

When you run a Docker Image → it becomes a **Docker Container**.

---

**What is Docker Daemon?**

--> The Docker Daemon (`dockerd`) is the background service that runs on your system and does all the hard work of Docker.

---

### Screenshots

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

---
