## Week 4 Homework Submission File: Linux Systems Administration

Please edit this file by adding the solution commands on the line below the prompt.

Save and submit the completed file for your homework submission.


### Step 1: Ensure/Double Check Permissions on Sensitive Files

1. Permissions on `/etc/shadow` should allow only `root` read and write access.

    - Command to inspect permissions: ls -l shadow

    - Command to set permissions (if needed): sudo chmod 600 shadow

2. Permissions on `/etc/gshadow` should allow only `root` read and write access.

    - Command to inspect permissions: ls -l gshadow

    - Command to set permissions (if needed): chmod 600 gshadow

3. Permissions on `/etc/group` should allow `root` read and write access, and allow everyone else read access only.

    - Command to inspect permissions: ls -l group

    - Command to set permissions (if needed): chmod 644 group 
    
4. Permissions on `/etc/passwd` should allow `root` read and write access, and allow everyone else read access only.

    - Command to inspect permissions: ls -l passwd

    - Command to set permissions (if needed):  chmod 644 passwdadd

### Step 2: Create User Accounts

1. Add user accounts for `sam`, `joe`, `amy`, `sara`, and `admin`.

    - Command to add each user account (include all five users): 
    - sudo useradd sam, sudo useradd amy, sudo useradd sara, sudo   useradd admin
  

2. Ensure that only the `admin` has general sudo access.

    - Command to add `admin` to the `sudo` group: sudo usermod -aG sudo admin 

### Step 3: Create User Group and Collaborative Folder

1. Add an `engineers` group to the system.

    - Command to add group: sudo usermod -aG engineers

2. Add users `sam`, `joe`, `amy`, and `sara` to the managed group.

    - Command to add users to `engineers` group (include all four users): sudo usermod -aG engineers sam, sudo usermod -aG engineers joe, sudo usermod -aG engineers amy, sudo usermod -aG engineers sara

3. Create a shared folder for this group at `/home/engineers`.

    - Command to create the shared folder: mkdir engineers

4. Change ownership on the new engineers' shared folder to the `engineers` group.

    - Command to change ownership of engineer's shared folder to engineer group:  sudo chgrp engineers engineers

### Step 4: Lynis Auditing

1. Command to install Lynis: sudo apt install lynis

2. Command to see documentation and instructions: cd lynis, cat default.prf

3. Command to run an audit: sudo lynis --auditor cisco

4. Provide a report from the Lynis output on what can be done to harden the system. 

    - Screenshot of report output:
    -  2022-01-20 00:03:40 Hardening: assigned partial number of hardening points (1 of 3) Currently having 197 points (out of 344)2022-01-20 00:03:40 Hardening: assigned partial number of hardening points (2 of 3). Currently having 199 points (out of 347)
2022-01-20 00:03:41 Hardening: assigned partial number of hardening points (2 of 3). Currently having 201 points (out of 350)
2022-01-20 00:03:41 Hardening: assigned maximum number of hardening points for this item (3). Currently having 204 points (out of 353)


### Bonus
1. Command to install chkrootkit:

2. Command to see documentation and instructions:

3. Command to run expert mode:

4. Provide a report from the chrootkit output on what can be done to harden the system.
    - Screenshot of end of sample output:

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
