# 🚀 Linux Nginx Mini Project

## 📌 Project Overview
This project demonstrates the installation, configuration, and management of an Nginx web server on Linux.

The project includes:
- Installing Nginx
- Managing services using systemctl
- Editing Nginx configuration files
- Configuring a custom port (8080)
- Testing the server using curl
- Basic troubleshooting and verification

This project helped me gain hands-on experience with Linux administration and web server management.

---

# 🛠️ Technologies Used
- Linux (Ubuntu)
- Nginx
- Systemctl
- Curl
- Nano Editor
- Git & GitHub

---

# 📂 Project Architecture

```text
User Request
      ↓
Nginx Web Server
      ↓
Port 8080
      ↓
HTML Response Returned
```

---

# ⚡ Step 1: Install Nginx

```bash
sudo apt update
sudo apt install nginx -y
```

---

# ⚡ Step 2: Start and Check Nginx Service

```bash
sudo systemctl start nginx
sudo systemctl status nginx
```

## ✅ Output
Nginx service started successfully and running in active state.

### 📸 Screenshot
<img width="100%" alt="Nginx Status" src="https://raw.githubusercontent.com/Chandrashekhar-cloud/linux-nginx-mini-project/main/screenshots/nginx-status.jpg">

---

# ⚡ Step 3: Configure Custom Port

Open default Nginx configuration file:

```bash
sudo nano /etc/nginx/sites-available/default
```

Change:

```nginx
listen 80 default_server;
```

To:

```nginx
listen 8080 default_server;
```

---

## 📸 Configuration Screenshot
<img width="100%" alt="Nginx Config" src="https://raw.githubusercontent.com/Chandrashekhar-cloud/linux-nginx-mini-project/main/screenshots/nginx-config.jpg">

---

# ⚡ Step 4: Restart Nginx

```bash
sudo systemctl restart nginx
```

---

# ⚡ Step 5: Verify Using Curl

```bash
curl localhost:8080
```

## ✅ Output
Successfully received the Nginx welcome page response.

### 📸 Curl Output Screenshot
<img width="100%" alt="Curl Output" src="https://raw.githubusercontent.com/Chandrashekhar-cloud/linux-nginx-mini-project/main/screenshots/curl-output.jpg">

---

# 🧠 Key Learnings
- Linux command-line operations
- Installing and configuring Nginx
- Managing services with systemctl
- Understanding ports and networking basics
- Editing server configuration files
- Troubleshooting web server issues
- Testing server responses using curl

---

# 📊 Skills Demonstrated
- Linux Administration
- DevOps Fundamentals
- Web Server Deployment
- Networking Basics
- Troubleshooting
- Service Management
- Command Line Operations

---

# 🚀 Future Improvements
- Host a custom website using Nginx
- Configure reverse proxy
- Add HTTPS with SSL/TLS
- Deploy on AWS EC2
- Dockerize the Nginx server

---

# 🔗 GitHub Repository
## 👉 https://github.com/Chandrashekhar-cloud/linux-nginx-mini-project

---

# 👨‍💻 Author
### Chandrashekhar H S

Aspiring DevOps | Cloud | SRE Engineer 🚀
