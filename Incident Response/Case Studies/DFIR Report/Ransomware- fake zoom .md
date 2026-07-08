# DFIR Report #1

## Executive Summary

What happened?

---

## Detection

How was the incident initially detected?

Who detected it?

What alert triggered the investigation?

Which security tool detected it?

- SIEM
- EDR
- IDS
- IPS
- Firewall
- Antivirus
- User Report
- Threat Intelligence

Could the attack have been detected sooner?

---

## Initial Access

How did the attacker first get inside?

MITRE ATT&CK Technique

Evidence

How could this have been prevented?

---

## Timeline

List every important event in chronological order.

Time

Action

Evidence

---

## Execution

What did the attacker execute?

PowerShell?

CMD?

Scripts?

Malware?

Living off the Land Binaries (LOLBins)?

Evidence?

---

## Persistence

How did they survive a reboot?

Scheduled Task?

Registry?

Service?

Startup Folder?

New Account?

Evidence?

---

## Privilege Escalation

How did they obtain administrator rights?

Local Admin?

Domain Admin?

Exploit?

Credential Theft?

Evidence?

---

## Defense Evasion

How did they avoid detection?

Disabled AV?

Disabled Defender?

PowerShell Obfuscation?

Deleted Logs?

Renamed Files?

Evidence?

---

## Credential Access

Were credentials stolen?

LSASS?

Mimikatz?

Kerberoasting?

NTDS.dit?

Browser Passwords?

Evidence?

---

## Discovery

What information did they collect?

Users?

Groups?

Shares?

Computers?

Processes?

Network?

Domain Trusts?

Evidence?

---

## Lateral Movement

How did they move?

RDP?

SMB?

PsExec?

WMI?

WinRM?

Remote Services?

Evidence?

---

## Collection

What data did they gather?

Documents?

Financial?

Databases?

Email?

Evidence?

---

## Command and Control (C2)

How did they communicate?

DNS?

HTTPS?

Reverse Shell?

Beacon?

Evidence?

---

## Exfiltration

Did they steal data?

How?

Cloud?

FTP?

HTTPS?

Dropbox?

Evidence?

---

## Impact

What damage occurred?

Encryption?

Data Theft?

Service Disruption?

Account Creation?

Evidence?

---

# Windows Artifacts

Which Windows artifacts were important?

Windows Event Logs

Sysmon

Registry

Services

Scheduled Tasks

PowerShell Logs

Prefetch

Amcache

Shimcache

MFT

USN Journal

---

# Security Controls

Which technologies detected the attack?

Firewall

IDS

IPS

EDR

XDR

SIEM

SOAR

Defender

Email Security

NAC

VPN

---

# MITRE ATT&CK Mapping

Initial Access

Execution

Persistence

Privilege Escalation

Defense Evasion

Credential Access

Discovery

Lateral Movement

Collection

Command and Control

Exfiltration

Impact

---

# Incident Response

## Identification

How did we know something was wrong?

---

## Containment

Immediate actions?

Isolate endpoint?

Disable account?

Block IP?

Disconnect server?

---

## Eradication

Remove malware?

Delete persistence?

Patch vulnerability?

Reset passwords?

---

## Recovery

Restore from backup?

Reconnect systems?

Monitor environment?

Validate integrity?

---

## Lessons Learned

What failed?

What worked?

What controls should be improved?

What monitoring should be added?

How could this have been prevented?

---

# Indicators of Compromise (IOCs)

IPs

Domains

URLs

Hashes

File Names

Registry Keys

Processes

Services

Scheduled Tasks

---

# Detection Opportunities

What alerts could have been written?

Sigma Rules

YARA Rules

SIEM Detection

Sysmon Detection

PowerShell Detection

EDR Detection

---

# Interview Questions

If I were the Security Engineer...

What would I do first?

What logs would I review?

What would I preserve?

Who would I notify?

What would I isolate?

How would I verify the attacker is gone?

---

# Personal Notes

What did I learn?

What do I still need to research?

How would I improve our security posture?

#Reference Location
DFIR
https://thedfirreport.com/company/about-us/?utm_source=chatgpt.com
