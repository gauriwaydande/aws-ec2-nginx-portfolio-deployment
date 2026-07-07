# AWS EC2 Nginx Portfolio Deployment

## Project Overview

This project demonstrates the deployment of my personal portfolio website on an AWS EC2 Ubuntu instance using the Nginx web server. The website is hosted on a cloud server and is publicly accessible through the internet.

---

## Technologies Used

- AWS EC2
- Ubuntu Linux
- Nginx Web Server
- HTML5
- CSS3
- JavaScript
- Git
- GitHub
- SSH

---

## Architecture

User Browser
      │
      ▼
Public IP Address
      │
      ▼
AWS EC2 Instance (Ubuntu)
      │
      ▼
Nginx Web Server
      │
      ▼
Portfolio Website

---

## Prerequisites

- AWS Account
- EC2 Ubuntu Instance
- SSH Key Pair (.pem)
- Portfolio Website Files
- GitHub Account

---

# Step 1: Launch EC2 Instance

- Login to AWS Console
- Open EC2 Dashboard
- Launch Ubuntu Server
- Select t2.micro (Free Tier)
- Create Key Pair
- Allow HTTP (80), HTTPS (443) and SSH (22)

---

# Step 2: Connect to EC2

```bash
ssh -i your-key.pem ubuntu@your-public-ip
```

---

# Step 3: Update Server

```bash
sudo apt update
sudo apt upgrade -y
```

---

# Step 4: Install Nginx

```bash
sudo apt install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
```

Check Status

```bash
sudo systemctl status nginx
```

---

# Step 5: Upload Portfolio Files

```bash
cd /var/www/html
sudo rm index.nginx-debian.html
sudo cp -r ~/portfolio/* /var/www/html/
```

Set Permissions

```bash
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
```

---

# Step 6: Restart Nginx

```bash
sudo systemctl restart nginx
```

---

# Step 7: Access Website

Open Browser

```
http://YOUR_PUBLIC_IP
```

Example

```
http://13.xxx.xxx.xxx
```

---

## Project Outcome

- Successfully deployed portfolio website on AWS EC2.
- Installed and configured Nginx Web Server.
- Hosted a static website on Ubuntu Linux.
- Learned Linux server management.
- Website accessible using Public IP.

---

## Troubleshooting

### Nginx Not Running

```bash
sudo systemctl restart nginx
sudo systemctl status nginx
```

### Website Not Opening

- Check Security Group Rules
- Verify Port 80 is open
- Check Nginx Service
- Verify Public IP

---

## Future Enhancements

- HTTPS using SSL
- Custom Domain
- Docker Deployment
- CI/CD Pipeline
- Monitoring using CloudWatch

---

## Author

**Gauri Waidande**

Cloud & DevOps Learner

GitHub:
https://github.com/gauriwaydande

Portfolio:
https://gauriwaydande.github.io/myportfoliowebsite/