# ☁️ Static Website Hosting using Amazon EC2, Nginx & Git

## 📌 Project Overview
This project demonstrates static website hosting on an Ubuntu-based Amazon EC2 instance using Nginx as the web server.  
Unlike serverless hosting (S3), this implementation provisions compute infrastructure and follows a version-controlled Git deployment workflow, representing a traditional single-tier architecture.

## 💻 Tech Stack
Amazon EC2, Ubuntu 22.04, Nginx, Git

## 🏗 Architecture Flow

Client → Internet → Security Group → EC2 Instance → Nginx → `index.html`

## ⚙️ Implementation Summary

### Infrastructure Provisioning
- Launched Ubuntu 22.04 EC2 instance (t2.micro)  
- Used default VPC with Internet Gateway  
- Configured Security Group for SSH (22) and HTTP (80)  
- Verified public IP accessibility  

### Server Configuration
- Connected via SSH  
- Updated system packages  
- Installed Nginx and Git  
- Enabled and started Nginx using `systemctl`  

### Deployment (Git-Based)
- Created GitHub repository with `index.html`  
- Cloned repository onto EC2 instance  
- Copied files to `/var/www/html`  
- Restarted Nginx service  
- Verified deployment using public IP  

## 🔍 Alternative Methods Explored
- **SCP** – Securely transfer files from local machine to EC2  
- **wget** – Download files directly from a remote source  
- **nano** – Directly edit files on the server  

These highlight trade-offs between speed, control, and maintainability compared to Git-based deployment.

## 🛠 Implementation Steps
1. Launched EC2 instance in public subnet  
2. Configured inbound rules (SSH & HTTP)  
3. Connected to instance via SSH  
4. Installed Nginx and Git  
5. Enabled Nginx service  
6. Cloned GitHub repository  
7. Moved project files to `/var/www/html`  
8. Restarted Nginx and tested via public IP  

## 🔐 Security Considerations
- Public access restricted to required ports only  
- Applied principle of least privilege at Security Group level  
- SSH key-based authentication for instance access  
- No unnecessary services exposed  
- Verified proper file permissions in Nginx root directory  

## ⚠️ Limitations
- Single EC2 instance setup (no horizontal scaling)  
- No load balancing → single point of failure  
- Manual scaling required for higher traffic  
- No CDN → higher latency for global users  

## 🚀 Key Outcomes
- Deployed static website on compute-based infrastructure  
- Implemented version-controlled deployment workflow  
- Gained hands-on experience with Linux server management  
- Understood differences between server-based and serverless hosting  

## 📂 Repository Files
- `index.html` – Static website file  
- `README.md` – Project documentation  
- `Snapshots.pdf` – Deployment snapshots  

> **Disclaimer:** The repository was renamed; the clone URL may differ from earlier versions. Only `index.html` is used for deployment; unnecessary files were removed before configuring Nginx.

## 📸 Snapshots Include
- Deployed website output  
- EC2 instance configuration  
- Ubuntu terminal with command execution
