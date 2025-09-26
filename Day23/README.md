---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 23

### Installation of Jenkins

**Step 1** – Launch an Ubuntu EC2 Instance

**Step 2** – Update the machine using this command:

```bash
sudo apt update
```

**Step 3** – Jenkins is a Java-based application, so install Java first:

```bash
sudo apt install default-jre
```

**Step 4** – Install Jenkins with these commands:

```bash
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update
sudo apt install jenkins
```

**Step 5** – Verify Jenkins is running:

```bash
ps -ef | grep jenkins
```

**Step 6** – By default, Jenkins runs on port **8080**, but AWS blocks incoming ports by default. You need to allow port **8080** in the inbound rules.

**Step 7** – To edit inbound rules:

* Go to **Security → Security Groups**
* Click on your **launch-wizard-18** group
* Select **Security Group ID**
* Click **Edit inbound rules**
* Add a new rule → Port **8080** → Save

**Step 8** – Copy the public IP address of your EC2 instance and paste it in the browser with `:8080`.

**Step 9** – Jenkins should now be running successfully. ✅

Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2001.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2002.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2003.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2004.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2005.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2006.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2007.jpg)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/13338b08a896d6552b62868dba74b2793af1aad0/Day23/Day23%2008.jpg)

---


