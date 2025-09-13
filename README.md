# 🖥️ AWS EC2 Windows RDP Lab

This project demonstrates how to launch a **Windows Server EC2 instance** on AWS (Free Tier) and connect to it using **Remote Desktop (RDP)**.  
It covers **core Cloud Engineer skills**: EC2 provisioning, Security Groups, password decryption with PEM, and RDP connectivity.

---

## 📌 Lab Overview
- **Region:** us-east-1 (N. Virginia)  
- **Instance Type:** t3.micro (Free Tier eligible)  
- **AMI:** Microsoft Windows Server 2019 Base  
- **Access Method:** Remote Desktop Protocol (RDP)  
- **Security:** Inbound rule for RDP (TCP 3389) restricted to my IP  

---

## 🚀 Steps Performed

### 1️⃣ Launch Windows EC2
- Selected Windows Server 2019 AMI.  
- Instance type: `t3.micro`.  
- Public IP auto-assigned.  

**Screenshot:**  
[![01-AMI](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/01-AMI.png)](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/01-AMI.png)
---

### 2️⃣ Instance Running
- Verified in AWS Console.  
- Instance state = Running ✅  
- Status checks = Passed ✅  

**Screenshot:**  
[![02-aws-console](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/02-aws-console.png)](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/02-aws-console.png)
---

### 3️⃣ Decrypt Windows Password
- EC2 → Connect → RDP Client → Get Password.  
- Uploaded `.pem` file.  
- Decrypted the Administrator password (blurred in screenshot).  

**Screenshot:**  
[![03-decrypted-password](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/03-decrypted-password.png)](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/03-decrypted-password.png)
---

### 4️⃣ RDP Login
- Downloaded `.rdp` file from AWS Console.  
- Opened in mstsc.  
- Used Administrator username + decrypted password.  

**Screenshot:**  
[![04-rdp-login](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/04-rdp-login.png)](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/04-rdp-login.png)


---

### 5️⃣ Public IP Assigned
- Copied Public IPv4 address to connect via RDP.  

**Screenshot:**  
[![05-public-ip](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/05-public-ip.png)](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/05-public-ip.png)
---

### 6️⃣ Security Group Rules
- Configured inbound rules for **RDP (3389)** from **My IP**.  

**Screenshot:**  
[![06-security-groups](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/06-security-groups.png)](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/06-security-groups.png)
---

### 7️⃣ Inside Windows Desktop
- Successfully logged into Windows Server EC2.  
- Verified via Command Prompt (`hostname`).  

**Screenshot:**  
[![07-inside-windows-desktop](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/07-inside-windows-desktop.png)](https://github.com/yashkumarunt/aws-ec2-windows-rdp-lab/blob/main/07-inside-windows-desktop.png)
---

## 🧹 Clean-Up
- Stopped/terminated instance to avoid charges.  
- Free Tier covers t3.micro + 30 GB storage.  

---

## 🛠️ Skills Demonstrated
- **EC2 provisioning** (Windows workload)  
- **Networking** (Security Groups, RDP access)  
- **Identity** (Key pair usage, password decrypt flow)  
- **Ops hygiene** (Cost controls, cleanup)  
- **Documentation** (GitHub repo with screenshots)  

---

## 📂 Repository Structure
