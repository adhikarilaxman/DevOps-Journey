---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 34

### Docker Interview Questions with Answers

1. **What is Docker?**
2. 
   --> Docker is an open-source containerization platform. It enables developers to package applications and their dependencies into containers, ensuring consistency across different environments.

---

2. **How are containers different from virtual machines?**

| Feature        | Containers               | Virtual Machines       |
| -------------- | ------------------------ | ---------------------- |
| **OS**         | Share the host OS kernel | Have their own OS      |
| **Size**       | Lightweight (MBs)        | Heavy (GBs)            |
| **Speed**      | Start in seconds         | Start in minutes       |
| **Efficiency** | Uses fewer resources     | High resource usage    |
| **Use Case**   | Microservices, CI/CD     | Full OS virtualization |

---

3. **What is the Docker lifecycle?**
4. 
   --> The Docker container lifecycle includes these stages:

5. **Create** – Create a new container from an image.

6. **Start** – Run the container.

7. **Pause/Unpause** – Temporarily stop/resume processes inside the container.

8. **Stop** – Gracefully stop the container.

9. **Kill** – Forcefully terminate the container.

10. **Remove (rm)** – Delete the container permanently.

---

4. **What are the different Docker components?**


   -->  * **Docker Engine** – Core part (includes Daemon and CLI).
     * **Docker Daemon (dockerd)** – Background service that manages images, containers, and networks.
    * **Docker CLI** – Command-line interface to interact with Docker.
    * **Docker Images** – Blueprints for containers.
    * **Docker Containers** – Running instances of images.
    * **Docker Hub/Registry** – Cloud storage for sharing images.

---

5. **What is the difference between COPY and ADD in Docker?**

| Command  | Description                                                                                                                   |
| -------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **COPY** | Copies files/folders from the host to the image.                                                                              |
| **ADD**  | Does everything `COPY` does **plus** supports: <br> - Downloading from URLs <br> - Extracting compressed files automatically. |

---

6. **What is the difference between CMD and ENTRYPOINT?**

| Feature         | CMD                                     | ENTRYPOINT                        |
| --------------- | --------------------------------------- | --------------------------------- |
| **Purpose**     | Sets default command                    | Defines the main executable       |
| **Overridable** | Yes (can be overridden in `docker run`) | Not easily overridden             |
| **Example**     | `CMD ["npm", "start"]`                  | `ENTRYPOINT ["python", "app.py"]` |

---

7. **What are the networking types in Docker and what is the default?**

| Type                 | Description                                                   |
| -------------------- | ------------------------------------------------------------- |
| **Bridge (default)** | Connects containers on the same host using a virtual network. |
| **Host**             | Shares the host’s network directly.                           |
| **None**             | No networking.                                                |
| **Overlay**          | Connects containers across multiple hosts (used in Swarm).    |
| **Macvlan**          | Assigns containers their own MAC address (like real devices). |
 **Default:** Bridge Network

---

8. **How to isolate networking between containers?**
9. 
   --> Use **user-defined bridge networks** instead of the default bridge.
   Containers on different networks **cannot communicate** unless connected explicitly.

---

9. **What is a multi-stage build in Docker?**
10. 
   --> Multi-stage builds use **multiple FROM statements** in a Dockerfile to separate build and runtime environments.
   This helps create **smaller, faster, and more secure images** by copying only the final build artifacts into the final image.

---

10. **What are distroless images in Docker?**
    --> Distroless images are **minimal images** that contain only the application and its dependencies — no shell, package manager, or OS utilities.
    They are **more secure and smaller** than normal base images.

---

11. **What are real-time challenges faced with Docker?**
  

  -->  * Large image sizes → slow deployment.
       * Networking conflicts (port collisions).
       * Security vulnerabilities in base images.
       
---

12. **What steps would you take to secure the container?**


-->  * Use official and verified images.
     * Regularly scan images for vulnerabilities.
     * Use non-root users in containers.


---

Would you like me to make the next section (**Day 35**) about *Docker Compose* — its concept, YAML structure, and implementation?
