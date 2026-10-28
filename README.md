# Week-12---DG-HUB-Intern

# SOC Final Capstone – Threat Detection & Incident Response

## Overview

This repository contains my submission for **Week 12** of the **DG Interns Hub Cyber Security Internship**.

The objective of this capstone was to perform a complete Security Operations Center (SOC) investigation in an authorized lab environment by combining **Snort IDS** and **Wazuh SIEM** to detect, investigate, correlate, respond to, and document a simulated cyber security incident.

---

## Objectives

- Build and validate a SOC lab environment.
- Simulate a controlled security incident.
- Detect malicious activity using Snort and Wazuh.
- Perform complete incident investigation.
- Correlate network and host-based alerts.
- Collect Indicators of Compromise (IOCs).
- Create an incident response plan.
- Generate a professional SOC incident ticket.
- Produce SOC metrics and analyst reflection.

---

# Lab Environment

- Ubuntu Linux Server
- Kali Linux Attacker Machine
- Wazuh Manager
- Wazuh Agent
- Wazuh Dashboard
- Snort IDS
- VirtualBox Host-Only Network
- OpenSSH Server

---

# SOC Architecture

```
Kali Linux
     │
     │
Reconnaissance
SSH Authentication
File Activity
     │
     ▼
Ubuntu Endpoint
     │
 ┌─────────────┐
 │Wazuh Agent  │
 └─────────────┘
     │
     ▼
Wazuh Manager
     │
     ▼
Wazuh Dashboard

Snort IDS monitors all network traffic.
```

---

# Incident Scenario

**Scenario D – Multi-Stage Incident**

The following authorized activities were performed inside the isolated SOC lab:

1. Network Reconnaissance (ICMP Ping)
2. Failed SSH Login Attempts
3. Successful SSH Login
4. Privilege Escalation (sudo)
5. File Creation
6. File Modification

---

# Detection

## Snort

- Detects ICMP Reconnaissance
- Custom Rule SID: **1000001**
- Generates Network IDS Alerts

## Wazuh

Monitors:

- SSH Authentication
- PAM Events
- Sudo Events
- File Integrity Monitoring (FIM)

Important Rule IDs:

- 5710
- 5760
- 5711
- 5763
- 5715
- 5501
- 5402
- 554
- 550

---

# Investigation

The incident investigation answers:

- What happened?
- When did it happen?
- Which host was affected?
- Source IP
- Destination IP
- User Account
- Triggered Alerts
- Evidence Collected
- IOC Analysis
- Impact Assessment
- True Positive Classification

---

# Snort + Wazuh Correlation

The investigation correlates:

- Network Reconnaissance
- Authentication Failures
- Successful Login
- Privilege Escalation
- File Integrity Monitoring Events

This provides complete visibility of the attack lifecycle.

---

# Indicators of Compromise (IOC)

Collected IOCs include:

- Source IP Address
- Destination IP Address
- Username
- SSH Port
- Protocol
- File Path
- Wazuh Rule IDs
- Snort SID
- Timestamp

---

# Incident Response

The report follows the standard Incident Response lifecycle:

1. Preparation
2. Identification
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

---

# SOC Incident Ticket

A professional SOC ticket was created including:

- Incident ID
- Severity
- Detection Source
- Description
- Investigation Findings
- Containment
- Recovery
- Recommendations
- Status

---

# SOC Metrics

The report includes:

- Total Events
- Total Alerts
- True Positives
- False Positives
- Critical Alerts
- High Alerts
- Medium Alerts
- Low Alerts
- Snort Detections
- Wazuh Detections
- Most Important IOC

---

# Repository Structure

```
Week-12---DG-HUB-Intern/
│
├── Report/
│   └── Week12_SOC_Final_Report.pdf
│
├── PPT/
│   └── Week12_SOC_Presentation.pptx
│
├── Screenshots/
│   ├── Wazuh Dashboard
│   ├── Wazuh Agent
│   ├── Snort Alerts
│   ├── Investigation
│   ├── Timeline
│   ├── IOC Analysis
│   ├── Incident Ticket
│   └── SOC Metrics
│
├── README.md
```

---

# Tools & Technologies

- Kali Linux
- Ubuntu Server
- Wazuh SIEM
- Wazuh Agent
- Wazuh Dashboard
- Snort IDS
- OpenSSH
- VirtualBox
- Linux CLI

---

# Learning Outcomes

Through this capstone, I learned:

- Security Operations Center (SOC) Workflow
- Network Intrusion Detection
- Host-Based Monitoring
- SIEM Operations
- Log Analysis
- Incident Investigation
- Threat Detection
- IOC Collection
- Alert Correlation
- Incident Response
- SOC Documentation

---

# Author

**Md Mohtasim**

Cyber Security Intern

DG Interns Hub

---

> **Disclaimer**
>
> This project was conducted entirely in an isolated and authorized virtual lab environment for educational purposes. No third-party systems, production infrastructure, or personal data were involved during testing.
