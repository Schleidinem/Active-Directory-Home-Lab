# 🖥️ Active Directory Home Lab with VMware 

## 📌 Project Overview  
This lab demonstrates how to set up **Active Directory (AD)** on a **Windows Server virtual machine** using **VMware Workstation Pro**.  
The project covers installation, configuration, and AD setup, including **Organizational Units (OUs), groups, users, and role assignments**

## 🎯 Objectives  
- Install Windows Server in VMware Workstation Pro  
- Set up and configure **Active Directory Domain Services (AD DS)**
-  Use **Server Manager** to install and assign roles/features  
- Create **Organizational Units (OUs)** to represent departments/regions  
- Add **groups** within OUs  
- Create and manage **user accounts** in AD  

## 🛠️ Tech Stack  
- VMware Workstation 
- Windows Server (ISO image)  
- Active Directory Domain Services (AD DS)  

## 📂 Lab Steps  

1. **VMware Setup**  
   - Installed VMware Workstation Pro
     <img width="975" height="635" alt="image" src="https://github.com/user-attachments/assets/206d19bc-202c-4eae-b36c-23245c7144f4" />

   - Created a new virtual machine (VM)
     <img width="975" height="426" alt="image" src="https://github.com/user-attachments/assets/a1c6171a-49aa-4fc5-aded-5bdd7a0b5a90" />
     Once VM is created, Upload ISO Image (right click on window server => Setting)
     <img width="975" height="452" alt="image" src="https://github.com/user-attachments/assets/7581c7c4-43b0-4a97-887d-06a4605baf72" />



   - Installed Windows Server on the VM (select Standard evaluation Desktop Experience)

     <img width="975" height="425" alt="image" src="https://github.com/user-attachments/assets/4eceef33-2685-4213-87e3-75f4ce87451b" />
  
     Select Custom Install
     <img width="975" height="719" alt="image" src="https://github.com/user-attachments/assets/07dfb931-46f7-4c52-9896-a86a6fd7df92" />
     Next
     <img width="975" height="673" alt="image" src="https://github.com/user-attachments/assets/5f0ea178-548d-479f-a8e2-0660ac680931" />

     <img width="975" height="578" alt="image" src="https://github.com/user-attachments/assets/1c4cbabb-c8b5-49af-ae53-4af59dcbb553" />

     <img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/69121507-f1ee-47be-a9bd-77360c2ca23b" />


  2. **In the Server Manager Dashboard Select Add roles and features**

   <img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/dd77a468-100e-4df1-ac7b-888fc6f6c70b" />
   <img width="975" height="690" alt="image" src="https://github.com/user-attachments/assets/6deb2496-ca10-45fa-8cc8-fa355553b242" />
   <img width="975" height="435" alt="image" src="https://github.com/user-attachments/assets/1956cbfe-5ef0-433a-89f9-04c03c6137be" />

   <img width="975" height="663" alt="image" src="https://github.com/user-attachments/assets/a73373df-fb03-40fc-9317-28b21bc5ef5c" />
  
  3. **Active Directory Installation**  
   - Installed **Active Directory Domain Services (AD DS)**
     <img width="975" height="628" alt="image" src="https://github.com/user-attachments/assets/167a9753-d269-4c9a-88e7-65c940d00c83" />
     <img width="975" height="586" alt="image" src="https://github.com/user-attachments/assets/4dbdbf83-85a1-44a1-a157-4a92b5ffc3e5" />

      We have installed the Active directory role but now we need to promote it to a domain controller
     so click to add new forest and set root domain name to mydomain.com ==> click next
    <img width="975" height="535" alt="image" src="https://github.com/user-attachments/assets/7b152df1-98d5-4ba9-a2a0-3ac0fffff505" />

   Set Password
   <img width="975" height="573" alt="image" src="https://github.com/user-attachments/assets/3635fa24-22a0-411d-902d-20520be848c4" />

    Next
   <img width="975" height="554" alt="image" src="https://github.com/user-attachments/assets/938bae6d-ffdd-46e7-80ac-9f87c2aab661" />

   Next
   <img width="975" height="556" alt="image" src="https://github.com/user-attachments/assets/f9dec2b0-c103-4369-9df3-383f4fda4383" />

  Install when done restart

 <img width="975" height="559" alt="image" src="https://github.com/user-attachments/assets/db2594ca-0095-4c2a-aed8-35ec30590ab3" />
 <img width="975" height="459" alt="image" src="https://github.com/user-attachments/assets/ae241ad5-3e02-4384-9a87-4b2cd2c4989f" />


4. Creating Admin User Account
In the start menu select active directory users and computers
<img width="561" height="458" alt="image" src="https://github.com/user-attachments/assets/88d261d2-b0cc-4356-9d3d-473e351278cd" />

   - Right click to create Organizational unit
     <img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/040af9b1-c15c-427a-adef-eae96b0d8bdb" />
  
   - Created **Groups** within OUs
     <img width="975" height="672" alt="image" src="https://github.com/user-attachments/assets/db52449b-f7bb-49c3-b89b-490d40a5d331" />

   - Added **Users** and assigned them to groups
     <img width="975" height="483" alt="image" src="https://github.com/user-attachments/assets/7466886a-59c0-48b9-8b6f-d209e846ec9a" />
     <img width="975" height="561" alt="image" src="https://github.com/user-attachments/assets/428b498c-0bda-449a-9a44-983d2c3660cc" />


## 📜 Key Learnings  
- Hands-on experience with **VMware Workstation Pro**  
- Installing and configuring **Windows Server**  
- Using **Server Manager** to assign roles and features  
- Setting up **Active Directory Domain Services (AD DS)**  
- Managing users, groups, and OUs in AD  
- Role-based access control and permissions management  
- Understanding enterprise **Identity & Access Management (IAM)**  

            
