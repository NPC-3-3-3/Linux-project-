
# Setup Guide for Personal Web Server Using Apache on Red Hat Linux

## Introduction
This guide provides detailed steps to install and configure Apache HTTP Server on Kali Linux, enabling you to host a simple webpage. Follow each step carefully to ensure a successful setup.

## Prerequisites
- A working installation of Kali Linux on VMware.
- Internet connection to download packages and updates.

## Step 1: Install Red Hat Linux on VMware
1. Download the Red Hat Enterprise Linux Developer Edition.
2. Install VMware Workstation or VMware Player on your system.
3. Create a new virtual machine and allocate appropriate resources (CPU, RAM, Disk Space).
4. Follow the installation prompts to complete the installation of Kali Linux.

## Step 2: Update the System
After logging into the Red Hat Linux system, open the terminal and run the following command to update the system:
```bash
sudo apt update && sudo apt upgrade -y
```

## Step 3: Install Apache Web Server
To install the Apache HTTP Server, execute the following command in the terminal:
```bash
sudo apt install apache2 -y
```

### Step 4: Start and Enable Apache Service
After logging into the Kali Linux system, open the terminal and run the following command to update the system:
```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

### Step 5: Configure Firewall
Allow HTTP traffic through the firewall with the following commands:
```bash
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --reload
```

### Step 6: Create a Custom Webpage
1. Navigate to the Apache root directory:
```bash
   cd /var/www/html/
   ```
2. Create a new HTML file for your webpage:
```bash
   sudo nano index.html
   ```
3. Add your HTML content and save the file.

### Step 7: Set File Permissions
Ensure that the file has the appropriate permissions:
```bash
sudo chown apache:apache /var/www/html/index.html
```

## Step 8: Access the Web Server
Open a web browser and access your webpage using the server's IP address:
```bash
 http://<your-server-ip>
```

## Conclusion
By following this setup guide, you will have a fully functional web server using Apache on Kali Linux, hosting your custom webpage. Ensure to explore additional configurations and security measures for production environments.

