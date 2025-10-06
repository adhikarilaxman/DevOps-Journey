---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 33

### Docker Networking

Why you need networking on Docker?

--> Docker networking is needed so that containers can communicate with:
Each other (e.g., a web app container talking to a database container).

1. The host machine (to access files or APIs)
2. The outside world (internet access or users accessing your app).

Without networking, containers would be isolated and unable to share data or services.

How does Docker Networking Work?

--> When we start Docker, it automatically creates a virtual network on your host.

* Each container gets its own virtual network interface and IP address.
* Docker uses network drivers (like bridge, host, none, overlay, macvlan) to connect containers internally and externally.

**Bridge Network**

* The default Docker network — used when containers run on the same host.
* Docker creates a virtual bridge.
* Each container gets its own internal IP address.

**Host Network**

* The container shares the host’s network directly — no isolation.
* The container uses the same network interface and IP as the host.
* No separate IP for the container.

**Overlay Network**

* Used to connect containers running across multiple Docker hosts.
* Creates a virtual network that spans multiple machines.
* Ideal for distributed systems or microservices across servers.

**Screenshots of Implementation**

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

---
