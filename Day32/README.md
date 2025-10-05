---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 32

### Docker Volumes and Bind Mounts

When you run a container, by default, any data inside the container is temporary.
If the container stops or is deleted → the data is lost.

To solve this, Docker gives us data persistence options:

* **Volumes**
* **Bind Mounts**

---

### 1. Docker Volumes

* Volumes are managed by Docker itself.
* Docker stores them in a special location on the host (usually `/var/lib/docker/volumes/`).
* They are completely separate from the container’s lifecycle (i.e., data won’t be deleted if the container stops or is removed).
* Easy to back up, migrate, and share between multiple containers.

---

### 2. Bind Mounts

* Bind mounts link a specific folder/file from the host machine to the container.
* Whatever changes happen inside the container → reflect on the host, and vice versa.
* Useful for development (e.g., syncing your source code on your laptop with the container).
* Less portable than volumes because they depend on the host machine’s file paths.


Summary:

Volumes → safer, portable, best for production

Bind Mounts → flexible, great for development

---

### Screenshot of Implementation

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
