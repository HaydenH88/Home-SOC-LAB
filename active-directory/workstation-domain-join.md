# Workstation Domain Join

## Overview

This lab demonstrates the process of joining a Windows 11 Pro workstation to the Active Directory domain hosted on the Windows Server 2022 Domain Controller (DC01).

## Objective

* Configure a Windows 11 Pro workstation.
* Verify network connectivity to the Domain Controller.
* Configure DNS to use the Domain Controller.
* Join the workstation to the Active Directory domain.
* Verify successful domain membership.

## Environment

### Domain Controller

* Hostname: DC01
* Operating System: Windows Server 2022
* Domain: homesoc.local
* IP Address: 10.0.2.15

### Workstation

* Hostname: WIN11-01
* Operating System: Windows 11 Pro
* IP Address: 10.0.2.3

## Configuration Steps

### 1. Verify Connectivity

On WIN11-01, verify communication with the Domain Controller:

```cmd
ping 10.0.2.15
```

Successful replies confirmed network connectivity.

### 2. Configure DNS

The workstation initially used the home router for DNS resolution, preventing Active Directory domain discovery.

Updated the IPv4 settings to use the Domain Controller as the preferred DNS server:

```text
Preferred DNS Server: 10.0.2.15
```

Verified DNS resolution:

```cmd
nslookup homesoc.local
```

### 3. Join the Domain

Opened System Properties:

```text
sysdm.cpl
```

Navigated to:

```text
Computer Name → Change
```

Selected:

```text
Member of: Domain
```

Entered:

```text
homesoc.local
```

Authenticated using domain administrator credentials.

### 4. Reboot Workstation

Restarted WIN11-01 to complete domain membership changes.

### 5. Verify Domain Membership

Logged into the workstation using a domain account:

```text
HOMESOC\jsmith
```

Confirmed successful authentication.

Verified WIN11-01 appeared in:

```text
Active Directory Users and Computers
→ Computers
```

## Results

The workstation successfully joined the Active Directory domain and was able to authenticate domain users. DNS resolution, domain discovery, and authentication services were functioning correctly.

## Skills Demonstrated

* Active Directory Administration
* DNS Configuration
* Windows Domain Management
* Network Troubleshooting
* Windows Server 2022
* Windows 11 Administration

## Screenshots

### Domain Join Configuration

![Domain Join](../screenshots/domain-join.png)

### Successful Domain Membership

![Domain Joined](../screenshots/domain-membership.png)

### Computer Object in Active Directory

![Computer Object](../screenshots/ad-computer-object.png)

