# Windows EC2 RDP Lab (AWS)

**Goal:** Deploy a **Windows Server (WS)** EC2 (**t3.micro – Free Tier**) and connect via **RDP (Remote Desktop Protocol)** using the **AWS-decrypted Administrator password**. Demonstrates **Networking (SG – Security Group)**, **IAM (Identity and Access Management)**, and **cost-safe operations**.

## Architecture (High-level)
- **Region**: `us-east-1 (N. Virginia)`
- **EC2**: Windows Server 2019, `t3.micro`
- **Access**: RDP (TCP 3389) from **My IP**
- **IAM**: Key pair for decrypting Windows password (no secrets committed)

## Steps

### 1) Launch EC2
- AMI (Amazon Machine Image): *Microsoft Windows Server 2019 Base*
- Instance type: `t3.micro` (**Free Tier**)
- Auto-assign Public IP: **Enabled**
- SG (Security Group): RDP **3389** from **My IP**
- ✅ Status checks = **Passed**

**Screenshot:**  
![Instances dashboard](screenshots/instance-dashboard.png)

### 2) Instance details
- Public IPv4, DNS, AZ visible
- Stop protection: Disabled (lab)
- Root volume: default

**Screenshot:**  
![Instance details](screenshots/instance-details.png)

### 3) Networking & Security
- Inbound rule: **RDP (TCP 3389)** → **My IP**
- Principle of least exposure (no 0.0.0.0/0 in production)

**Screenshot:**  
![Security group rule](screenshots/security-group.png)

### 4) Obtain Windows password
- EC2 → **Connect** → **RDP client** → **Get Password**
- Upload **.pem** → Decrypt → Copy **Administrator** password

**Screenshot (password blurred):**  
![Get password](screenshots/get-password.png)

### 5) Connect via RDP
- Download **.rdp** file from EC2 → open with mstsc
- User: **Administrator**
- Paste decrypted password → accept certificate → log in

**Screenshots:**  
![RDP login](screenshots/rdp-login.png)  
![Windows desktop](screenshots/windows-desktop.png)

## Clean-up (Cost-safe)
- **Stop** instance when idle (compute $0; storage billed).
- **Terminate** when done (deletes instance + EBS, stops billing).

## Skills Demonstrated
- **EC2 (Elastic Compute Cloud)** provisioning
- **Networking**: Security Groups, Public IPs
- **Identity**: Key pair usage, password decrypt flow
- **Ops hygiene**: Cost controls, documentation, screenshots

## Notes
- No secrets or keys committed. Screenshots redacted where needed.
- Region: `us-east-1`. Free Tier-friendly configuration.
