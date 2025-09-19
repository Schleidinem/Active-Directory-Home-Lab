# Windows-Server-Hybrid-Environment---Personal-Home-Lab

# 🖥️ Active Directory Setup Lab

This project demonstrates how to set up a Microsoft Active Directory (AD) environment inside a Windows Server virtual machine. It showcases hands-on skills in system administration, user/group management, domain configuration, and automation with PowerShell.  

---

## 📌 Overview
- **Platform**: VirtualBox / VMware / Azure VM  
- **OS**: Windows Server 2019/2022 Datacenter (Desktop Experience)  
- **Network**: Private Virtual Network (Static IP)  
- **Tools**:  
  - Active Directory Domain Services (AD DS)  
  - Active Directory Users and Computers (ADUC)  
  - PowerShell  

---

## ⚙️ Environment Setup

### Step 1: Create the VM
1. Provision a new VM with:  
   - 4 GB RAM, 2 CPUs, 60 GB storage.  
   - Networking: NAT + Host-Only (or Azure VNet if cloud-based).  
2. Install **Windows Server 2019/2022**.  
3. Configure **Administrator password**.  

---

### Step 2: Configure Networking
Set a **static IP** on your VM:  
- **IP**: `192.168.1.10`  
- **Subnet**: `255.255.255.0`  
- **Gateway**: `192.168.1.1`  
- **DNS**: `127.0.0.1`  

---

### Step 3: Install AD DS Role
1. Open **Server Manager** → *Add Roles and Features*.  
2. Install **Active Directory Domain Services (AD DS)**.  
3. Promote the server to a **Domain Controller**.  
4. Create a new forest:  
   - Domain name: `corp.local`.  
5. Restart VM.  

---

### Step 4: Configure Active Directory
1. Open **ADUC**.  
2. Create **Organizational Units (OUs)**:  
   - `Users`  
   - `Groups`  
   - `Service Accounts`  
3. Add test users:  
   - `John.Doe` (Sales)  
   - `Jane.Smith` (HR)  
   - `Admin.User` (Help Desk Admin)  
   - `Svc_Deploy` (Service Account)  
4. Add groups:  
   - `IT.Support`  
   - `HR.Team`  

---

### Step 5: Automate with PowerShell
```powershell
# Bulk create sample users in OU=Users
1..10 | ForEach-Object {
  New-ADUser -Name "User$_" `
             -SamAccountName "user$_" `
             -Path "OU=Users,DC=corp,DC=local" `
             -Enabled $true `
             -AccountPassword (ConvertTo-SecureString 'P@ssw0rd!' -AsPlainText -Force)
}
