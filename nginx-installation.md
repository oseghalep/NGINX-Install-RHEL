# NGINX Installation on RHEL

Follow these steps to install NGINX on a RHEL server.

## Step 1: Update System Packages

Before installing any software, it's a good practice to update your system:
```bash
sudo dnf update -y

## Step 2: Install NGINX
To install NGINX, run the following command:
sudo dnf install nginx -y

## Step 3: Start NGINX Service
Once installed, start the NGINX service:
sudo systemctl start nginx

## Step 4: Enable NGINX to Start on Boot
To ensure NGINX starts automatically when the server reboots:
sudo systemctl enable nginx

## Step 5: Adjust Firewall Rules
If you're using firewalld, allow HTTP and HTTPS traffic:
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --permanent --add-service=https
sudo firewall-cmd --reload

## Step 6: Verify Installation
Open a web browser and navigate to your server's IP address. You should see the NGINX welcome page.
http://your-server-ip

Step 7: Basic Configuration
The default configuration file is located at /etc/nginx/nginx.conf.
Virtual host files can be added to /etc/nginx/conf.d/.

Conclusion
You have successfully installed and configured NGINX on your RHEL server.
