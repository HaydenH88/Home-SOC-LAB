# KQL Queries

This directory contains the Kusto Query Language (KQL) queries used throughout the Home-SOC-LAB project.

## Queries

| File | Purpose |
|--------|---------|
| failed-logons.kql | Detect multiple failed logon attempts (Event ID 4625) |
| new-local-admin-account.kql | Detect local administrator account creation (Event IDs 4720, 4732) |
| privileged-logon.kql | Detect privileged account logons (Event ID 4672) |

## Platform

- Microsoft Sentinel
- Azure Log Analytics

## Data Sources

- Windows Security Event Logs
- Azure Monitor Agent
