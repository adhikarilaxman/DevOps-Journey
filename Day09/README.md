---

# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day09 Notes

### Shell Scripting 03 – Interview Questions

---

**Q1. List some of the commonly used Linux commands.**

* ls
* cp
* mv
* mkdir
* touch
* vim
* grep
* find
* df
* nproc

---

**Q2. Write a simple shell script to list all processes.**

```bash
ps -ef
ps -ef | awk -F " " '{print $2}'
```

---

**Q3. Write a script to print only errors from a remote log.**

```bash
curl <link_of_log_file> | grep ERROR
```

---

**Q4. Write a shell script to print numbers divisible by 3 and 5, but not 15.**

```bash
#!/bin/bash

for i in {1..100}
do
    if { [ $((i % 3)) -eq 0 ] || [ $((i % 5)) -eq 0 ]; } && [ $((i % 15)) -ne 0 ]; then
        echo $i
    fi
done
```

---

**Q5. Write a script to print the number of "s" in *mississippi*.**

```bash
#!/bin/bash
x=mississippi
grep -o "s" <<< "$x" | wc -l
```

---

**Q6. How will you debug a shell script?**

* Add `set -x` in your script to enable debug mode.

---

**Q7. What is Crontab in Linux? Provide an example.**

* **Crontab** is a tool in Linux used to run tasks automatically at specific times.

Example: Run a backup script every day at midnight

```bash
0 0 * * * /home/user/backup.sh
```

---

**Q8. How to open a read-only file in Linux?**

```bash
vim -R test.txt
```

---

**Q9. Difference between Soft Link and Hard Link.**

* **Soft Link (Symbolic Link):**

  * Like a shortcut to another file.
  * Points to the file name.
  * If the original file is deleted, the link breaks.

* **Hard Link:**

  * Like a duplicate reference to the actual file data.
  * Points directly to the file’s data (inode).
  * Still works even if the original file is deleted.

---

**Q10. Difference between `break` and `continue`.**

* `break` → Exits the loop completely.
* `continue` → Skips the current iteration and continues with the next one.

---

**Q11. What are some disadvantages of shell scripting?**

1. Hard to debug (errors are not always clear).
2. Slow for large/complex tasks.
3. Security risks if not written carefully.
4. Limited error handling.
5. Not portable across all systems (different shells, commands).
6. Can be difficult to read and maintain in long scripts.

---

**Q12. What are the different types of loops in shell scripting?**

* **for loop** → When the number of iterations is known.
* **while loop** → Runs while a condition is true.
* **until loop** → Runs until a condition becomes true.

---

**Q13. Is Bash dynamically or statically typed? Why?**

* Bash is **dynamically typed** because variable types are determined at runtime, not declared beforehand.

---

**Q14. Explain a network troubleshooting utility.**

| Tool         | Use Case                                        |
| ------------ | ----------------------------------------------- |
| ping         | Check if a network device is reachable          |
| traceroute   | Trace the route packets take across the network |
| netstat      | View active connections and statistics          |
| nslookup/dig | Resolve domain names to IP addresses            |
| ifconfig/ip  | View or configure network interfaces            |

---

**Q15. How will you sort a list of names in a file?**

```bash
sort names.txt               # Alphabetical sort
sort -r names.txt            # Reverse sort
sort -f names.txt            # Case-insensitive sort
sort -u names.txt            # Sort and remove duplicates
sort names.txt -o sorted.txt # Sort and save to a new file
```

---

**Q16. How will you manage logs on a system that generates huge files every day?**

* **Log Rotation** → Use `logrotate` to rotate logs by size or time.
* **Log Cleanup** → Use cron jobs to delete/archive old logs.
* **Log Compression** → Compress old logs to save disk space.
* **Archiving** → Move old logs to another directory/server.
* **Monitoring** → Use `logwatch` to track log health.
* **Centralized Logging** → Send logs to a remote log server (e.g., ELK stack).

---
