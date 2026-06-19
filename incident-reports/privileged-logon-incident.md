# Privileged Logon Incident Report

## Incident Summary

Microsoft Sentinel generated an alert for a privileged logon event on the monitored Windows endpoint. The alert was triggered when an administrator account successfully logged into the system and received elevated privileges.

## Alert Information

| Field            | Value                      |
| ---------------- | -------------------------- |
| Alert Name       | Privileged Logon Detection |
| Severity         | Medium                     |
| Host             | DESKTOP-ML09R3T            |
| Event ID         | 4672                       |
| Detection Source | Microsoft Sentinel         |

## Investigation

The investigation began by reviewing the associated Windows Security Event Logs collected in Log Analytics.

The following Event ID was observed:

* Event ID 4672 – Special privileges assigned to a new logon

Log analysis confirmed that the activity originated from a known administrator account created during lab testing. No evidence of unauthorized access or malicious activity was identified.

## Findings

* Privileged logon activity successfully detected.
* Microsoft Sentinel generated an incident as expected.
* Event logs were successfully collected through Azure Monitor Agent and Log Analytics.
* Detection rule functioned as designed.

## Impact Assessment

No business impact occurred. The activity was part of a controlled security monitoring exercise.

## Disposition

**Benign / Expected Activity**

The alert was generated during testing of a custom Microsoft Sentinel detection rule.

## Lessons Learned

* Validated end-to-end log collection.
* Confirmed successful detection of privileged account activity.
* Demonstrated incident generation and investigation workflow within Microsoft Sentinel.
