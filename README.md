# AWS EC2 Nginx Portfolio Deployment

## Project Overview

This project demonstrates the deployment of a personal portfolio website on an AWS EC2 instance using Nginx as the web server. The objective was to host a static portfolio website on a cloud environment and make it accessible through a public IP address.

## Technologies Used

* Amazon Web Services (AWS)
* EC2 (Elastic Compute Cloud)
* Ubuntu Server
* Nginx Web Server
* HTML
* CSS
* JavaScript
* Linux Command Line

## Project Architecture

User Browser → AWS EC2 Instance → Nginx Web Server → Portfolio Website

## Deployment Steps

### 1. Launch EC2 Instance

* Created an Ubuntu EC2 instance on AWS.
* Configured Security Groups.
* Allowed:

  * SSH (Port 22)
  * HTTP (Port 80)
  * HTTPS (Port 443)

### 2. Connect to EC2

```bash
ssh -i key.pem ubuntu@<public-ip>
```

### 3. Update System

```bash
sudo apt update
sudo apt upgrade -y
```

### 4. Install Nginx

```bash
sudo apt install nginx -y
```

### 5. Verify Installation

```bash
sudo systemctl status nginx
```

### 6. Deploy Portfolio Files

```bash
cd /var/www/html
sudo rm index.nginx-debian.html
```

Upload portfolio files and place them inside:

```bash
/var/www/html
```

### 7. Restart Nginx

```bash
sudo systemctl restart nginx
```

### 8. Access Website

Open browser and visit:

```text
http://<EC2-Public-IP>
```

## Features

* Cloud-hosted portfolio website
* Public internet accessibility
* Nginx web server configuration
* Linux server administration
* AWS EC2 deployment experience

## Learning Outcomes

Through this project, I gained practical experience in:

* Cloud Computing with AWS
* Linux Server Management
* Web Hosting
* Nginx Configuration
* EC2 Instance Management
* Network Security Configuration

## Screenshots

Add deployment screenshots here:

* AWS EC2 Dashboard
* Nginx Running Status
* Portfolio Website Homepage
* Security Group Configuration

## Author

**Omkar Dhakane**

Data Science Student | Cloud Enthusiast | Web Developer

GitHub: https://github.com/omkar-dhakane

LinkedIn: https://www.linkedin.com/in/omkar-dhakane/

## License

This project is created for educational and learning purposes.
