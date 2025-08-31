---

# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---
### Amazon CLI (Command Line Interface)

The AWS CLI (Command Line Interface) is a tool that lets you interact with Amazon Web Services directly from your command line (Terminal, PowerShell, or CMD).

---

### Key Points

* It is open-source and supported on Windows, macOS, and Linux.
* Provides direct access to AWS services like EC2, S3, IAM, Lambda, etc.
* Useful for automation (writing scripts instead of clicking in the console).
* Often used in DevOps pipelines with CI/CD.

---

### Example Commands

```bash
# Check AWS CLI version
aws --version

# Configure AWS credentials
aws configure

# List all S3 buckets
aws s3 ls

# Launch a new EC2 instance
aws ec2 run-instances --image-id ami-12345678 --count 1 --instance-type t2.micro --key-name MyKeyPair --security-groups MySecurityGroup
```

---

### How to Install and Configure AWS CLI

#### 1. Install AWS CLI

**On Windows**

* Download the MSI installer from the official AWS link: [AWS CLI v2 Windows Installer](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
* Run the installer.
* Verify installation:

  ```bash
  aws --version
  ```

---

#### 2. Configure AWS CLI

Once installed, you need to set up your credentials:

```bash
aws configure
```

It will ask for:

* **AWS Access Key ID** → From your AWS IAM user
* **AWS Secret Access Key** → From your AWS IAM user
* **Default region name** → Example: `us-east-1` or `ap-south-1` (Mumbai)
* **Default output format** → `json` (you can also use `table` or `text`)

---

#### 3. Test AWS CLI

```bash
# Check current configuration
aws configure list

# List S3 buckets
aws s3 ls

# Describe EC2 instances
aws ec2 describe-instances
```

---
