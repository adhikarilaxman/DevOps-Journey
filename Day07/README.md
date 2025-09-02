---
# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

Shell Scripting 01

What is the purpose of scripting and automation?
--> Scripting and automation are fundamentals in IT, DevOps, Software Devlopment and system adminstration. Their purpose is to save time, reduce errors, and improve efficency by automating manual or repetitve task.

Example of Use Cases

Task                                      Scripted Automation
----------------------------------------------------------------------------------------------------
1. Server setup                          install software, configure service, open firewall ports.
2. Deployment                            Build code, run test to staging/production.
3. Monitoring                            Health checks for services, disk space alerts.


What is the purpose of #!/bin/bash or #!bin/sh?
--> The line is called "Shebang", and it tells the system which interpreter to use when executing a script.

:q, :wq!

-! --> puts you into command mode.
-w --> stands for write(save).
-q --> stands for quit (exit the editor).
-! --> means force.

First Shell Script 
--> #!/bin/bash
    echo "My name is Laxman Adhikari"

How to Run Shell Script files?
1. sh filename.sh
2. ./filename.sh

Sh
--> Runs the script using sh shell no matter what's written at the top.
--> Doesn't need permission to run.

./
--> Runs the script directly.
--> Uses the shell written at the top of the script (like #!/bin/bash).
--> Need permission to run (chmod +x filename.sh).

About Chmod Command

--> Chmod --> Grant Permission.
--> ch -->Change


chmod -- 1. Which user
         2. Which Group
         3. What are your permission

    7 --> 4 --> Read
          2 --> Write
          1 --> Execute
Simple Shell Script to Create a folder & Create two files.

#!bin/bash

#create a folder
mkdir laxman

#create two files 
cd laxman
touch firstfile secondfile


![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/b0010568f7c0d175b3012a1e6618d4b49947863d/Day02/Phases.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/b0010568f7c0d175b3012a1e6618d4b49947863d/Day02/Phases.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/b0010568f7c0d175b3012a1e6618d4b49947863d/Day02/Phases.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/b0010568f7c0d175b3012a1e6618d4b49947863d/Day02/Phases.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/b0010568f7c0d175b3012a1e6618d4b49947863d/Day02/Phases.png)
