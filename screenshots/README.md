(1) SSH Login to Cowrie Honeypot
Attacker successfully connects to the Cowrie SSH honeypot running on a non-standard port.
Technique: T1078 – Valid Accounts
(2) System Identity & OS Discovery
Attacker checks current user privileges and system information.
Techniques:
- T1033 – System Owner/User Discovery
- T1082 – System Information Discovery
(3) Privilege & Group Enumeration
Attacker enumerates user ID, groups, and privilege context.
Technique: T1033 – System Owner/User Discovery
(4) Local User Enumeration
Attacker lists system users via /etc/passwd.
Technique: T1087 – Account Discovery
(5) Process Discovery
Attacker inspects running processes to understand the environment.
Technique: T1057 – Process Discovery
(6) Network & Service Discovery
Attacker checks listening services and open ports.
Technique: T1016 – Network Discovery
(7) Cowrie Honeypot Running Status
Verification that Cowrie is actively running and capturing attacker activity.
Defensive Validation
(8) Cowrie Log Evidence
Recorded attacker commands and session metadata captured by Cowrie.
Data Source: Cowrie JSON Logs
