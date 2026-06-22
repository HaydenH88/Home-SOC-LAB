# Active Directory Home Lab

## Overview

This project expands the Home SOC environment by deploying a Windows Server 2022 Active Directory Domain Services (AD DS) environment.

## Objectives

- Install Windows Server 2022
- Deploy Active Directory Domain Services
- Create a new forest and domain
- Configure Organizational Units (OUs)
- Create users and security groups
- Join client systems to the domain
- Generate Active Directory security events
- Forward domain logs to Microsoft Sentinel
- Develop detection rules for Active Directory activity

## Lab Environment

### Domain Controller

- Windows Server 2022
- Hostname: DC01
- Domain: homesoc.local

### Security Tools

- Microsoft Sentinel
- Log Analytics Workspace
- Azure Monitor Agent
- KQL

## Project Progress

- [x] Create Windows Server VM
- [x] Install Windows Server 2022
- [x] Promote DC01 to Domain Controller
- [ ] Create Organizational Units
- [ ] Create Domain Users
- [ ] Create Security Groups
- [ ] Deploy Domain Workstation
- [ ] Join Workstation to Domain
- [ ] Connect Domain Logs to Sentinel
- [ ] Create AD Detection Rules

## Planned Detections

| Detection | Event ID |
|------------|-----------|
| New User Created | 4720 |
| User Added to Group | 4728 |
| User Deleted | 4726 |
| Password Reset | 4724 |
| Account Lockout | 4740 |
| Privileged Group Changes | 4732 |
