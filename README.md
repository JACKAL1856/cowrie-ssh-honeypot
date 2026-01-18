# cowrie-ssh-honeypot

SSH honeypot deployment using Cowrie with attacker behavior analysis and MITRE ATT&CK mapping.

##  Project Overview
This project demonstrates the deployment of a Cowrie-based SSH honeypot to capture, monitor, and analyze real-world attacker behavior.  
The honeypot simulates a vulnerable SSH service and records attacker interactions including login attempts, command execution, system enumeration, and network discovery.

The goal of this project is to gain hands-on experience with:
- Honeypot deployment
- Adversary behavior analysis
- Log-based threat detection
- MITRE ATT&CK technique mapping

---

##  Tools & Technologies
- **Cowrie SSH Honeypot**
- **Linux (Ubuntu/Kali)**
- **OpenSSH**
- **Python**
- **JSON Log Analysis**
- **MITRE ATT&CK Framework**

---

##  Honeypot Setup Summary
- Cowrie deployed on a non-standard SSH port (2222)
- Fake filesystem and user environment enabled
- Attacker sessions fully logged in JSON format
- Commands and session metadata captured for analysis

---

##  Attacker Activity Observed
The following attacker behaviors were captured during the simulation:

1. **SSH Login Attempt**
   - Successful authentication to the honeypot SSH service  
   - *MITRE ATT&CK:* T1078 – Valid Accounts

2. **System Identity & OS Discovery**
   - Commands: `whoami`, `uname -a`  
   - *MITRE ATT&CK:*  
     - T1033 – System Owner/User Discovery  
     - T1082 – System Information Discovery

3. **Privilege & Group Enumeration**
   - Command: `id`  
   - *MITRE ATT&CK:* T1033 – System Owner/User Discovery

4. **Local User Enumeration**
   - Command: `cat /etc/passwd`  
   - *MITRE ATT&CK:* T1087 – Account Discovery

5. **Process Discovery**
   - Command: `ps aux`  
   - *MITRE ATT&CK:* T1057 – Process Discovery

6. **Network & Service Discovery**
   - Command: `netstat -tulnp`  
   - *MITRE ATT&CK:* T1016 – Network Discovery

7. **Honeypot Verification**
   - Cowrie service verified as running and actively logging attacker sessions

8. **Log Evidence Collection**
   - Full attacker session details captured in Cowrie JSON logs

## Repository Structure

