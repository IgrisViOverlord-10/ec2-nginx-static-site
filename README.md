# ☁️ Static Website Hosting using Amazon EC2, Nginx & Git

## 📌 Project Overview

This project demonstrates static website hosting on an Ubuntu-based Amazon EC2 instance using Nginx as the web server.  
Unlike serverless hosting (such as S3), this implementation provisions compute infrastructure and follows a version-controlled Git deployment workflow, representing a traditional single-tier architecture.

---

## 🏗 Architecture Flow

Client → Internet → Security Group → EC2 Instance → Nginx → `index.html`

---

## ⚙️ Implementation Summary

### Infrastructure Provisioning
- Launched Ubuntu 22.04 EC2 instance (t2.micro)  
- Used default VPC with Internet Gateway  
- Configured Security Group for ports 22 and 80  
- Verified public IP accessibility  

### Server Configuration
- Connected via SSH  
- Updated system packages  
- Installed Nginx and Git  
- Enabled and started Nginx using systemctl  

### Deployment (Git-Based)
- Created GitHub repository with `index.html`  
- Cloned repository onto EC2 instance  
- Copied files to `/var/www/html`  
- Restarted Nginx service  
- Verified deployment using public IP  

---

## 🔍 Alternative Methods Explored

To compare different deployment approaches, the following methods were also tested:

- **SCP** – Securely transfers files from local machine to EC2  
- **wget** – Downloads project files directly from a remote source  
- **nano** – Allows direct editing of files on the server  

These approaches highlight trade-offs between speed, control, and maintainability compared to a Git-based workflow.

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
- Instance access restricted using SSH key-based authentication  
- No unnecessary services exposed  
- Verified proper file permissions in Nginx root directory  

---

## 🚀 Key Outcome

- Successfully deployed static website on compute-based infrastructure  
- Implemented version-controlled deployment workflow  
- Gained hands-on experience with Linux server management  
- Understood differences between server-based and serverless hosting approaches  

---

## 📂 Repository Files

- `index.html` – Static website file  
- `README.md` – Project documentation  
- `Snapshots - 1.pdf` – Project snapshots  

> **Disclaimer:** The repository was renamed, so the clone URL may differ from earlier versions. Only the `index.html` file is used for deployment, and unnecessary files are removed before configuring Nginx.

---

## 📸 Snapshots include:

- Deployed website output  
- EC2 instance configuration  
- Ubuntu terminal with command execution  

---
