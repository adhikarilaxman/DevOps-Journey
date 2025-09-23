---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 22

### CI/CD

**What is CI/CD?**

* **CI (Continuous Integration):** Developers frequently merge their code into a shared repository. Each merge is automatically tested and verified.
* **CD (Continuous Delivery/Deployment):** After CI passes, the code is automatically deployed to production (or staging), ensuring fast and reliable releases.

CI/CD is the pipeline (automated process) that takes code from developer → testing → deployment → production.

---

**Why CI/CD?**

* Faster development → Code changes are tested and deployed automatically.
* Fewer bugs → Every change is checked before release.
* Consistency → The same process is followed for every release.
* Confidence → Developers can release anytime without worrying about breaking things.

---

**Standard Steps in CI/CD Pipeline**

| **Step**                              | **Meaning**                                                                                                  | **Why it’s Important**                         |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| **1. Unit Testing**                   | Run small tests to check if each function/module works correctly.                                            | Detects errors early in code.                  |
| **2. Static Code Analysis**           | Analyze source code without running it (e.g., check for syntax errors, bad practices).                       | Improves code readability and maintainability. |
| **3. Code Quality / Vulnerabilities** | Tools check for **security issues** (like SQL injection, hardcoded passwords, etc.) and **quality metrics**. | Ensures secure and clean code.                 |
| **4. Automation**                     | Automate build, testing, and deployment processes.                                                           | Saves time and avoids manual mistakes.         |
| **5. Reports**                        | Generate reports of test results, code coverage, and analysis.                                               | Provides feedback to developers and managers.  |
| **6. Deployment**                     | Push the application to staging or production environment.                                                   | Delivers the final working app to users.       |

---

Do you want me to also prepare a **visual text-based CI/CD pipeline diagram** so you can easily include it in your notes?
