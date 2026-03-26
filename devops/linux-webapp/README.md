## 🐧 Linux Web Application Deployment (LAMP Stack)
Deployed a simple e-commerce web application on a Linux server using Apache, MariaDB, and PHP. Configured firewall rules, database setup, and application connectivity.

# 🧰 Technologies Used
- Linux (CentOS / RHEL-based)
- Apache (httpd)
- MariaDB
- PHP
- Firewalld
- Git

# 🏗️ Architecture Overview
Client → Apache (httpd) → PHP → MariaDB

# 🔧 Key Implementation Steps
🔹 Firewall Configuration

```
sudo yum install firewalld
sudo systemctl start firewalld
sudo systemctl enable firewalld

sudo firewall-cmd --permanent --add-port=80/tcp
sudo firewall-cmd --permanent --add-port=3306/tcp
sudo firewall-cmd --reload
```
🔹 Database Setup (MariaDB)

```
sudo yum install mariadb-server
sudo systemctl start mariadb
sudo systemctl enable mariadb
```
Created:
- Database: ecomdb
- User: ecomuser
- Permissions configured for application access

🔹 Web Server Setup (Apache + PHP)

```
sudo yum install -y httpd php php-mysqlnd
sudo systemctl start httpd
sudo systemctl enable httpd
```
Configured Apache to use:
- index.php as default page

🔹 Application Deployment

```
sudo yum install -y git
git clone <repo> /var/www/html/
```

🔹 Testing
```
curl http://localhost
```

✅ Website fully operational

![Curl Test Result](cloud-ops-portfolio/devops/linux-webapp/curl.png)
![Pipeline Success](cloud-ops-portfolio/devops/linux-webapp//ecom site.png)

# ⚠️ Challenges & Fixes
- ❌ Database connection issues
→ Fixed by updating application config and verifying credentials
- ❌ Firewall blocking traffic
→ Opened required ports (80, 3306)
- ❌ Apache default page not loading PHP
→ Updated DirectoryIndex to use index.php

# 🧠 What I Learned
- How to configure a full LAMP stack on Linux
- Managing firewall rules for application access
- Connecting a web application to a database
- Troubleshooting service and connectivity issues

# 🎯 Outcome
Successfully deployed a working web application on a Linux server with a configured database backend and web server.
