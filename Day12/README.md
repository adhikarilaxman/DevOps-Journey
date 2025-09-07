# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 12 Notes

### Networking Concepts

---

### IP Address

* An **IP Address** is a unique number given to a device connected to a network.
* It helps identify and communicate with that device.
* Format: **4 bytes (32 bits)** → ranges from `0–255`.

---

### IPv4

* **IPv4 (Internet Protocol Version 4)** is the most widely used system for identifying devices on a network.

---

### Subnet

* A **Subnet** is like a smaller group inside a larger network.
* It divides a big network into smaller, manageable networks.

✅ **Advantages of Subnetting:**

1. Security
2. Privacy
3. Isolation

**Types of Subnets:**

* **Private Subnet** → Does not have access to the Internet.
* **Public Subnet** → Has access to the Internet.

---

### CIDR

* **CIDR (Classless Inter-Domain Routing)** is a method for allocating IP addresses.
* It helps improve data routing efficiency on the Internet.

---

### Port Number

* A **Port Number** is a **16-bit identifier** used to specify a particular application or process on a device.
* Example: Port `80` for HTTP, Port `443` for HTTPS.

---

### DNS

* **DNS (Domain Name System)** is the **phonebook of the Internet**.
* It converts domain names (like `google.com`) into IP addresses so browsers can connect to websites.

---

### OSI Model (Open Systems Interconnection)

* The **OSI Model** explains how computers communicate over a network.
* It has **7 layers**, and each layer has a specific role.

---

#### 1. Physical Layer (Layer 1)

* Handles the **hardware** part (wires, routers, Wi-Fi signals).
* Example: Ethernet cable, Wi-Fi signal.

#### 2. Data Link Layer (Layer 2)

* Ensures data moves correctly between two devices on the same network.
* Example: Ethernet protocol, Wi-Fi protocol.

#### 3. Network Layer (Layer 3)

* Finds the **best path** for data across networks.
* Example: IP address.

#### 4. Transport Layer (Layer 4)

* Ensures data arrives **in order** and without errors.
* Example: TCP (Transmission Control Protocol).

#### 5. Session Layer (Layer 5)

* Manages **sessions** between two computers.
* Example: Keeps a Zoom call open until you end it.

#### 6. Presentation Layer (Layer 6)

* Formats, encrypts, or compresses data so the receiver can understand it.
* Example: JPEG (images), MP4 (videos), data encryption.

#### 7. Application Layer (Layer 7)

* The layer users **directly interact with**.
* Example: Browsers (Chrome), email apps, messaging apps.

---

### Easy Analogy → Sending a Letter

* **Physical Layer**: The paper & envelope.
* **Data Link Layer**: The local post office sorting letters.
* **Network Layer**: The address on the envelope.
* **Transport Layer**: The postman making sure the letter arrives safely.
* **Session Layer**: Knowing where to pick up & drop off letters.
* **Presentation Layer**: The letter written in a readable language or code.
* **Application Layer**: The actual contents of the letter the recipient reads.

---

✅ Each layer plays a special role, and together they make sure data moves smoothly across networks!

---
