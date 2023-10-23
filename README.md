# Building a SOC + Honeynet in Azure (Live Traffic)
![Cloud Honeynet / SOC](https://i.imgur.com/ZWxe03e.jpg)

## Introduction

In this project, I build a mini honeynet in Azure and ingest log sources from various resources into a Log Analytics workspace, which is then used by Microsoft Sentinel to build attack maps, trigger alerts, and create incidents. I measured some security metrics in the insecure environment for 24 hours, apply some security controls to harden the environment, measure metrics for another 24 hours, then show the results below. The metrics we will show are:

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

In this project, a mini honeynet was constructed in Microsoft Azure and log sources were integrated into a Log Analytics workspace. Microsoft Sentinel was employed to trigger alerts and create incidents based on the ingested logs. Additionally, metrics were measured in the insecure environment before security controls were applied, and then again after implementing security measures. It is noteworthy that the number of security events and incidents were drastically reduced after the security controls were applied, demonstrating their effectiveness.

It is worth noting that if the resources within the network were heavily utilized by regular users, it is likely that more security events and alerts may have been generated within the 24-hour period following the implementation of the security controls.
