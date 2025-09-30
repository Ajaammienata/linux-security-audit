# Linux Security Audit — Accounts, Privileges & Permissions

This project demonstrates a hands-on security audit of a Linux system.  
The goal was to identify weak account configurations, excessive privileges, and misconfigured permissions that could lead to security risks.

---

## Objectives
- Audit system accounts and identify suspicious or insecure entries.  
- Review `sudo` privileges to detect excessive rights.  
- Analyse file/directory permissions for security misconfigurations.  
- Recommend improvements to strengthen system security.  

---

## Steps Performed

### 1. User Account Enumeration
- Listed all accounts on the system with `/etc/passwd`.  
- Identified accounts with login shells and checked for unnecessary/unused accounts.  

### 2. Privilege Review
- Reviewed `sudoers` file and group memberships.  
- Verified which accounts had administrative (`sudo`) rights.  

### 3. Permissions Analysis
- Inspected file and directory permissions for world-writable entries.  
- Checked system binaries and sensitive files for potential abuse.  

---

## Findings
- Accounts with interactive shells but no clear business need.  
- Multiple users with `sudo` rights — violating least privilege.  
- Files with insecure (`777`) permissions exposing data to all users.  

---

## Recommendations
- Disable or remove unused accounts.  
- Restrict `sudo` privileges to essential administrators only.  
- Correct permission misconfigurations to follow principle of least privilege.  
- Implement regular audits as part of baseline security hardening.  

---

## What I Learned
- How to enumerate accounts and interpret `/etc/passwd`.  
- The importance of auditing privilege escalation vectors (sudo, groups).  
- That permissions are a frequent weak spot in system security.  

---

## Ethical Note
This audit was performed in a safe lab environment on a Linux VM I controlled.  
No production systems were tested.
