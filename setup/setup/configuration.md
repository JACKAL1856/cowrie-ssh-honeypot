# Cowrie Configuration

This document describes the configuration of the Cowrie SSH honeypot used to capture attacker behavior.

## SSH Deception Strategy
 Cowrie SSH service is configured to listen on port **2222**
 The real SSH service on port 22 remains protected
 Attackers are tricked into interacting with a fake shell environment

## Configuration Details
 SSH Listen Port: 2222
 Default credentials accepted (honeypot behavior)
 All attacker commands are logged in JSON format

## Log Files
 Command and session logs:
   `/home/cowrie/cowrie/var/log/cowrie/cowrie.json`
 Session metadata:
   Source IP
   Timestamp
   Executed commands

## Verification
 Cowrie service verified as running
 Successful SSH connection observed from attacker machine (Kali Linux)
 Attacker commands captured and stored in logs
