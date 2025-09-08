# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 13 Notes

### Git and GitHub

---

### What is Version Control System (VCS)?

\--> A Version Control System (VCS) is a tool that helps developers **track, manage, and control changes** to code or files over time.

---

### Types of Version Control

```
Version Control
|
|--> CVS   | --> Centralized
|--> SVN   | --> Centralized
|--> GIT   | --> Distributed
```

---

### Centralized VCS (CVCS)

* In Centralized VCS, there is **one central server** that stores the project history.
* Developers connect to this server to get the latest version of code.
* If the server goes down, **nobody can collaborate until it’s back**.
* **Examples:** SVN (Subversion), CVS

---

### Distributed VCS (DVCS)

* In Distributed VCS, **every developer has a complete copy** of the entire project history on their own computer.
* Developers can **work offline** and later sync with others.
* Even if the main server goes down, **anyone’s copy can restore the project**.
* **Examples:** Git, Mercurial

---

### What is a Fork in GitHub?

\--> A **fork** is a personal copy of someone else’s repository.

When you fork a repo on GitHub:

* It creates a **copy under your account**.
* You can make changes in your fork without affecting the original project.
* Later, you can send your changes back to the original repo via a **Pull Request (PR)**.

---

### Difference Between Git and GitHub

\-->
![Difference between Git and GitHub](https://github.com/adhikarilaxman/DevOps-Journey/blob/c9437c74f12b766c34d51dd308937e72b330b26a/Day13/Day13%2003.png)

---

### Some Git Commands

1. `git status` – Show the current state of your repo
2. `git add .` – Stage all changes
3. `git log` – Show commit history
4. `git commit -m "Initial Commit"` – Save changes with a message
5. `git reset --hard` – Go to a previous version (discard changes)

---

### Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/c9437c74f12b766c34d51dd308937e72b330b26a/Day13/Day13%2001.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/c9437c74f12b766c34d51dd308937e72b330b26a/Day13/Day13%2002.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/c9437c74f12b766c34d51dd308937e72b330b26a/Day13/Day13%2004.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/c9437c74f12b766c34d51dd308937e72b330b26a/Day13/Day13%2005.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/c9437c74f12b766c34d51dd308937e72b330b26a/Day13/Day13%2006.png)

---
