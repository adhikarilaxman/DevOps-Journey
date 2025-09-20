---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Ansible

### What is Ansible?

Ansible is an **IT automation tool** maintained by **Red Hat**.
It is built using **Python** and is widely used for automating IT tasks like configuration management, application deployment, and orchestration.

---

### Why Do We Need to Automate?

 Without automation:
If we want to download and install software on multiple servers, we need to **manually log in to each server (via SSH)** and install one by one.

* This is **time-consuming**.
* High chances of **human error**.

![Without Ansible](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Without%20Ansible%20SSH.png)

 With Ansible:

* We install Ansible only on **one control server**.
* Write configurations in **Inventory files** and **Playbooks**.
* Ansible then **pushes tasks** to all other servers automatically.

![With Ansible](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/With%20Ansible%20SSH.png)

---

### Example Playbook (YAML File)

```yaml
---
- name: Install and Start nginx
  hosts: all
  become: yes
  become_user: root

  tasks:
    - name: Install nginx
      apt:
        name: nginx
        state: present

    - name: Start nginx
      service:
        name: nginx
        state: started
```

 This playbook will:

1. Install **nginx** on all servers.
2. Start the **nginx service**.

---

### Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2001.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2002.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2003.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2004.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2005.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2006.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2007.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2008.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2009.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2010.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2011.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2012.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2013.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2014.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2015.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2016.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/a1ce94e7f429fba0220e02b28f1119f1eed28141/Day19/Day%2019%2017.png)

---
better?
