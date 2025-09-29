# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 26 

### CICD Interview Questions 

# Jenkins – Common Interview Questions and Answers (Simplified)

---

### Q: Can you explain the CI/CD process in your project?

**A:** Yes. In my project, we use Jenkins with tools like Maven, Sonar, AppScan, ArgoCD, and Kubernetes. The process has 8 steps:

1. **Code Commit:** Developers push code to GitHub.
2. **Build:** Jenkins builds the code using Maven and runs unit tests.
3. **Code Analysis:** Sonar checks for code quality issues, bugs, and vulnerabilities.
4. **Security Scan:** AppScan scans for security risks.
5. **Deploy to Dev:** If all checks pass, Jenkins deploys the app to Kubernetes (dev environment).
6. **Continuous Deployment:** ArgoCD automatically deploys new commits to the dev environment.
7. **Promote to Prod:** When ready, we manually promote to production using ArgoCD.
8. **Monitoring:** Kubernetes and monitoring tools track performance and availability.

---

### Q: What are the different ways to trigger Jenkins pipelines?

**A:** Pipelines can be triggered in many ways:

* **Poll SCM:** Jenkins checks Git repo at intervals for new commits.
* **Build Triggers (Git plugin):** Builds automatically when changes are pushed.
* **Webhooks:** GitHub notifies Jenkins immediately when code is pushed.

---

### Q: How do you back up Jenkins?

**A:** Backup important folders/files:

* `~/.jenkins` (main configuration)
* `plugins/` (all plugins)
* `jobs/` (job configs)
* Custom scripts/artifacts
* Database (if used)

Backups can be automated with cron jobs or task schedulers.

---

### Q: How do you handle secrets in Jenkins?

**A:** Ways to manage secrets:

* **Credentials Plugin:** Safely stores passwords, API keys, certificates.
* **Environment Variables:** Quick but less secure (visible in logs).
* **Vault Integration:** Use HashiCorp Vault or cloud secret managers (AWS, Azure, GCP).

---

### Q: What is the latest Jenkins version (or which version are you using)?

**A:** Interviewers want to see if you’re up to date. Always check the latest version before interviews.

---

### Q: What are shared modules in Jenkins?

**A:** Shared modules = reusable code/configurations across jobs. Examples:

* Shared libraries or scripts
* Common Jenkinsfile for multiple jobs
* Global variables (e.g., repo URLs, version numbers)
* Common plugins

---

### Q: Can Jenkins build apps with multiple languages using different agents?

**A:** Yes. Jenkins supports different agents for different stages.
Example:

* Agent 1: Build Java code
* Agent 2: Run Node.js tests
* Agent 3: Deploy using Python scripts
  This makes it flexible for multi-language projects.

---

### Q: How do you set up Jenkins with auto-scaling in AWS?

**A:** High-level steps:

1. Create an EC2 instance and install Jenkins.
2. Create a Launch Configuration with that setup.
3. Create an Auto Scaling Group with min/max instance count.
4. Add Scaling Policies (based on CPU/memory).
5. Attach a Load Balancer to distribute traffic.
6. Monitor with CloudWatch.

This ensures Jenkins scales automatically with load.

---

### Q: How to add a new worker node in Jenkins?

**A:** Go to **Manage Jenkins → Manage Nodes → New Node**, enter details, configure SSH, and launch.

---

### Q: How to install a new plugin in Jenkins?

**A:**

* **UI:** Manage Jenkins → Manage Plugins → Install.
* **CLI:** `java -jar jenkins-cli.jar install-plugin <PLUGIN_NAME>`

---

### Q: What is JNLP in Jenkins?

**A:** JNLP (Java Network Launch Protocol) is used for connecting Jenkins agents (worker nodes) to the master remotely. Agents receive tasks from the master and send results back.

---

### Q: What are some common plugins you use in Jenkins?

**A:** Be ready with 3–4 examples:

* Git Plugin (connect GitHub/GitLab)
* Maven/Gradle Plugin (build tools)
* Pipeline Plugin (define CI/CD pipelines)
* SonarQube Plugin (code quality)
* Docker Plugin (build/test inside containers)

---
