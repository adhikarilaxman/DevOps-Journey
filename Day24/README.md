# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 24

### Creating First Pipeline with Jenkins

#### Jenkins Master and Worker Nodes

When you use Jenkins in a large setup, it does not run everything on one machine. Instead, it follows a **Master–Worker architecture**.

**1. Jenkins Master**

* The main server of Jenkins.
* It gives instructions and controls the whole system.
* **Responsibilities:**

  1. Schedule jobs (decide when/where a build will run).
  2. Distribute jobs to worker nodes.
  3. Monitor workers and collect results.
  4. Provide the web interface (UI).

**2. Jenkins Worker Nodes**

* Machines where the actual work (build, test, deploy) happens.
* Each worker node can be on a different machine/server.
* They follow the master’s instructions.
* **Responsibilities:**

  1. Run builds (e.g., compile code, run tests).
  2. Report results back to the master.

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Jenkins%20master%20to%20jenkins%20worker%20node.png)

---

### Jenkins Master with Docker Containers

* Normally, Jenkins runs jobs on worker nodes (physical or virtual machines).
* But instead of full servers, Jenkins can also use **Docker containers as workers**.

**1. Jenkins Master**

* Controls everything (job scheduling, pipeline definitions, UI).
* Decides where each job will run.

**2. Docker Plugin / Docker Agent**

* Jenkins can use Docker to create on-demand containers.
* Each container acts like a mini worker node.

**3. Docker Containers (Workers)**

* Instead of setting up full worker VMs, Jenkins launches lightweight Docker containers.
* **Example:**

  * Container 1 → Runs Node.js build
  * Container 2 → Runs Python tests
  * Container 3 → Runs Java Maven build

**4. After Job Finishes**

* The container is destroyed, providing a clean environment for the next job.

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Jenkins%20master%20to%20Docker%20containers.png)

---

### Two Types of Jobs in Jenkins

**1. Freestyle Project**

* The most basic type of Jenkins job.
* Provides a GUI (click-based setup) where you configure everything.
* No need to write code — just select options.

**Example Use Case**

* You want to build a simple Java project.
* **Steps:**

  1. Go to Jenkins → New Item → Freestyle Project.
  2. Add GitHub repo URL.
  3. Add build steps (e.g., `mvn clean install`).
  4. Save & Build.
* Jenkins will now pull the code, build it, and show results.

**When to Use?**

* For simple projects.
* When automation is minimal.
* When you prefer a UI-based setup instead of writing code.

---

**2. Pipeline**

* An advanced way to create jobs using code (**Jenkinsfile**).
* Instead of clicking buttons, you write a Groovy-based script.
* The Jenkinsfile defines all steps (build, test, deploy).

**Example Jenkinsfile**

```groovy
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building the project...'
      }
    }
    stage('Test') {
      steps {
        echo 'Running tests...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying the application...'
      }
    }
  }
}
```

**Example Use Case**

* You have a Node.js app.
* Jenkinsfile defines:

  1. Install dependencies (`npm install`)
  2. Run tests (`npm test`)
  3. Deploy (`npm run deploy`)

This provides automation + version control, since the Jenkinsfile lives inside the repo.

**When to Use?**

* For complex projects.
* When you need CI/CD pipelines.
* When you want everything defined as code (**Pipeline-as-Code**).

---

### My First Jenkins Pipeline

```groovy
pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
      }
    }
  }
}
```

---

### Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2001.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2002.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2003.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2004.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2005.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2006.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2007.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/20170f8f7ac2cea76267c608cf9058738ed6dd27/Day24/Day24%2008.jpg)

---
