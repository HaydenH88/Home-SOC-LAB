# Home-SOC-LAB

## Overview

This project documents the design and implementation of a Home Security Operations Center (SOC) using Microsoft Sentinel, Azure Log Analytics, Azure Arc, Sysmon, Windows Event Logs, and Kusto Query Language (KQL). The lab simulates a real-world SOC environment by collecting endpoint telemetry, creating custom detections, generating security incidents, and performing investigations.

## Objectives

* Collect endpoint telemetry using Sysmon and Windows Event Logs
* Centralize security logs in Microsoft Sentinel
* Develop KQL-based detection queries
* Create and validate Sentinel analytics rules
* Generate and investigate security incidents
* Perform threat hunting activities
* Map detections to MITRE ATT&CK techniques
* Document detection engineering and incident response workflows

## Lab Architecture

### Systems

* Windows 11 Endpoint
* Kali Linux Attack Platform
* macOS Management Workstation

### Security Tools

* Microsoft Sentinel
* Azure Log Analytics
* Azure Arc
* Azure Monitor Agent (AMA)
* Sysmon
* Kusto Query Language (KQL)
* Event Viewer

## Project Progress

* [x] Create GitHub Repository
* [x] Create Azure Resources
* [x] Install Sysmon
* [x] Verify Sysmon Logging
* [x] Connect Logs to Sentinel
* [x] Create KQL Queries
* [x] Build Detection Rules
* [x] Generate Test Activity
* [x] Investigate Incidents
* [x] Complete Documentation

## Implemented Detections

| Detection                               | Event ID   | MITRE ATT&CK           | Status |
| --------------------------------------- | ---------- | ---------------------- | ------ |
| Multiple Failed Logons                  | 4625       | T1110 - Brute Force    | Tested |
| New Local Administrator Account Created | 4720, 4732 | T1136 - Create Account | Tested |
| Privileged Logon                        | 4672       | T1078 - Valid Accounts | Tested |

## Detection Rules

See the `detection-rules` directory for full detection logic, KQL queries, testing procedures, and screenshots.

## Incident Reports

See the `incident-reports` directory for documented investigations and incident response activities.

## Skills Demonstrated

* Microsoft Sentinel Administration
* Azure Log Analytics
* Azure Arc Onboarding
* Azure Monitor Agent Deployment
* Windows Event Log Analysis
* Sysmon Configuration and Validation
* Detection Engineering
* KQL Query Development
* Security Monitoring
* Incident Response
* Threat Hunting
* MITRE ATT&CK Mapping

## Repository Structure

```text
Home-SOC-LAB/
├── architecture/
├── detection-rules/
├── incident-reports/
├── kql/
├── screenshots/
└── README.md
```

## Repository Contents

- [Detection Rules](./detection-rules)
- [Incident Reports](./incident-reports)
- [KQL Queries](./kql)
- [Architecture Diagram](./architecture)
