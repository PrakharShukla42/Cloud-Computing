# 🌐 Multi Server Hosting on AWS Linux Server in Mumbai Region🌐

## Overview 🚀
Welcome to the Multi Server Hosting on AWS project! This guide walks you through the process of hosting multiple websites on a single Amazon Linux EC2 instance in the AWS Mumbai region. By leveraging Amazon Web Services (AWS), we create an efficient, scalable, and cost-effective environment for hosting multiple websites without the need for multiple servers.

## Key Features 🔑
- ✅ **Single EC2 Instance Hosting**: Host multiple websites on a single EC2 instance.
- ✅ **Apache Web Server Setup**: Use Apache to configure multiple virtual hosts.
- ✅ **Domain Configuration**: Set up domains and SSL for each website for secure connections.
- ✅ **Cost Optimization**: Minimize resource usage while maintaining high availability.

## Prerequisites 📋
Before diving into the setup, please ensure you have:
- An AWS Account (If you don’t, create one [here](https://aws.amazon.com/)).
- A basic understanding of AWS EC2 and Linux commands.
- Access to domain names for each website you plan to host.

## 🛠️ Setup Instructions

### Step 1: Launch Your EC2 Instance 🚀
1. **Log in to AWS**: Head over to your AWS Management Console.
2. **Create EC2 Instance**:
   - Navigate to the EC2 Dashboard and launch a new instance with the Amazon Linux 2 AMI.
   - Select an instance type (e.g., t2.micro for lightweight testing).
   - Choose security group settings that allow HTTP (port 80), HTTPS (port 443), and SSH (port 22).
   - Assign an Elastic IP for consistent public access.
   - Generate or use an existing SSH key pair for instance login.

### Step 2: Install Apache Web Server 🖥️
Once your EC2 instance is up and running:
1. **Connect to your EC2 instance via SSH**:
   ```bash
   ssh -i your-key.pem ec2-user@your-instance-public-ip
2. **Update Packages**
   ```bash
   sudo yum update -y
3. **Install Apache**
   ```bash
   sudo yum install httpd -y
4. **Start Apache and set it to auto-start on boot**
   ```bash
   sudo service httpd start
   sudo chkconfig httpd on

## Configure Firewall for Apache
### 1.Allow HTTP and HTTPS traffic in the security group:
 - Go to your EC2 Dashboard.
 - Click on "Security Groups" in the left menu.
 - Select the security group associated with your EC2 instance.
 - Under the "Inbound rules" tab, ensure that rules for HTTP (port 80) and HTTPS (port 443) are added.

## Configure Virtual Hosts for Multiple Websites 🌐
5. **Create directories for each website**
   ``` bash
    sudo mkdir /var/www/html/website1
    sudo mkdir /var/www/html/website2

###



https://github.com/user-attachments/assets/7647e40f-1670-4734-b380-99d557ba96b3

