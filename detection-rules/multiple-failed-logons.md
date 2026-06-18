Detection Name: Multiple Failed Logons

Objective:
Detect potential brute-force activity against Windows systems.

Data Source:
Windows Security Events via Azure Monitor Agent

Event ID:
4625 - Failed Logon

KQL Query:

Event
| where EventID == 4625
| where TimeGenerated > ago(10m)
| summarize FailedAttempts=count() by Computer
| where FailedAttempts >= 3

MITRE ATT&CK:
T1110 - Brute Force

Result:
Successfully generated incidents in Microsoft Sentinel after repeated failed authentication attempts on the monitored Windows endpoint.
