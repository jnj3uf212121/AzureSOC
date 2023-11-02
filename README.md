# Building a SOC + Honeynet in Azure (Live Traffic)
![Cloud Honeynet / SOC](https://i.imgur.com/ZWxe03e.jpg)

## Introduction

This project focused on constructing a mini honeynet within the Microsoft Azure platform. The primary objective was to capture, analyze, and consolidate logs from several sources into a Log Analytics workspace. By leveraging these logs, Microsoft Sentinel facilitated the development of attack maps, alert triggers, and incident generation. Metrics of an insecure environment were measured over a period of 1 week, with security controls introduced after the first week to strengthen the virtual environment.

- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)

## Architecture of Honeypot:
- Virtual Network (VNet)
- Network Security Group (NSG)
- Virtual Machines (2 windows, 1 linux)
- Log Analytics Workspace
- Azure Key Vault
- Azure Storage Account
- Microsoft Sentinel

## Architecture Before Hardening / Security Controls:
![Architecture Diagram](https://i.imgur.com/aBDwnKb.jpg)
- The virtual environment was deployed and made publicly accessible. Microsoft Sentinel monitored this unsecured environment.

## Architecture After Hardening / Security Controls:
![Architecture Diagram](https://i.imgur.com/YQNa9Pp.jpg)
- The environment was fortified using NIST SP 800-53 Policy.

## Attack Maps Before Hardening / Security Controls
![NSG Allowed Inbound Malicious Flows](AzureSOC/nsg.PNG)<br>
![Linux Syslog Auth Failures](AzureSOC/linux.PNG)<br>
![Windows RDP/SMB Auth Failures](AzureSOC/windows.PNG)<br>

## Metrics Before Hardening / Security Controls

The following table shows the metrics we measured in our insecure environment for 24 hours:
Start Time 2023-10-20 07:55 
Stop Time 2023-10-27 07:55 

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 19818
| Syslog                   | 6889
| SecurityAlert            | 2
| SecurityIncident         | 114
| AzureNetworkAnalytics_CL | 5328

The following table shows the metrics we measured in our environment for another 24 hours, but after we have applied security controls:
Start Time 2023-10-28 08:55
Stop Time	2023-11-03 08:55

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 8500
| Syslog                   | 30
| SecurityAlert            | 0
| SecurityIncident         | 0
| AzureNetworkAnalytics_CL | 0

## Regulations used for Incidence Response and Security Implementation
- NIST SP 800-53, NIST SP 800-61

## Conclusion
The honeynet project in Microsoft Azure showcased the importance and efficiency of integrating proper security measures. After the application of more stringent controls:
- There was a 57.11% reduction in Windows Security Events, 99.56% in Linux Events, and 100% in security alerts, incidents, and malicious traffic.




