# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---
### Shell Scripting 01

**What is the purpose of scripting and automation?**
\--> Scripting and automation are fundamentals in IT, DevOps, Software Development, and System Administration. Their purpose is to save time, reduce errors, and improve efficiency by automating manual or repetitive tasks.

---

### Example of Use Cases

| Task         | Scripted Automation Example                               |
| ------------ | --------------------------------------------------------- |
| Server Setup | Install software, configure services, open firewall ports |
| Deployment   | Build code, run tests, deploy to staging/production       |
| Monitoring   | Health checks for services, disk space alerts             |

---

### What is the purpose of `#!/bin/bash` or `#!/bin/sh`?

\--> This line is called a **Shebang**, and it tells the system which interpreter to use when executing a script.

---

### vi Editor Commands

* `:q` → Quit (exit the editor)
* `:wq!` → Save and quit (force if needed)

---

### First Shell Script

```bash
#!/bin/bash
echo "My name is Laxman Adhikari"
```

---

### How to Run Shell Script Files?

1. `sh filename.sh`

   * Runs the script using `sh` shell no matter what’s written at the top.
   * Doesn’t need permission to run.

2. `./filename.sh`

   * Runs the script directly.
   * Uses the shell written at the top of the script (like `#!/bin/bash`).
   * Needs execution permission (`chmod +x filename.sh`).

---

### About chmod Command

* `chmod` → Grant permissions
* `ch` → Change

**chmod format**:

1. Which user
2. Which group
3. What permissions

**Permission values:**

* 4 → Read
* 2 → Write
* 1 → Execute

Example:

* `7` = 4 (read) + 2 (write) + 1 (execute)

---

### Simple Shell Script to Create a Folder & Two Files

```bash
#!/bin/bash

# create a folder
mkdir laxman

# create two files
cd laxman
touch firstfile secondfile
```

---

### Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/e52a7b916f0753e8da3a9bb90cf9681738b6f6d1/Day07/First%20Shell%20Script.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/e52a7b916f0753e8da3a9bb90cf9681738b6f6d1/Day07/First%20Shell%20Script%2002.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/e52a7b916f0753e8da3a9bb90cf9681738b6f6d1/Day07/Second%20Shell%20Script.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/e52a7b916f0753e8da3a9bb90cf9681738b6f6d1/Day07/Second%20Shell%20Script%2001.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/e52a7b916f0753e8da3a9bb90cf9681738b6f6d1/Day07/Second%20Shell%20Script%2002.png)

---
