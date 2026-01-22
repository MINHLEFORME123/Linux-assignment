# Linux-assignment
<img width="1100" height="612" alt="image" src="https://github.com/user-attachments/assets/314696ed-6b8f-4f04-b123-f9ea0fdd08bd" />

Project Overview:
This document details the process of setting up a Linux Virtual Machine on Microsoft Azure at HAMK. The goal was to create a functional Ubuntu server to serve as a platform for future course assignments.

1. Environment Configuration  
The virtual machine was provisioned with the following specific settings as per the course requirements:  

Setting: Value  
Cloud Provider: Microsoft Azure (Azure for Students Subscription),  
Virtual Machine Name: Robo,  
Operating System: Ubuntu Server 24.04.3 LTS (Gen 2),  
Size: "Standard_B2ls (2 vcpus, 1 GiB memory)",  
Public IP Address: 172.161.69.141,  
Authentication Method: SSH Public Key (Robo_key.pem),  
Username: minhle,  

2. Installation Steps  
 
 -Subscription Setup: Logged into the Azure Portal using the HAMK student credentials and activated the Azure for Students subscription to access cloud resources.  
 
 -Resource Provisioning: Created a new Resource Group and configured the Virtual Machine instance named "Robo" with the Standard_B2ls size.  
 
 -Networking: Configured the Network Security Group (NSG) to allow inbound SSH traffic on port 22 to enable remote access.  
 
 -Security: Generated an SSH RSA private key and downloaded the .pem file to the local machine for secure authentication.  

3. Remote Connection  
Instead of using a third-party client like PuTTY, the connection was established using the Native SSH client via the Windows Command Prompt (CMD) for better integration.  

Command used: ssh -i "C:\Users\minhb\Downloads\Robo_key.pem" minhle@172.161.69.141  

4. Conclusion  
The Virtual Machine is successfully deployed and accessible. The system is running Kernel 6.14.0-1017-azure and is ready for further software installation and configuration  
