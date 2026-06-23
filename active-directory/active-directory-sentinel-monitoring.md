# Active Directory Security Monitoring with Microsoft Sentinel

## Overview

This lab documents the integration of an on-premises Active Directory environment with Microsoft Sentinel for centralized security monitoring and log analysis. The environment consists of a Windows Server 2022 Domain Controller (DC01) and a Windows 11 Pro domain-joined workstation (WIN11-01) within the homesoc.local domain.

## Objective

The objective of this exercise was to onboard Active Directory assets into Microsoft Sentinel using Azure Arc, Azure Monitor Agent, and Data Collection Rules (DCRs) to collect and analyze Windows Security Events.

## Environment

### Domain Controller

* Hostname: DC01
* Operating System: Windows Server 2022
* Domain: homesoc.local
* Role: Active Directory Domain Services (AD DS)

### Workstation

* Hostname: WIN11-01
* Operating System: Windows 11 Pro
* Domain Joined: homesoc.local

### Azure Components

* Microsoft Sentinel
* Log Analytics Workspace (HomeSOC-LAW)
* Azure Arc
* Azure Monitor Agent (AMA)
* Data Collection Rule (HomeSOC-DCR)

## Implementation

### Azure Arc Onboarding

Both DC01 and WIN11-01 were onboarded to Azure Arc to enable centralized management and monitoring from Azure.

### Azure Monitor Agent Deployment

The Azure Monitor Agent was deployed to both systems to collect telemetry and Windows Event Logs.

### Data Collection Rule Configuration

The HomeSOC-DCR data collection rule was configured and associated with both systems to collect Security, Application, and System event logs.

### Log Ingestion Verification

Heartbeat data was successfully received from:

* DC01.homesoc.local
* WIN11-01.homesoc.local

Windows Security Events were successfully collected and stored within the Log Analytics Workspace.

## Security Events Observed

Examples of collected events include:

* Event ID 4624 – Successful Logon
* Event ID 4625 – Failed Logon
* Event ID 4634 – Logoff
* Event ID 4672 – Special Privileges Assigned
* Event ID 4768 – Kerberos Authentication Ticket Request
* Event ID 4769 – Kerberos Service Ticket Request

## Outcome

The Active Directory environment was successfully integrated with Microsoft Sentinel. Security logs from both the domain controller and domain-joined workstation were centralized within Azure, providing visibility into authentication activity, privilege assignments, and user behavior across the domain.

## Skills Demonstrated

* Active Directory Administration
* Azure Arc Onboarding
* Microsoft Sentinel Configuration
* Azure Monitor Agent Deployment
* Data Collection Rule Management
* Log Analytics
* Security Event Monitoring
* Kusto Query Language (KQL)
* Windows Event Analysis
