---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 31

### Multi-Stage Docker Build

**What is Multi-Stage Docker Build?**

--> A multi-stage build means using multiple `FROM` statements in a single Dockerfile.
Each `FROM` creates a new stage.

* **First stage** → build or compile the app (heavy tools needed here).
* **Second stage** → copy only the final output (binary/app files) into a clean, small image.

This helps reduce the size of the final image and makes it more secure.

**Why do we use Multi-Stage Builds?**

1. Smaller images
2. Faster deployment
3. More secure
4. Cleaner Dockerfiles

Multi-stage builds = Big image for building + Small image for running.

---

### What are Distroless Images in Docker?

--> Normally, Docker images are built from a Linux distribution (like Ubuntu, Debian, Alpine).

That means they come with a lot of extra stuff:

* Shell (`/bin/bash`)
* Package managers (`apt`, `yum`)
* Utilities (`curl`, `vi`, etc.)

But for running an application in production, you don’t need all that. You only need:

* Your app
* Its dependencies

**Distroless images** are minimal Docker images **without a Linux distribution**.
They don’t have a shell or package manager — only the runtime environment (e.g., Java, Python, Node.js).

---

### Screenshot of Implementation

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/7e4774bfd53777ac21770cdc052eeb91752c5dc5/Day31/Day31%2001.jpg)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/7e4774bfd53777ac21770cdc052eeb91752c5dc5/Day31/Day31%2002.jpg)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/fd6cba1d380e3def2350c0d378f2b5bd1565dbbd/Day31/Day31%20Without%20Multistage.jpg)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/fd6cba1d380e3def2350c0d378f2b5bd1565dbbd/Day31/Day31%2004.jpg)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/fd6cba1d380e3def2350c0d378f2b5bd1565dbbd/Day31/Day31%2005.jpg)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/fd6cba1d380e3def2350c0d378f2b5bd1565dbbd/Day31/Day31%2003%20With%20Multistage.jpg)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/fd6cba1d380e3def2350c0d378f2b5bd1565dbbd/Day31/Day31%2006.jpg)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/fd6cba1d380e3def2350c0d378f2b5bd1565dbbd/Day31/Day31%2007.jpg)

---
