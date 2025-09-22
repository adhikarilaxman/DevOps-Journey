---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 21

### Terraform - Making EC2 Instance

#### What is Terraform?

\--> Terraform is an IAC tool, used primarily by DevOps teams to automate various infrastructure tasks.

#### What is state file in Terraform?

\--> State file maintains track of your entire infrastructure (e.g., .tf files). By default, the state file is stored locally in the same directory as your Terraform configuration.

---

### Steps to Install Terraform on Ubuntu

1. Add the HashiCorp GPG key to your system:

   ```bash
   curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
   ```

2. Add the official HashiCorp Terraform Linux repository to apt:

   ```bash
   sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
   ```

3. Update apt and install Terraform:

   ```bash
   sudo apt-get update && sudo apt-get install terraform
   ```

4. Verify installation:

   ```bash
   terraform -v
   ```

---

### Configure AWS CLI (Required before running Terraform file)

1. Install unzip:

   ```bash
   sudo apt install unzip
   ```

2. Download and install AWS CLI:

   ```bash
   curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
   unzip awscliv2.zip
   sudo ./aws/install
   ```

3. Verify AWS CLI installation:

   ```bash
   aws --version
   ```

4. Configure AWS credentials:

   ```bash
   aws configure
   ```

   Provide the following details from your AWS Account (IAM):

   * AWS Access Key ID \[None]:
   * AWS Secret Access Key \[None]:
   * Default region name \[None]:
   * Default output format \[None]:

---

### Create EC2 Instance using Terraform

1. Create a file:

   ```bash
   vim main.tf
   ```

2. Paste the following HCL code in `main.tf`:

   ```hcl
   terraform {
     required_providers {
       aws = {
         source  = "hashicorp/aws"
         version = "~> 4.16"
       }
     }
     required_version = ">= 1.13.3"
   }

   provider "aws" {
     region = "us-west-2"
   }

   resource "aws_instance" "app_server" {
     ami           = "ami-830c94e3"
     instance_type = "t2.micro"

     tags = {
       Name = "Terraform_Demo"
     }
   }
   ```

3. Initialize Terraform:

   ```bash
   terraform init
   ```

4. Dry run to preview changes:

   ```bash
   terraform plan
   ```

5. Apply the configuration:

   ```bash
   terraform apply
   ```

6. Go to the **us-west-2** region in AWS Console. You will see the EC2 instance running successfully.

---

### Screenshots

![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()


---
