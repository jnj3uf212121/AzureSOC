# Building a SOC + Honeynet in Azure (Live Traffic)
![Cloud Honeynet / SOC](https://i.imgur.com/ZWxe03e.jpg)

## Project Overview
In this endeavor, I meticulously constructed and monitored a network environment that mimicked enterprise-level SOC operations, integrated with a Honeynet to capture and analyze malicious activities. The use of Azure's cloud capabilities allowed me to create a dynamic and scalable infrastructure that can handle live traffic and adapt to various attack scenarios.

## Key Features
- Virtual Machine Configuration: Configured Linux and Windows VMs, adjusting security settings to monitor and respond to traffic appropriately.
- Attack Simulation: Set up an Attack VM designed to launch simulated attacks on other VMs, creating an environment to study attack patterns and practice incident response.
- Azure Active Directory Management: Explored Azure AD's structure, creating and managing users with diverse permission sets to understand the impact of administrative roles on security.
- Centralized Logging: Leveraged Azure's Log Analytics Workspace for gathering and analyzing logs from all over the environment, providing a centralized point for security data.
- Threat Detection with Azure Sentinel: Utilized Azure Sentinel as a SIEM system to create attack maps, generate and manage alerts, and investigate malicious activities.
- Microsoft Defender for Cloud Integration: Ensured all security alerts from various sources were pushed into the Log Analytics Workspace for a unified threat management approach.
- Compliance and Standards: Emphasized adherence to NIST 800-61 for incident response and NIST 800-53 for establishing a robust cybersecurity framework within the environment.
- Live Traffic Management: Successfully managed and analyzed live traffic within the environment, simulating a real SOC's experience.

## Project Objectives
- Educate: Serve as an educational resource for those looking to understand the intricacies of SOC operations and Honeynet deployment.
- Demonstrate: Showcase the capabilities of Azure services in hosting and managing security operations.
- Innovate: Provide a platform for continuous improvement and experimentation with new security methodologies and tools.

## Project Achievements
- Established a realistic and secure virtual network environment.
- Demonstrated the ability to capture and analyze live traffic.
- Created and resolved simulated security incidents.
- Developed a comprehensive understanding of SOC and Honeynet operations.

## Tools and Technologies Used:
- Azure Cloud Services
- Virtual Machines (Windows and Linux)
- Azure Active Directory
- Azure Log Analytics
- Azure Sentinel
- Microsoft Defender for Cloud
- Kusto Query Language (KQL)
- Network Security Groups (NSGs)

## Attacks Maps created from Azure Sentinel Workbooks
![NSG Allowed Inbound Malicious Flows](https://drive.google.com/drive/u/0/my-drive)<br>
![Linux Syslog Auth Failures](https://drive.google.com/drive/u/0/my-drive)<br>
![Windows RDP/SMB Auth Failures](https://drive.google.com/drive/u/0/my-drive)<br>

## Metrics Before Hardening / Security Controls

The following table shows the metrics we measured in our insecure environment for 24 hours:
Start Time 2023-10-20 7:55
Stop Time 2023-03-16 17:04:29

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 19818
| Syslog                   | 6889
| SecurityAlert            | 2
| SecurityIncident         | 114
| AzureNetworkAnalytics_CL | 5328

## Metrics After Hardening / Security Controls

The following table shows the metrics we measured in our environment for another 24 hours, but after we have applied security controls:
Start Time 2023-03-18 15:37
Stop Time	2023-03-19 15:37

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 8500
| Syslog                   | 50
| SecurityAlert            | 0
| SecurityIncident         | 0
| AzureNetworkAnalytics_CL | 0
                                                                              
