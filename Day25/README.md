# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 25

GitHub Actions 

GitHub Actions is a CI/CD (Continuous Integration / Continuous Deployment) service built directly into GitHub.

--> It allows you to automate workflies like 
1. Building Code
2. Running Tests
3. Scanning Vulnerabilities
4. Deploying apps to servers to cloud

Key Points about GitHub Actions:

1. Workflow

A set of automation rules written in a YAML file.

Stored in .github/workflows/ inside your repo.

2. Job

A unit of work (e.g., build, test, deploy).

Each job runs on a runner.

3. Runner

The environment (VM or container) where jobs execute.

GitHub provides free runners like Ubuntu, Windows, macOS, or you can use your own server.

4. Action

A reusable task in a workflow (e.g., checkout code, set up Node.js, run tests).

Available from GitHub Marketplace or custom-built.


--> Why use GitHub Actions?

1. Built-in with GitHub (no extra setup like Jenkins server).

2. Works cross-platform.

3. Free minutes for public repos.

4. Huge marketplace of prebuilt actions.

5. Easy integration with cloud providers (AWS, Azure, GCP).


--> Advantages of GitHub Actions Over Jenkins 

1. Hosting

Jenkins → You must install and manage it on your own server.

GitHub Actions → Already hosted by GitHub, no server setup needed.

2. User Interface

Jenkins → Powerful but complex, may feel overwhelming for beginners.

GitHub Actions → Simple, easy-to-use interface directly inside GitHub.

3. Cost

Jenkins → Costs time and money to maintain servers.

GitHub Actions → Free for public repos, affordable for private ones.

I have made one simple GitHub Actions 

1. I have fork the repository from
   https://github.com/iam-veeramalla/GitHub-Actions-Zero-to-Hero

   ![image alt]()


2. Made changes on addition.py
   ![image alt]()

3. As you can see all the jobs are running and executing that written on YAML file that is inside .github/worflows in the repo
   ![image alt]()
   ![image alt]()
  


