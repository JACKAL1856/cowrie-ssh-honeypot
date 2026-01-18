# MITRE ATT&CK Mapping

This document maps observed attacker behavior from the Cowrie SSH honeypot to the MITRE ATT&CK framework.

## Data Source
- Honeypot: Cowrie SSH
- Log file: `/home/cowrie/cowrie/var/log/cowrie/cowrie.json`
- Observed attacker session via SSH (port 2222)

---

## Technique Mapping

| Command Observed | MITRE Technique ID | Technique Name | Tactic |
|-----------------|------------------|---------------|--------|
| `whoami` | T1033 | System Owner/User Discovery | Discovery |
| `uname -a` | T1082 | System Information Discovery | Discovery |
| `ls` | T1083 | File and Directory Discovery | Discovery |
| `pwd` | T1083 | File and Directory Discovery | Discovery |

---

## Analysis

The attacker demonstrated **early-stage post-compromise discovery behavior**, commonly observed after initial access.

### Key Observations
- No privilege escalation attempts observed
- No lateral movement detected
- Activity limited to system and filesystem reconnaissance

### Threat Context
This behavior aligns with **Discovery-phase tactics** used by attackers to:
- Understand system identity
- Identify OS and kernel
- Explore filesystem structure

Such behavior is often a precursor to:
- Credential harvesting
- Privilege escalation
- Payload deployment

---

## Defensive Value

Mapping honeypot telemetry to MITRE ATT&CK enables:
- Faster incident triage
- Improved SOC alert classification
- Behavioral threat hunting
