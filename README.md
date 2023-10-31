# Building a SOC + Honeynet in Azure (Live Traffic)
![Cloud Honeynet / SOC](https://i.imgur.com/ZWxe03e.jpg)

## Introduction

This project focused on constructing a mini honeynet within the Microsoft Azure platform. The primary objective was to capture, analyze, and consolidate logs from several sources into a Log Analytics workspace. By leveraging these logs, Microsoft Sentinel facilitated the development of attack maps, alert triggers, and incident generation. Metrics of an insecure environment were measured over a period of 2 weeks, with security controls introduced after the first week to strengthen the virtual environment.

- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)

## Architecture Before Hardening / Security Controls:
- The virtual environment was deployed and made publicly accessible. Microsoft Sentinel monitored this unsecured environment.

## Architecture After Hardening / Security Controls:
- The environment was fortified using NIST SP 800-53 Policy.

## Attack Maps Before Hardening:
- Images illustrating traffic, threat actor attempts to access the VMs, and database server.

