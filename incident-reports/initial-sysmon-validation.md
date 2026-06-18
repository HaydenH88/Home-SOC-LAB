# Initial Sysmon Validation

## Objective
Verify Sysmon installation and confirm telemetry collection.

## Actions Performed
- Downloaded Sysmon from Microsoft Sysinternals.
- Downloaded and applied the SwiftOnSecurity Sysmon configuration.
- Installed Sysmon as a Windows service.
- Verified Sysmon service status.
- Generated test activity on the host.

## Validation
The Sysmon Operational log successfully generated events after installation.

Observed event types included:
- Event ID 1 – Process Creation
- Event ID 3 – Network Connections
- Event ID 22 – DNS Queries (if present)

## Result
Sysmon telemetry collection is functioning correctly and ready for integration with Microsoft Sentinel.
