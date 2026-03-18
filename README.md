# ☁️ Static Website Hosting using Amazon EC2, Nginx & Git

## 📌 What I Built

This project demonstrates static website hosting on an Ubuntu-based Amazon EC2 instance using Nginx as the web server.
Instead of serverless hosting (like S3), this implementation provisions compute infrastructure and follows a version-controlled Git deployment workflow, representing a traditional single-tier web architecture.

---

## 🏗 Architecture Flow

Client → Internet → Security Group → EC2 Instance → Nginx → index.html

- Amazon EC2 provides compute infrastructure  
- Security Group controls inbound access (SSH 22, HTTP 80)  
- Nginx serves static content from `/var/www/html`  
- Git manages version-controlled deployment  

---

## ⚙️ Implementation Summary

### Infrastructure Provisioning
- Launched Ubuntu 22.04 EC2 instance (t2.micro)
- Used default VPC with Internet Gateway
- Configured Security Group for ports 22 and 80
- Verified public IP accessibility

### Server Configuration
- Connected via SSH
- Updated package repository
- Installed Nginx and Git
- Enabled and started Nginx using systemctl

### Deployment (Git-Based)
- Created GitHub repository with index.html
- Cloned repository directly onto EC2
- Copied files to `/var/www/html`
- Restarted Nginx service
- Verified deployment using public IP

---

## 🛠 Implementation Steps

1. Launched EC2 instance in public subnet  
2. Configured inbound rules (SSH & HTTP)  
3. Connected to instance via SSH  
4. Installed Nginx and Git  
5. Enabled Nginx service  
6. Cloned GitHub repository  
7. Moved project files to `/var/www/html`  
8. Restarted Nginx and tested via public IP  

---

## 🔐 Security Considerations

- Public access restricted to required ports only  
- Applied principle of least privilege at Security Group level  
- No unnecessary services exposed  
- Verified proper file permissions in Nginx root directory  

---

## 🚀 Key Outcome

- Successfully deployed static website on compute-based infrastructure  
- Implemented version-controlled deployment workflow  
- Gained hands-on experience with Linux server management  
- Compared server-based hosting vs serverless (S3) approaches  

---

## 📂 Project Files

- `index.html` – Static website file  
- `README.md` – Project documentation  

---

### 📸 Snapshots include:

- Deployed website output  
- EC2 instance configuration  
- Ubuntu terminal with command execution

( Snapshots available in `Snapshots - 1.pdf` )

> **Disclaimer:** The repository was renamed so the clone URL may be different from earlier versions. Only the `index.html` file is used for deployment and the remaining files are removed before configuring Nginx.

---
