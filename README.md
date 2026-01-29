<div align="center">

# ⧉ SwiftDesk IT Support Lab

### A hands-on enterprise-style IT Support portfolio  
designed to replicate **real-world service desk and junior systems administration work**.

This project demonstrates how Windows enterprise environments are **planned, built, secured, supported, and documented** in business settings — using Active Directory, Group Policy, NTFS permissions, and structured troubleshooting.

<br/>

<!-- Optional banner (add later if desired) -->
<!-- <img src="assets/banner-swiftdesk.png" width="100%" /> -->

<br/>

![VMware](https://img.shields.io/badge/VMware-Lab-607078?logo=vmware&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows%20Server-2019-0078D4?logo=windows&logoColor=white)
![Windows 10](https://img.shields.io/badge/Windows-10-0078D4?logo=windows&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active%20Directory-AD%20DS-2E2E2E)
![Group Policy](https://img.shields.io/badge/Group%20Policy-GPOs-5C2D91)

<br/>

📘 **Start here:** [Project Overview](docs/00-Project-Overview.md)  
📂 **Jump to:** [Documentation Index](#-documentation-index) • [Lab Environment](#-lab-environment) • [Core Highlights](#-core-highlights)

</div>

---

## 🔬 Lab Environment

| Component | Details |
|---|---|
| Domain | `swiftdesk.local` |
| Network | `10.88.0.0/24` (Host-Only / VMnet2) |
| Domain Controller | `SD-DC01` (Windows Server 2019) |
| Client | `SD-CLIENT01` (Windows 10) |
| Platform | VMware Workstation |

---

## ⭐ Core Highlights (What Recruiters Care About)

✔ Designed and deployed a **Windows Server 2019 Active Directory domain**, including DNS configuration and domain validation  
✔ Installed, configured, and joined a **Windows 10 client** to the domain, validating authentication using domain user accounts  
✔ Built a structured **OU hierarchy** and implemented **role-based access control (RBAC)** using security groups  
✔ Configured **centralised file shares** with NTFS permissions, applying the **principle of least privilege**  
✔ Implemented **departmental Group Policy Objects (GPOs)** to manage user environments and enforce configuration standards  
✔ Validated access, permissions, and policies directly from the **client perspective**, simulating real end-user experience  
✔ Documented **real troubleshooting scenarios**, including configuration errors, access issues, and corrective decisions  
🧪 Explored **imaging and Sysprep concepts** as an advanced learning phase, documenting outcomes and lessons learned

---

## ⌂ Skills Demonstrated (Mapped to Project Phases)

- **Virtualisation & Networking (Phase 1)**  
  Built an isolated lab environment using VMware Workstation with Host-Only networking (VMnet2), applying foundational IP addressing and connectivity concepts.

- **Windows Server Deployment (Phase 2)**  
  Installed and configured Windows Server 2019, promoted the server to a domain controller, and implemented core Active Directory Domain Services (AD DS) and DNS functionality.

- **Client Build & Configuration (Phase 3)**  
  Installed and prepared Windows 10 client systems, configured networking, and applied enterprise naming and baseline configuration prior to domain integration.

- **Domain Join & Authentication (Phase 4)**  
  Joined client machines to the Active Directory domain, validated DNS dependencies, and verified authentication using domain user accounts.

- **Active Directory Organisation (Phase 5)**  
  Designed and implemented a structured OU hierarchy, created users and department security groups, and managed group membership using a role-based access control (RBAC) approach.

- **File Sharing & Access Control (Phase 6)**  
  Created centralised file shares and applied NTFS permissions using security groups, enforcing least-privilege access and validating results from the client.

- **Group Policy Management (Phase 7)**  
  Designed, linked, and tested departmental Group Policy Objects (GPOs) to control user environments and apply consistent configuration standards.

- **Troubleshooting & Validation (Phase 8)**  
  Identified and resolved common domain, access, and configuration issues, validated fixes, and documented outcomes clearly.

- **Imaging & Deployment Concepts (Phase 9 – Learning Phase)**  
  Explored enterprise imaging concepts such as Audit Mode and Sysprep, encountered real deployment issues, and documented lessons learned and rebuild decisions.

---

## ✅ Project Progress

| Phase | Status |
|---|---|
| Phase 0 – Project Overview | ✅ |
| Phase 1 – Virtualisation & Network Setup | ✅ |
| Phase 2 – Domain Controller Deployment (AD DS + DNS) | ✅ |
| Phase 3 – Client Build & Configuration | ✅ |
| Phase 4 – Client Domain Join & Verification | ✅ |
| Phase 5 – Users, Groups & OU Structure | ✅ |
| Phase 6 – File Sharing & NTFS Permissions | ⭐ **Completed (Core IT Support Phase)** |
| Phase 7 – Departmental Group Policy (GPOs) | ⏳ Documenting |
| Phase 8 – Troubleshooting Scenarios | ⏳ |
| Phase 9 – Imaging & Deployment (Audit Mode / Sysprep) | ⚠ Learning Phase |

---

## 📂 Documentation Index

> Each phase is documented with **important screenshots only**  
> (3–4 per phase, Phase 6 includes 4–5).

| Phase | Description |
|---|---|
| 00 | [Project Overview](docs/00-Project-Overview.md) |
| 01 | [VMware & Network Setup](docs/01-Phase-1-VMware-Network.md) |
| 02 | [Domain Controller (AD DS + DNS)](docs/02-Phase-2-DC01-AD-DNS.md) |
| 03 | [Client Build & Configuration](docs/03-Phase-3-Client-Build.md) |
| 04 | [Client Domain Join & Verification](docs/04-Phase-4-Client-Domain-Join.md) |
| 05 | [Users, Groups & OU Structure](docs/05-Phase-5-Users-Groups-OU.md) |
| 06 | [File Sharing & NTFS Permissions](docs/06-Phase-6-Shares-NTFS.md) |
| 07 | [Departmental Group Policy](docs/07-Phase-7-Department-GPOs.md) |
| 08 | [Troubleshooting](docs/08-Phase-8-Troubleshooting.md) |
| 09 | [Imaging & Deployment](docs/09-Phase-9-Imaging-Deployment.md) |

---

## 🗂️ Evidence & Screenshots

| Folder | Purpose |
|---|---|
| assets/screenshots/phase-1 | VMware & network configuration |
| assets/screenshots/phase-2 | Domain controller setup |
| assets/screenshots/phase-3 | Client build & preparation |
| assets/screenshots/phase-4 | Domain join verification |
| assets/screenshots/phase-5 | Users, groups & OU structure |
| assets/screenshots/phase-6 | File sharing & NTFS permissions |
| assets/screenshots/phase-7 | Departmental Group Policy |
| assets/screenshots/phase-8 | Troubleshooting evidence |
| assets/screenshots/phase-9 | Imaging & deployment |


 ## 📌 Outcome
This project serves as a **job-ready IT Support portfolio**, demonstrating the ability to build, support, secure, and document a Windows enterprise environment. It reflects how IT Support professionals work in practice: planning configurations, validating access, troubleshooting issues, and documenting decisions clearly for future reference and handover. The lab and documentation are suitable as supporting evidence for **IT Support, Desktop Support, and Junior Systems Administrator roles**.