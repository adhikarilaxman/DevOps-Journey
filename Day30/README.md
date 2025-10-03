---

# DevOps – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 30

### Docker Containerization for Django

1. **Clone the repository** into the EC2 instance:

   ```
   https://github.com/iam-veeramalla/Docker-Zero-to-Hero.git
   ```

   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/d5e961d42858bd99d65248f88cf2c9c70a003bd2/Day30/Day30%2001.jpg)

2. Navigate to the project directory:

   ```
   cd example/python-web-app
   ```

3. **Build the Docker image** using the `docker build` command:

   ```
   docker build -t my-django-app .
   ```

   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/d5e961d42858bd99d65248f88cf2c9c70a003bd2/Day30/Day30%2002.jpg)

4. After building, you can see your image available:
   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/d5e961d42858bd99d65248f88cf2c9c70a003bd2/Day30/Day30%2003.jpg)

5. **Run the Docker container**:

   ```
   docker run -p 8000:8000 -it <IMAGE_ID>
   ```

   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/d5e961d42858bd99d65248f88cf2c9c70a003bd2/Day30/Day30%2004.jpg)

6. Open your browser → enter your EC2 server’s IP address followed by port `8000`.
   Example:

   ```
   http://<EC2-Public-IP>:8000
   ```

   You should now see your Django app running.
   ![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/d5e961d42858bd99d65248f88cf2c9c70a003bd2/Day30/Day30%2005.jpg)

---

**Note:**
Make sure you update the **Inbound Rules** of your EC2 security group to allow traffic on port **8000**.
![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/d5e961d42858bd99d65248f88cf2c9c70a003bd2/Day30/Day30%2006.jpg)

---
