# AWS EC2 Nginx Portfolio Deployment

## 📌 Project Overview

This project demonstrates how to deploy a personal portfolio website on an AWS EC2 Ubuntu instance using the Nginx web server. The website is hosted on a cloud server and can be accessed using the EC2 Public IP address.

---

## 🚀 Features

- Deploy Portfolio Website on AWS EC2
- Configure Ubuntu Server
- Install and Configure Nginx
- Host Static Website
- Access Website using Public IP
- Version Control using Git & GitHub

---

## 🛠 Technologies Used

- AWS EC2
- Ubuntu 24.04 LTS
- Nginx
- HTML5
- CSS3
- JavaScript
- Git
- GitHub
- Linux Commands

---

## 📂 Project Structure

```
aws-ec2-nginx-portfolio-deployment
│
├── Portfolio-profile
│   ├── index.html
│   ├── image
│   └── assets
│
├── screenshots
│
└── README.md
```

---

# Step 1 : Launch EC2 Instance

- Login to AWS Console
- Open EC2 Dashboard
- Launch Ubuntu Instance
- Select t2.micro
- Create Key Pair
- Configure Security Group
    - SSH (22)
    - HTTP (80)

---

# Step 2 : Connect to EC2

```bash
ssh -i portfolio-key.pem ubuntu@YOUR_PUBLIC_IP
```

---

# Step 3 : Update Ubuntu

```bash
sudo apt update
sudo apt upgrade -y
```

---

# Step 4 : Install Nginx

```bash
sudo apt install nginx -y
```

Check Status

```bash
sudo systemctl status nginx
```

Enable Nginx

```bash
sudo systemctl enable nginx
```

---

# Step 5 : Clone Portfolio Project

```bash
git clone https://github.com/gauriwaydande/myportfoliowebsite.git
```

---

# Step 6 : Copy Website Files

```bash
sudo rm -rf /var/www/html/*
sudo cp -r Portfolio-profile/* /var/www/html/
```

---

# Step 7 : Restart Nginx

```bash
sudo systemctl restart nginx
```

---

# Step 8 : Access Website

Open Browser

```
http://YOUR_PUBLIC_IP
```

Portfolio Website will be displayed successfully.

---

## 📷 Screenshots

### EC2 Instance Running

(Add Screenshot)

### Ubuntu Terminal

(Add Screenshot)

### Nginx Welcome Page

(Add Screenshot)

### Portfolio Website Running

(Add Screenshot)

### GitHub Repository

(Add Screenshot)

---

## 📈 Learning Outcome

- AWS EC2 Launch
- Ubuntu Linux Basics
- Nginx Installation
- Website Deployment
- GitHub Repository Management
- Linux Commands

---

## 🔧 Future Enhancements

- HTTPS using SSL
- Custom Domain
- Docker Deployment
- CI/CD Pipeline
- CloudWatch Monitoring

---

## 👩 Author

**Gauri Waidande**

GitHub:
https://github.com/gauriwaydande

Portfolio:
https://gauriwaydande.github.io/myportfoliowebsite/