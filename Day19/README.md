---
# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

Ansible 

What is Ansible?
--> Ansible is an IT Automation tool which is maintain by redhat it is made by python.

Why do we need to Automate?
--> If we want to download & install any software into machine we have to manually login to each server (SSH) and downaload & install one by one. This approach was time consuming and chances of making error.
    Ansible make this task in efficent way.
    ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/4c72efed99934375abfde685473e64eb0adb580e/Day15/Day%2015%2001.png)

--> We have to install ansible on only one server and we have to write configuration like inventory files and playbooks then all the others server will task will completed.
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/4c72efed99934375abfde685473e64eb0adb580e/Day15/Day%2015%2001.png)


YAML File 
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



Screenshots 

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
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()

