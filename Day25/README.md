# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 25

### GitHub Actions

GitHub Actions is a CI/CD (Continuous Integration / Continuous Deployment) service built directly into GitHub.

It allows you to automate workflows such as:

1. Building code
2. Running tests
3. Scanning vulnerabilities
4. Deploying apps to servers or cloud

---

### Key Points about GitHub Actions

1. **Workflow**

   * A set of automation rules written in a YAML file.
   * Stored in `.github/workflows/` inside your repository.

2. **Job**

   * A unit of work (e.g., build, test, deploy).
   * Each job runs on a runner.

3. **Runner**

   * The environment (VM or container) where jobs execute.
   * GitHub provides free runners like Ubuntu, Windows, macOS, or you can use your own server.

4. **Action**

   * A reusable task in a workflow (e.g., checkout code, set up Node.js, run tests).
   * Available from GitHub Marketplace or can be custom-built.

---

### Why Use GitHub Actions?

1. Built-in with GitHub (no extra setup like a Jenkins server).
2. Works cross-platform.
3. Free minutes for public repositories.
4. Huge marketplace of prebuilt actions.
5. Easy integration with cloud providers (AWS, Azure, GCP).

---

### Advantages of GitHub Actions Over Jenkins

1. **Hosting**

   * Jenkins → You must install and manage it on your own server.
   * GitHub Actions → Already hosted by GitHub, no server setup needed.

2. **User Interface**

   * Jenkins → Powerful but complex, may feel overwhelming for beginners.
   * GitHub Actions → Simple, easy-to-use interface directly inside GitHub.

3. **Cost**

   * Jenkins → Costs time and money to maintain servers.
   * GitHub Actions → Free for public repositories, affordable for private ones.

---

### My First GitHub Actions Workflow

1. Forked the repository from:
   [GitHub-Actions-Zero-to-Hero](https://github.com/iam-veeramalla/GitHub-Actions-Zero-to-Hero)
   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2001.jpg)

2. Made changes in `addition.py`:
   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2002%20.jpg)

3. As you can see, all the jobs are running and executing as defined in the YAML file inside `.github/workflows/`:
   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2003.jpg)
   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2004.jpg)

---

### GitHub Actions Self-Hosted Runners

Self-hosted runners operate on your own infrastructure, whether on-premises or in the cloud.

We need to set up **Inbound** and **Outbound** rules in our EC2 instance.

* **Inbound Rules**
  ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2005%20Inbound%20Rules.jpg)

* **Outbound Rules**
  ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2006%20Outbound%20Rules.jpg)

Next, go to:
**Repository → Actions → Runners → Add new self-hosted runner**
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2007.jpg)

Copy the commands onto the EC2 instance:
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2008.jpg)

Finally, update the YAML file from **ubuntu runner** to **self-hosted runner**:
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2009.jpg)

Now, jobs run on self-hosted runners (EC2 instance) and communicate directly with your GitHub account.
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/48c0bac934a5554ecd2cb41bfdc00908aca53b3a/Day25/Day25%2010.jpg)

---
