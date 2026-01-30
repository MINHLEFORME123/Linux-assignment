# Linux-assignment
<img width="1100" height="612" alt="image" src="https://github.com/user-attachments/assets/314696ed-6b8f-4f04-b123-f9ea0fdd08bd" />

# 🤖 Project Robo: Linux VM Deployment on Microsoft Azure

![Ubuntu](https://img.shields.io/badge/OS-Ubuntu%2024.04%20LTS-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Azure](https://img.shields.io/badge/Cloud-Microsoft%20Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

## 📄 Project Overview
This document details the process of setting up a **Linux Virtual Machine** on **Microsoft Azure** at HAMK. The goal was to create a functional Ubuntu server to serve as a robust platform for future course assignments and software development.



---

## 🛠 1. Environment Configuration
The virtual machine was provisioned with the following specific settings as per the course requirements:

| Setting | Value |
| :--- | :--- |
| **Cloud Provider** | Microsoft Azure (Azure for Students Subscription) |
| **Virtual Machine Name** | `Robo` |
| **Operating System** | Ubuntu Server 24.04.3 LTS (Gen 2) |
| **Size** | `Standard_B2ls` (2 vcpus, 1 GiB memory) |
| **Public IP Address** | `172.161.69.141` |
| **Authentication** | SSH Public Key (`Robo_key.pem`) |
| **Username** | `minhle` |

---

## 🚀 2. Installation Steps

### 🔹 Subscription Setup
* Logged into the **Azure Portal** using HAMK student credentials.
* Activated the **Azure for Students** subscription to access cloud resources without upfront costs.

### 🔹 Resource Provisioning
* Created a new **Resource Group** to organize project assets.
* Configured the VM instance named **"Robo"** with the optimized `Standard_B2ls` size.

### 🔹 Networking & Security
* **NSG (Network Security Group):** Configured to allow inbound SSH traffic on **Port 22**.
* **Key Pair:** Generated an SSH RSA private key and securely downloaded the `.pem` file to the local machine.

---

## 💻 3. Remote Connection
Instead of using third-party clients like PuTTY, the connection was established using the **Native SSH client** via Windows Command Prompt (CMD) for better system integration.

> [!IMPORTANT]
> Make sure the `.pem` file has the correct permissions and the path is correct before running the command.

```bash
# Command to connect to the VM
ssh -i "C:\Users\minhb\Downloads\Robo_key.pem" minhle@172.161.69.141
```
## ✅4. Conclusion  
The Virtual Machine is successfully deployed and accessible. The system is running Kernel 6.14.0-1017-azure and is ready for further software installation and configuration  
