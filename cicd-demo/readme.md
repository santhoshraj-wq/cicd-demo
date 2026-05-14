Basic CI/CD Deployment Workflow using GitHub, Nginx & AWS EC2

 📌 Overview

This project demonstrates a simple CI/CD-style deployment workflow using GitHub and AWS EC2. A static website was stored inside a GitHub repository, cloned into an EC2 instance, and deployed using the Nginx web server.

The project helped in understanding deployment workflows, Git-based version control, Linux server hosting, and how code updates are pulled from GitHub into cloud servers.

---

🛠️ Services & Tools Used

- Amazon EC2
- Amazon Linux
- Git & GitHub
- Nginx
- HTML
- Linux Terminal
- SSH

---

⚙️ Project Workflow

1️⃣ Created GitHub Repository
Created a GitHub repository named:

```text
cicd-demo

and uploaded a simple static website (index.html).

2️⃣ Launched EC2 Instance

Created an Amazon Linux EC2 instance.
Configured security group rules:
SSH (22) → My IP
HTTP (80) → Anywhere

3️⃣ Installed Required Packages

sudo yum install git -y
sudo yum install nginx -y

Installed Git for version control operations and Nginx for web hosting.

4️⃣ Started Nginx Web Server

sudo systemctl start nginx
sudo systemctl enable nginx

Enabled and started the Nginx service.

5️⃣ Cloned GitHub Repository into EC2

git clone <repository-url>

Downloaded website source code from GitHub into the EC2 server.

6️⃣ Deployed Website Files

sudo cp -r * /usr/share/nginx/html/

Copied website files into the Nginx web root directory.

7️⃣ Restarted Nginx

sudo systemctl restart nginx

Applied updated website changes.

8️⃣ Verified Deployment

Successfully accessed the hosted website using:
http://<public-ip>

9️⃣ Simulated CI/CD Update Workflow

Modified website files locally.
Pushed updates to GitHub.
Pulled latest code into EC2 using Git.
Redeployed updated files to Nginx server.

This simulated a basic continuous deployment workflow.

🧠 Key Learnings

GitHub repository management
Git-based deployment workflow
EC2 web hosting
Nginx web server configuration
Linux deployment process
CI/CD workflow basics
Server-side deployment troubleshooting

📈 Outcome

Successfully implemented a basic CI/CD-style deployment workflow by integrating GitHub version control with an AWS EC2-hosted Nginx web server.

🔥 Real-World Relevance

This project introduces concepts commonly used in:

CI/CD pipelines
deployment automation
DevOps workflows
cloud application hosting
version-controlled deployments

🧹 Cleanup
Terminated EC2 instance after testing
Removed temporary deployment files