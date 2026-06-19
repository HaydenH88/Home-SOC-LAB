# Home SOC Lab

## Overview
This project documents the creation of a Home Security Operations Center (SOC) using Microsoft Sentinel, Sysmon, Windows Event Logs, and Kusto Query Language (KQL).

## Objectives
- Collect endpoint telemetry using Sysmon
- Centralize logs in Microsoft Sentinel
- Develop KQL detection queries
- Create analytics rules and incidents
- Perform threat hunting activities
- Map detections to MITRE ATT&CK techniques

## Lab Environment

### Systems
- Windows 11 Desktop
- Kali Linux
- macOS Management Workstation

### Security Tools
- Microsoft Sentinel
- Sysmon
- Azure Monitor Agent
- KQL
- Event Viewer

## Project Progress

- [x] Create GitHub Repository
- [x] Create Azure Resources
- [x] Install Sysmon
- [x] Verify Sysmon Logging
- [x] Connect Logs to Sentinel
- [x] Create KQL Queries
- [x] Build Detection Rules
- [x] Generate Test Attacks
- [x] Investigate Incidents
- [x] Complete Documentation


## Implemented Detections

### 1. Multiple Failed Logons
- Data Source: Windows Security Logs
- Event ID: 4625
- MITRE ATT&CK: T1110 (Brute Force)
- Status: Tested and validated

### 2. New Local Administrator Account Created
- Data Source: Windows Security Logs
- Event IDs: 4720, 4732
- MITRE ATT&CK: T1136 (Create Account)
- Status: Tested and validated

## Detection Rules

| Detection | Event ID |
|------------|-----------|
| Multiple Failed Logons | 4625 |
| New Local Administrator Account Created | 4720 |
| Privileged Logon | 4672 |

## Skills Demonstrated

- Microsoft Sentinel
- Log Analytics
- KQL
- Azure Arc
- Windows Event Logging
- Detection Engineering
- Incident Response
- SIEM Alerting
