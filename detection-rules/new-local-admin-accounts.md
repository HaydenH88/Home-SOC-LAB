# New Local Administrator Account Created

## Objective

Detect the creation of new local user accounts that are added to the Administrators group, which may indicate persistence or privilege escalation activity.

## MITRE ATT&CK

* T1136 - Create Account
* TA0003 - Persistence
* TA0004 - Privilege Escalation

## Data Source

Windows Security Event Logs collected through Azure Monitor Agent and Data Collection Rules (DCR).

## Detection Logic

Event IDs monitored:

* 4720 - User account created
* 4732 - User added to local Administrators group

KQL Query:

```kusto
Event
| where EventID in (4720,4732)
| project TimeGenerated, Computer, EventID, RenderedDescription
```

## Test Procedure

1. Created a new local account:

```powershell
net user backupadmin P@ssw0rd123! /add
```

2. Added the account to the local Administrators group:

```powershell
net localgroup Administrators backupadmin /add
```

3. Verified event ingestion in Log Analytics.
4. Confirmed Microsoft Sentinel generated a High Severity incident.

## Results

The detection successfully identified the creation of a privileged local account and generated a Sentinel incident for analyst review.

## Lessons Learned

* Configured Azure Monitor Agent and DCRs for Windows Event collection.
* Developed and tested custom KQL detections.
* Validated end-to-end SIEM alerting and incident creation workflow.
