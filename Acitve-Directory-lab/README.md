# active-directory-home-lab
Windows server Active Directory lab demonstrating user management, GPO, RBAC and access management.

**Overview**
This project demonstrates a Window Server Active Directory environment built to simulate a real enterprise setup. The lab is focused on roles of help desk and sysadmin.

**Lab Environment**
Windows Server 2019 (Domain Controller)
Windows 10 pro (Client)
Oracle Virtualbox
Domain Name: lab.local

**Active Directory Structure**
**Organizational Units (OUs)**
-staffs
**Groups**
-Engineer
-It
**Users**
-Client1
-Client2

Permissions were assigned based on Groups not individual user. OUs were used to assign GPO.

**Group Policy Objectives**
The following GPOs were configured:
Password Complexity and account lockout policy.
USB storage disabled
Desktop settings and Control panel restriction for non-admin.

**File Shares and Permission**
Created shared folders on the Domain Controllers:
\\it\itsec
\\engineer\tools
Access control was made using the shared permission and NTFS mapped to security group.

**Testing and Validation**
logged in through different domains user to cerify access permission and password policies.
Confirmed access denial for unauthorized users on contol panel and desktop settings.
Simulated common helpdesk tasks like password reset and account lock.

**Screenshots**
Screenshots included:
AD and group user configuration
GPO settings
Access allowed and access denial scenarios.


**Troubleshoot**
Initially, account lockout didnt trigger because lockout threshold was set to "never" in the default domain policy. After configuring the whole thing worked well along with lockout threshold and duration.


