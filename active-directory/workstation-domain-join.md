# Workstation Domain Join

## Overview

This lab documents the process of joining a Windows 11 Pro workstation (WIN11-01) to the Active Directory domain hosted on the Windows Server 2022 Domain Controller (DC01).

## Objective

The objective of this exercise was to configure a Windows 11 workstation, establish communication with the Domain Controller, and join the workstation to the `homesoc.local` Active Directory domain.

## Environment

### Domain Controller

* Hostname: DC01
* Operating System: Windows Server 2022
* Domain: homesoc.local

### Workstation

* Hostname: WIN11-01
* Operating System: Windows 11 Pro

## Domain Join Process

1. Verified network connectivity between WIN11-01 and DC01.
2. Configured the workstation to use the Domain Controller as its DNS server.
3. Opened System Properties and selected the option to join a domain.
4. Entered the domain name `homesoc.local`.
5. Authenticated using domain administrator credentials.
6. Successfully joined the workstation to the domain and restarted the system.

## Verification

After rebooting, the workstation was successfully joined to the domain and appeared as a computer object within Active Directory Users and Computers on the Domain Controller.

### Domain Join Configuration

![WIN11-01 Domain Join](../screenshots/win11-domain-join.png)

*Figure 1. WIN11-01 successfully joined to the homesoc.local domain.*

### Computer Object in Active Directory

![WIN11-01 Computer Object](../screenshots/win11-01-computer-object.png)

*Figure 2. WIN11-01 computer account automatically created and visible within Active Directory.*

## Results

The workstation was successfully joined to the `homesoc.local` domain. Communication between the workstation and Domain Controller was verified, DNS resolution was functioning correctly, and Active Directory automatically created the computer object for WIN11-01.

## Skills Demonstrated

* Active Directory Administration
* Windows Server 2022
* Windows 11 Administration
* DNS Configuration
* Domain Management
* Network Troubleshooting
* Enterprise Identity Management
