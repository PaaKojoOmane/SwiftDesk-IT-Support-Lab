# Project Overview

This project documents the build of a small Windows-based enterprise lab designed to reflect real IT Support work rather than exam-style exercises.

The goal of the lab is hands-on experience with common tasks performed in IT Support and junior infrastructure roles, including system setup, user access management, policy enforcement, troubleshooting, and documentation.

The environment was built gradually, with each phase validated before moving on. Decisions were made based on practicality and best practice rather than over-engineering the setup.

---

## Project Objectives

The objectives of this project are to:

- Build a functioning Active Directory domain from scratch  
- Support a Windows client within that domain  
- Manage users, groups, and access using structured methods (RBAC)  
- Implement file sharing with least-privilege NTFS permissions  
- Apply and verify departmental Group Policy settings  
- Document troubleshooting issues and fixes in a support-friendly way  
- Produce a clear GitHub portfolio with minimal but strong evidence screenshots  

---

## Lab Environment (Summary)

| Component | Details |
|---|---|
| Virtualisation | VMware Workstation |
| Domain | `swiftdesk.local` |
| Network | `10.88.0.0/24` (Host-Only / VMnet2) |
| Domain Controller | `SD-DC01` (Windows Server 2019) |
| Client | `SD-CLIENT01` (Windows 10) |

---

## Scope of the Lab

The lab simulates a small organisation with multiple departments and a central IT function.

It includes:

- One domain controller (SD-DC01)
- One domain-joined client machine (SD-CLIENT01)
- Department-based OU structure and security groups
- Department users (for realistic access testing)
- Centralised file shares with NTFS permissions
- Departmental Group Policy Objects

Imaging and deployment was explored as a learning phase and documented based on outcomes and lessons learned.

---

## Standards Used (How the Lab Was Kept Consistent)

### Naming conventions
- Servers: `SD-DC01`
- Clients: `SD-CLIENT01`
- Domain: `swiftdesk.local`
- Department security groups: `HR_Group`, `Finance_Group`, `Sales_Group`, `IT_Group`, `Mgmt_Group`
- GPO naming: `HR_Policy`, `Finance_Policy`, `Sales_Policy`, `IT_AdminPolicy`, `Management_Policy`

### Evidence (screenshots)
Screenshots are kept minimal and organised per phase:

- 3–4 screenshots per phase (Phase 6 can be 4–5)
- Stored in: `assets/screenshots/phase-1/` through `assets/screenshots/phase-9/`
- Screenshots focus on configuration proof and validation proof (not every click)

### Validation rule (how “done” is confirmed)
Work is only marked complete when verified using a practical check, for example:

- Domain join verified by logging in with domain credentials  
- Shares verified by accessing them as a standard user  
- GPOs verified using results (e.g., applied settings, mapped drives, policy results)  

---

## Project Phases (Full Map)

| Phase | Title | Outcome |
|---|---|---|
| Phase 0 | Project Overview | Scope, standards, and documentation map |
| Phase 1 | Virtualisation & Network Setup | VMware installed + Host-Only VMnet2 configured |
| Phase 2 | Domain Controller Deployment | Server 2019 installed + AD DS + DNS + domain created |
| Phase 3 | Client Build & Configuration | Windows 10 client built + baseline settings applied |
| Phase 4 | Client Domain Join & Verification | Client joined to domain + login/auth tested |
| Phase 5 | Users, Groups & OU Structure | OU structure + department users + security groups created |
| Phase 6 | File Sharing & NTFS Permissions | Department shares created + least-privilege access enforced |
| Phase 7 | Departmental Group Policy (GPOs) | Department GPOs created, linked, and validated |
| Phase 8 | Troubleshooting Scenarios | Common support issues reproduced and resolved with evidence |
| Phase 9 | Imaging & Deployment (Learning) | Audit Mode/Sysprep imaging concepts explored and documented |

---

## Approach Taken

Each phase focused on one core area (networking, server setup, client setup, access control, policy enforcement, etc.) and was validated before continuing.

Where issues occurred, they were investigated, resolved where appropriate, or documented when a rebuild was the better option. This reflects real IT Support decision-making rather than forcing broken configurations to work.

---

## Documentation Style

Screenshots and explanations are kept minimal and relevant.

Only key screenshots that demonstrate configuration or validation are included. This keeps the documentation easy to review while still providing evidence of work completed.

---

## Next Document

Proceed to:

- [Phase 1 – VMware & Network Setup](01-Phase-1-VMware-Network.md)

