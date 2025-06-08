# SecurityMonitor
# Cloud Security Monitoring with Microsoft Azure
A hands-on cybersecurity project built using Microsoft Azure to simulate a secure cloud infrastructure, monitor for threats, and respond to security incidents in real time.

## Objective

The goal of this project was to:
- Set up a secure cloud environment using Microsoft Azure.
- Deploy virtual machines and simulate real-world infrastructure.
- Detect potential vulnerabilities using built-in Azure security tools.
- Visualize security incidents and perform basic remediation.

## Tools & Services Used
- **Microsoft Azure**
  - Azure Virtual Machines (Linux/Windows)
  - Microsoft Sentinal
  - Log Analytics Workspace
  - Azure Monitor
- **Languages/Queries**
  - KQL (Kusto Query Language)

## KQL Query – Detecting Successful Logins

This query filters security events to show only **successful login attempts** that were not made by system accounts:

```kql
SecurityEvent
| where Activity contains "success" and Account !contains "system"
