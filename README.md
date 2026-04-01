# Linux-Lab-01-user-management-
This lab demonstrates basic Linux user management, permissions, and workspace isolation using Bash.
---

## Overview

For this project, I was tasked to create two new users named **student** and **student2** utilizing Bash. The goal was to set up isolated workspaces, assign proper permissions, and verify access control between the two accounts.

Initial home directory before creating users
<img width="1307" height="841" alt="Initial home directory before creating users" src="https://github.com/user-attachments/assets/8ac15542-3c45-49f0-89e7-18cc354eb33b" />

---

## Commands Used

Created the users
'''bash 
sudo adduser student
sudo adduser student2

### 1. Creating users student and student2 using adduser
<img width="1317" height="857" alt="Creating users student and student2 using adduser" src="https://github.com/user-attachments/assets/b446ee0c-4524-4700-bd14-31a3d7edd3d6" />

Created workspace folders
sudo mkdir /home/student/workspace
sudo mkdir /home/student2/workspace

### 2. Creating and verifying workspace directories for both users
<img width="980" height="812" alt="Creating and verifying workspace directories for both users" src="https://github.com/user-attachments/assets/c8c4905c-75a7-4fdf-832e-a1b6a55c7d96" />

Assigned permissions and ownership
sudo chown student:student /home/student/workspace
sudo chown student2:student2 /home/student2/workspace

### 3. Assign permissions and ownership
<img width="1005" height="797" alt="Assigning file ownership to each user with chown" src="https://github.com/user-attachments/assets/c6dd6edd-15fb-4823-85e6-7651ff87065d" />


Created welcome letters 
sudo -u student touch /home/student/workspace/welcome.txt
sudo -u student2 touch /home/student2/workspace/welcome.txt

### 4. Create & edited welcome letters
<img width="981" height="802" alt="Created welcome letters" src="https://github.com/user-attachments/assets/736e9173-6268-4130-bca2-242f2a510750" />


edited the welcome letters through bash 
sudo -u student nano /home/student/workspace/welcome.txt
sudo -u student2 nano /home/student2/worksapce/welcome.txt

Verification
Loged into student VM to verify access:
- student succesfully accessed their own workspace
- student was denied access to student2's workspace

- ### 5 Verification
- <img width="972" height="796" alt="Verification" src="https://github.com/user-attachments/assets/eb85d60f-9a4c-41a3-99cb-ee1f3922a693" />

This confirmed that the permissions and ownership were configured correctly

