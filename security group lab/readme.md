# AWS EC2 Security Group & Secure Access Lab

📌 Overview

This project demonstrates how to configure AWS EC2 Security Groups to securely control access to cloud servers. The lab focused on implementing secure SSH access restrictions while allowing public HTTP access for web hosting.

The project helped in understanding AWS network security basics, inbound and outbound traffic rules, and how Security Groups act as virtual firewalls in cloud environments.

---

🛠️ Services & Tools Used

- Amazon EC2
- Amazon Linux
- AWS Security Groups
- Nginx
- Linux Terminal
- SSH

---

⚙️ Project Workflow

### 1️⃣ Launched EC2 Instance

- Created an Amazon Linux EC2 instance.
- Configured a custom Security Group.

---

### 2️⃣ Created Custom Security Group

Created:

```text
secure-ec2-sg

with custom inbound traffic rules.

3️⃣ Configured Secure Inbound Rules

Type	Port 	Source
SSH	     22	    My IP
HTTP	80	    Anywhere

This ensured:

SSH access remained restricted to a trusted IP address
Website traffic remained publicly accessible

4️⃣ Connected Securely using SSH

ssh -i "key.pem" ec2-user@<public-ip>

Successfully accessed the server securely using restricted SSH rules.

5️⃣ Installed Nginx Web Server

sudo yum install nginx -y

Installed Nginx inside the EC2 instance.

6️⃣ Started Nginx Service

sudo systemctl start nginx

Started the Nginx web server.

7️⃣ Verified Public HTTP Access

Successfully accessed the Nginx webpage using:

http://<public-ip>

8️⃣ Tested Security Group Rules

Temporarily removed the HTTP inbound rule and observed that the website became inaccessible.

Re-added the HTTP rule and confirmed website accessibility again.

This demonstrated how AWS Security Groups control incoming network traffic.

🧠 Key Learnings

AWS Security Group configuration
Inbound vs outbound traffic rules
SSH access restriction
Public HTTP access configuration
Cloud firewall concepts
EC2 secure access practices
Basic cloud security principles

📈 Outcome

Successfully configured secure AWS EC2 access using Security Groups by restricting SSH access to a trusted IP while exposing HTTP traffic publicly for web hosting.

🔥 Real-World Relevance

This project introduces concepts commonly used in:

cloud security
infrastructure protection
server hardening
secure cloud deployments
DevOps infrastructure management

🧹 Cleanup

Terminated EC2 instance after testing
Removed unused security groups and resources