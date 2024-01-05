# Building a SOC + Honeynet in Azure (Live Traffic)
![Cloud Honeynet / SOC](https://i.imgur.com/ZWxe03e.jpg)

Lab Overview
## 1. Infrastructure Setup
Created two virtual machines (VMs): one Linux and one Windows.
Exposed both VMs to the internet, forming a honeynet.
Established virtual networks for each VM and grouped them in resource groups.
Assigned both VMs to the same region.
Configured Network Security Groups (NSGs) to permit all inbound internet traffic.
Disabled the Windows VM firewall.

## 2. Database and Logging Configuration
Installed MS SQL Server and SQL Server Management Studio.
Connected SQL logs to the Windows Event Manager.

## 3. Simulated Attack Environment
Set up an additional VM to simulate attacks on the Windows VM, Linux VM, and SQL database.
Analyzed attack logs in the Event Manager.

## 4. Azure Active Directory Management
Reviewed Azure Active Directory components: tenant, subscription, and resource group.
Created users with varied permissions for access level testing.

## 5. Logging Mechanics
Conducted a mini-lesson on logging across different system layers.

## 6. Log Analytics and Sentinel Setup
Established a Log Analytics workspace for centralized log aggregation.
Integrated Azure Sentinel with the Log Analytics workspace.

## 7. Security Alert Integration
Enabled Microsoft Defender for Cloud to forward all security alerts from VMs and the SQL database to the Log Analytics workspace.

## 8. Storage and Data Collection
Created a storage account specifically for NSG flow logs.
Configured data collection rules in the Log Analytics workspace, both manually and through cloud services.
Tested KQL queries to ensure proper function.

## 9. KQL Proficiency
Deep dive into KQL, focusing on popular queries for log analysis.

## 10. Azure Sentinel Analysis
Utilized Azure Sentinel as a SIEM tool to:
Create attack maps from imported logs.
Simulate attack traffic from the attack VM.
Set up alerts for malicious activities and handle incidents.
Apply NIST 800-61 and NIST 800-53 standards for incident response and system hardening.
Analyze the impact of security measures.

## 11. Incident Response
Followed NIST 800-61 guidelines for incident handling:
Preparation: Ingested logs into the Log Analytics workspace.
Detection and Analysis: Managed incident severity, status, and ownership.
Containment, Eradication, and Recovery: Implemented a custom response playbook.
Post-Incident Activity: Documented findings and closed incidents in Sentinel.

## 12. Compliance and Security Posture
Enabled NIST 800-53 compliance measures in Microsoft Defender for Cloud.
Assessed the secure score in Microsoft Defender for Cloud.

## 13. NIST 800-53 Implementation
Focused on SC-7 (Boundary Protection):
Applied NSGs to subnets.
Enabled built-in firewalls and configured private links for public internet-facing resources.
Reviewed network topology for accuracy.
Additional Activities
Tenant-Level Logging
Tested user management at the tenant level.
Analyzed logs using custom KQL queries.
Subscription-Level Logging
Managed resources at the subscription level.
Observed changes through activity logs.
Resource-Level Logging
Enabled logging for a storage account and a key vault.
Generated logs through user interactions with these resources.
Security Alert Testing
Set up and tested alerts for various security incidents like brute force attacks and malware downloads.
Responded to incidents using NIST 800-61 guidelines.
Updated NSG rules and re-enabled the Windows VM firewall for enhanced security.

## Attacks Maps created from Azure Sentinel Workbooks
![NSG Allowed Inbound Malicious Flows](https://github.com/jnj3uf212121/images/blob/821268c33d0257d4bbf1d4caed508cfe23697895/nsg.PNG)<br>
![Linux Syslog Auth Failures](https://github.com/jnj3uf212121/images/blob/821268c33d0257d4bbf1d4caed508cfe23697895/linux.PNG)<br>
![Windows RDP/SMB Auth Failures](https://github.com/jnj3uf212121/images/blob/821268c33d0257d4bbf1d4caed508cfe23697895/windows.PNG)<br>

## Metrics Before Hardening / Security Controls

The following table shows the metrics we measured in our insecure environment for one week:
Start Time 2023-10-20 7:55
Stop Time 2023-03-16 7:55

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 19818
| Syslog                   | 6889
| SecurityAlert            | 2
| SecurityIncident         | 114
| AzureNetworkAnalytics_CL | 5328

## Metrics After Hardening / Security Controls

The following table shows the metrics we measured in our environment for another one week, but after we have applied security controls:
Start Time 2023-10-28 8:55
Stop Time	2023-11-03 8:55

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 8500
| Syslog                   | 50
| SecurityAlert            | 0
| SecurityIncident         | 0
| AzureNetworkAnalytics_CL | 0
                                                                              
