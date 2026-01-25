Linux Mini Project – Nginx Port Configuration & Verification
Project Overview
This project demonstrates basic Linux system administration and SRE fundamentals by installing and configuring an Nginx web server, modifying its default port, managing services, and verifying connectivity using command-line tools.
The goal is to show hands-on understanding of:
Linux services (systemctl)
Configuration files
Networking ports
Basic troubleshooting
Tools & Technologies
OS: Linux (Ubuntu)
Web Server: Nginx
Commands Used:
apt, systemctl
nano
ss
curl
ufw
Steps Performed
1. Install Nginx
Copy code
Bash
sudo apt update
sudo apt install nginx -y
Verify installation:
Copy code
Bash
systemctl status nginx
2. Start and Enable Nginx Service
Copy code
Bash
sudo systemctl start nginx
sudo systemctl enable nginx
3. Change Default Port (80 → 8080)
Edit the default Nginx configuration file:
Copy code
Bash
sudo nano /etc/nginx/sites-available/default
Change:
Copy code
Nginx
listen 80;
To:
Copy code
Nginx
listen 8080;
Save and exit.
Test configuration:
Copy code
Bash
sudo nginx -t
Restart Nginx:
Copy code
Bash
sudo systemctl restart nginx
4. Open Firewall for Port 8080
Copy code
Bash
sudo ufw allow 8080
sudo ufw reload
5. Verify Using curl
Copy code
Bash
curl localhost:8080
Expected output:
Copy code

Welcome to nginx!
Troubleshooting Performed
When curl localhost failed, identified that Nginx was no longer listening on port 80.
Verified active listening ports using:
Copy code
Bash
ss -tulnp | grep nginx
Confirmed Nginx was correctly bound to port 8080.
Key Learnings
Linux services listen only on configured ports
Configuration changes require service restart
curl is useful for local service verification
Basic troubleshooting follows check service → check port → verify logs
Outcome
✅ Successfully installed and configured Nginx
✅ Changed default port from 80 to 8080
✅ Verified service using command-line tools
Project Type
Linux / SRE / DevOps – Beginner Mini Project
