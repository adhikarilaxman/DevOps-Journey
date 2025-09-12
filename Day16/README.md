---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Deploying a Node.js Application on AWS EC2

### Steps

**Step 1:** Create an EC2 instance from AWS.

**Step 2:** Install Git (if not already installed) on the VM.

**Step 3:** Install Node.js and npm.
--> [Guide – Install Node.js on Ubuntu 22.04](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-22-04)

**Step 4:** Clone the repository from your GitHub account.

**Step 5:** Navigate to the cloned project directory.

**Step 6:** Initialize and start the project:

```bash
npm install
npm run start
```

**Step 7:** Your web app will run on **port 3000** by default.

**Step 8:** Open your browser and enter your **public IP address with the port number**.
 Example: `http://<Public-IPv4>:3000`

**Step 9:** At this point, the application may not load because the **security group** is not configured.

**Step 10:** Go to **Security** settings of your EC2 instance.

**Step 11:** Navigate to **Inbound Rules → Edit inbound rules**.

**Step 12:** Add a new rule:

* **Type:** Custom TCP
* **Port Range:** 3000
* **Source:** Anywhere-IPv4

**Step 13:** Reload the page. ✅ Your Node.js application should now be successfully deployed on the AWS EC2 instance.

---

## Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2001.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2002.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2003.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2004.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2005%20install%20git.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2006%20git%20clone%20the%20repo.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2007%20install%20nodejs.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2008.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2009%20npm%20install.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2010%20npm%20start.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2011.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2012.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2013%20Edit%20inbound%20rules.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2013%20Edit%20inbound%20rules.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2014%20Add%20rules.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2015.png)
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/adafcfbf1c8012d9e10df93341e38e828adc2d58/Day16/Day16%2016%20nodejs%20app%20is%20running.png)

---
