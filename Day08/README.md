# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day08 Notes

### Shell Scripting 02

---

### Common Linux Commands

1. `df` → Show available disk space
2. `free` → Show memory usage of the machine
3. `nproc` → Show number of CPUs in the current machine
4. `top` → Show all information about current running processes

---

### Sample Script: Node Health Check

**Basic Version:**

```bash
#!/bin/bash

#######################
# Author: Laxman
# Date: 03/09/2025
# Description: This script outputs the node health
# Version: v1
#######################

echo "Print the disk space"
df -h 

echo "Print the memory"
free -g

echo "Print the CPU"
nproc
```

---

**With Debugging & Error Handling:**

```bash
#!/bin/bash

#######################
# Author: Laxman
# Date: 03/09/2025
# Description: Node health check with debug and error handling
# Version: v1
#######################

set -x   # Debug Mode (Show the commands and output)
set -e   # Exit the script if there is an error
set -o pipefail   # Catch errors in pipelines

df -h
free -g
nproc
```

---

### Process Management

**ps command**

* `ps` → Shows process status (information about running processes).
* `ps -ef` → Shows a full list of all running processes in **detailed format**.

| Option | Meaning                                                         |
| ------ | --------------------------------------------------------------- |
| `ps`   | Process status command                                          |
| `-e`   | Show **all** processes                                          |
| `-f`   | Show in **full format** (includes user, PPID, start time, etc.) |

**Example:**

```bash
ps -ef | grep "amazon"
```

* `ps -ef` → Lists all processes.
* `|` (pipe) → Sends output of left command to right command.
* `grep "amazon"` → Filters output to show only processes containing "amazon".

---

### awk Command

The `awk` command is used to read files or command output, split lines into columns, and process the data (print, filter, calculate, etc.).

**Example file: `file.txt`**

```
John  25  Developer
Amy   30  Designer
Tom   28  Manager
```

**Examples:**

1. Print the whole line:

   ```bash
   awk '{print $0}' file.txt
   ```

   ✅ Output:

   ```
   John 25 Developer
   Amy 30 Designer
   Tom 28 Manager
   ```

2. Print just the names (1st column):

   ```bash
   awk '{print $1}' file.txt
   ```

   ✅ Output:

   ```
   John
   Amy
   Tom
   ```

3. Print names and jobs:

   ```bash
   awk '{print $1, $3}' file.txt
   ```

   ✅ Output:

   ```
   John Developer
   Amy Designer
   Tom Manager
   ```

---

### Searching Errors in Logs

* **curl** → Retrieves information from the internet.
* **wget** → Downloads a file to the machine.

---

### Other Useful Commands

* `sudo su -` → Switch to root user.
* `find` → Search for files and folders in a directory (and subdirectories).
* Can search by **name, type, size, or date**.
* `trap` → Catch signals (e.g., script exit, `Ctrl+C`) and run custom commands.



### Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/0b0b46fc92e56d1100e6459498bdcad70a2451a5/Day08/Shell%20Script%2001%20Day08.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/0b0b46fc92e56d1100e6459498bdcad70a2451a5/Day08/Shell%20Script%2002%20Day08.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/0b0b46fc92e56d1100e6459498bdcad70a2451a5/Day08/Shell%20Script%2003%20Day08.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/0b0b46fc92e56d1100e6459498bdcad70a2451a5/Day08/Shell%20Script%2004%20ifelse%20Day08.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/0b0b46fc92e56d1100e6459498bdcad70a2451a5/Day08/Shell%20Script%2005%20ifelse%20Day08.png)

---
