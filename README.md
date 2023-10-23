# Building a SOC + Honeynet in Azure (Live Traffic)
![Cloud Honeynet / SOC](https://i.imgur.com/ZWxe03e.jpg)

## Introduction

In today's digital era, the cloud infrastructure, especially platforms like Azure, plays a pivotal role in business continuity and security. My experience with Azure spans its comprehensive suite, from basic account management to intricate security configurations and analytics. The following tools were used:

- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)

## Azure Cloud, Virtual Machine & Active Directory Management:
- Created, managed, monitored Azure accounts, subscriptions, virtual machines, and Azure AD.
- Setup logging for Azure Active Directory (Microsoft Entra ID), enabling audit logs and signin logs.
- Demonstrated expertise in networking, setting up Network Security Groups (NSGs), and ensuring correct VM traffic flow.

## Azure Security, Logging & Monitoring Configuration:

- Integrated SQL Server with Windows Event Viewer.
- Established Azure Storage, configured blob diagnostics, and incorporated key vault instance logging.
- Utilized Microsoft Defender for Cloud across VMs, storage accounts, and SQL instances.

## Azure Sentinel & Log Analytics:

- Set up Log Analytics Workspace and connected it to Azure Sentinel.
- Uploaded Geo-Data files to Azure Storage and created geoip watchlist.
- Utilized pre-built JSON maps to create visualization workbooks in Azure Sentinel, showcasing malicious traffic targeting resources.
- Demonstrated proficiency in Kusto Query Language, crafting specialized queries for diverse scenarios.

## Azure Sentinel Visualization & Map Creation:

- Developed and implemented four distinct workbooks in Azure Sentinel that visualized various types of malicious global traffic.
- Ensured accurate log ingestion through Sentinel by utilizing the integrated Log Analytics Workspace.
- Verified and rectified logging configurations for Microsoft Defender for Cloud, SQL Server, and NSG Flow Logs.

## Conclusion
In essence, my work with Azure underscores a holistic approach to cloud infrastructure management and security. By seamlessly blending the creation, monitoring, and visualization components, I ensure not only a robust digital ecosystem but also clarity in deciphering intricate data patterns. As the digital landscape continues to evolve, I remain committed to harnessing the power of platforms like Azure to drive both efficiency and security in all my endeavors.
