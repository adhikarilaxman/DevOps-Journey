---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Configuration Management with Ansible

### Tools for Configuration Management

1. Puppet
2. Chef
3. Ansible
4. Salt

---

### 🔹 What is Configuration Management?

Configuration Management is the process of **automating the setup, management, and maintenance of servers and applications**.

Instead of manually installing software or changing setups on each server, tools like **Ansible** handle it for you.

---

### Why Ansible?

* **Agentless** → No need to install extra software on target servers.
* **Simple** → Uses YAML (easy, human-readable language).
* **Automation** → Handles repetitive tasks (installing software, configuring servers, deploying apps).
* **Scalable** → Works with a few servers or thousands at once.

---

### 🔹 Difference Between Puppet and Ansible

| **Puppet**                | **Ansible**         | **Explanation**                                                                                                      |
| ------------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Pull Model**            | **Push Model**      | Puppet uses a **pull model** (agents pull from Master). Ansible uses a **push model** (control node pushes configs). |
| **Master/Slave**          | **Agentless**       | Puppet needs a **Master + Agents**. Ansible only needs **SSH/WinRM** (no agents).                                    |
| **DSL (Puppet Language)** | **YAML (Simple)**   | Puppet uses a special language (DSL). Ansible uses simple **YAML**.                                                  |
| **Linux-focused**         | **Linux & Windows** | Puppet was built mainly for Linux (Windows added later). Ansible supports both well.                                 |

---

### 🔹 Disadvantages of Ansible

1. **Windows Support (Limited)** → Strong on Linux, but fewer features for Windows.
2. **Debugging Issues** → Error messages/logs are not always clear.
3. **Performance (Speed)** → Can be slower on very large infrastructures since it pushes configs to each server.

---

### Questions Asked

1. **Which language does Ansible use?**
   → Python (backend), YAML (for playbooks).

2. **Which OS supports Ansible?**
   → Works on both **Linux** (via SSH) and **Windows** (via WinRM).

3. **Which mechanism does Ansible use?**
   → **Push Mechanism**.

4. **Does Ansible support all cloud platforms?**
   → Yes  (AWS, Azure, GCP, etc.).

---
