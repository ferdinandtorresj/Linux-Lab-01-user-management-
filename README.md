# Linux-Lab-01-user-management-
This lab demonstrates basic Linux user management, permissions, and workspace isolation using Bash.
---

## Overview

For this project, I was tasked to create two new users named **student** and **student2** utilizing Bash. The goal was to set up isolated workspaces, assign proper permissions, and verify access control between the two accounts.

---

## Commands Used

### 1. Create the users
'''bash 
sudo adduser student
sudo adduser student2

Created workspace folders
sudo mkdir /home/student/workspace
sudo mkdir /home/student2/workspace

Assigned permissions and ownership
sudo chown student:student /home/student/workspace
sudo chown student2:student2 /home/student2/workspace

Created welcome letters 
sudo -u student touch /home/student/workspace/welcome.txt
sudo -u student2 touch /home/student2/workspace/welcome.txt

edited the welcome letters through bash 
sudo -u student nano /home/student/workspace/welcome.txt
sudo -u student2 nano /home/student2/worksapce/welcome.txt

Verification
Loged into student VM to verify access:
- student succesfully accessed their own workspace
- student was denied access to student2's workspace
This confirmed that the permissions and ownership were configured correctly

