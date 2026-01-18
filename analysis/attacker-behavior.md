# Attacker Behavior Analysis

This document analyzes attacker behavior observed through the Cowrie SSH honeypot.

## Data Source
- Honeypot: Cowrie SSH
- Log file: `/home/cowrie/cowrie/var/log/cowrie/cowrie.json`
- Attacker machine: Kali Linux (simulated)

## Observed Session
- Source IP: 192.168.64.6
- Protocol: SSH
- Destination Port: 2222

## Commands Observed
The following commands were captured during the attacker session:

| Timestamp | Command | Purpose |
|---------|--------|---------|
| 2026-01-17 | `whoami` | Identify current user |
| 2026-01-17 | `uname -a` | Identify OS and kernel |
| 2026-01-17 | `ls` | Enumerate directory contents |
| 2026-01-17 | `pwd` | Identify working directory |

## Behavioral Analysis
The attacker followed a typical **post-compromise reconnaissance pattern**:
- User context discovery
- System fingerprinting
- Filesystem enumeration

This behavior is consistent with early-stage intrusion activity.
