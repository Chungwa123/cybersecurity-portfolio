**WINDOWS LOG ANALYSIS PROJECT**

**Objective**
To analyse Windows logs and identify Suspicious login acitivities

**Tools Used**
-Wazuh (SIEM)
-Kali Linux
-Evil-WinRM
-Virtual Machine

**What I Did**
-Setup up a Windows 10 Virtual Machine along with exposed WinRM  
-Sucessfully attacked and got access using crackmapexec with custom passwordlist
-Analysed the failed login attempts through the Wazuh 

**Outcome**
Wazuh logged all the failed login attempts along and detected the exact chain of attack. Failed login attempts along with successful logins precess were created with rule ID like 60122, 60121 and 5900. The dashboard made it easier to understand and visualize the attack since there was spike in login attempts due to failed authentication logs within a short span of time.

**Key learnings**
This gave me a bigger picture on how we can see live attacks through SIEM tools like Wazuh and how logs work. And how failed logins can be analysed to understand whether it is a genuine mistake or a attack.
