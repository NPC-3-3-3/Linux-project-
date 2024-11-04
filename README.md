# 24CAP-607-Linux-Project
This is the repo for the College Project of Linux


# Personal Web Server Setup Using Apache on Red Hat Linux

## Project Overview
This project demonstrates the setup of a personal web server using Apache on Kali Linux. It covers the installation, configuration, and deployment of a custom HTML webpage.

## Installation and Setup Guide

### 1. Install Kali Linux on VMware
- Download the Kali Linux ISO from the official website.
- Install VMware Workstation or VMware Player.
- Create a new virtual machine and allocate appropriate resources.
- Follow the steps to install Kali Linux.

### 2. Update the System
Once Kali Linux is installed, update the system to the latest packages using:
```bash
sudo apt update && sudo apt upgrade -y
```


### 3. Install Apache Web Server
```bash
sudo apt install apache2 -y
```
Start and enable the Apache service:
```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```
### 4. Configure Firewall
Allow HTTP traffic by configuring the firewall:
```bash
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --reload
```
### 5. Create and Host Custom Webpage
- Navigate to `/var/www/html/`.
- Create a custom HTML webpage and save it as `index.html`:
```bash
sudo nano /var/www/html/index.html
```
- Ensure the file has the correct permissions:
```bash
sudo chown apache:apache /var/www/html/index.html
```

### 6. Access the Web Server
You can access the webpage by navigating to the server’s IP address in a browser:
```bash
http://<your-server-ip>
```

## Results
The Apache web server successfully hosts the custom webpage, accessible via the IP address of the server.

Below is a demo of the custom webpage running on the Apache server:
![Webpage Running](./assets/assetswebpage_demo.gif)

## Repository Contents
- `index.html`: The custom webpage deployed on the web server.
- `setup_guide.md`: Step-by-step guide to setting up the web server.
- `screenshots/`: A folder containing images of the setup process.
- `setup_webserver.sh`: A Script that automates the process of server creation.

##Conclusion
This project successfully demonstrates how to set up a personal web server using Apache on Kali Linux. The server is configured to serve static content, and basic web server management is covered.