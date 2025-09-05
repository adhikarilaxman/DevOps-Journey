# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day10 Notes

### AWS Project using Shell Scripting for DevOps

---

### What is Crontab?

Crontab in Linux is a tool that helps you **automatically run commands or scripts at specific times**.
You can use it to schedule tasks like backups, cleanups, or running programs without doing them manually.

---

### Shell Script to Report AWS Resource Usage

```bash
#!/bin/bash

####################
# Author: Laxman
# Date: 05/09/2025
# Version: v1
# Description: This script reports AWS resource usage
####################

# AWS S3
# AWS EC2
# AWS Lambda
# AWS IAM Users

# List S3 Buckets
echo "Print list of S3 buckets"
aws s3 ls

# List EC2 Instances
echo "Print list of EC2 instances"
aws ec2 describe-instances

# List AWS Lambda Functions
echo "Print list of Lambda functions"
aws lambda list-functions

# List IAM Users
echo "Print list of IAM Users"
aws iam list-users
```

---
What is jq?

jq is a command-line tool used to process and format JSON data.
Think of it as grep, sed, or awk — but specifically for JSON.

What is yq?

yq is a command-line processor for YAML files, just like jq is for JSON.

It’s super useful in DevOps, especially when working with Kubernetes manifests, Ansible playbooks, or CloudFormation YAML templates.


### To Display Only EC2 Instance IDs

```bash
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'
```

### Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/59d90fa37c2fa4080e1e762f797bba8695bfe1a1/Day10/Day10%2001.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/59d90fa37c2fa4080e1e762f797bba8695bfe1a1/Day10/Day10%2002.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/59d90fa37c2fa4080e1e762f797bba8695bfe1a1/Day10/Day10%2003.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/59d90fa37c2fa4080e1e762f797bba8695bfe1a1/Day10/Day10%2004.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/59d90fa37c2fa4080e1e762f797bba8695bfe1a1/Day10/Day10%2005.png)

---
