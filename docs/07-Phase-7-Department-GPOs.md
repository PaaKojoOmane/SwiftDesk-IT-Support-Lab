# Phase 7 – Departmental Group Policy Objects (GPOs)

This phase documents the implementation and validation of **department-specific Group Policy Objects (GPOs)** within the SwiftDesk Active Directory environment.

Group Policy is applied per department to reflect real enterprise practice, where different teams operate under different security and operational controls.

---

## Purpose of This Phase

The purpose of this phase is to:

- Apply desktop and security controls by department
- Enforce least-privilege access
- Standardise user environments
- Reduce manual configuration on client machines
- Validate policy application from both system and user perspectives

---

## Departments Implemented

The following departments are implemented in this phase:

- Human Resources (HR)
- Information Technology (IT)

Other departments (Finance, Sales, Management) are planned for future iterations.

---

## Group Policy Design Approach

Each department uses its **own dedicated GPO**, linked directly to the relevant Organisational Unit (OU).

This approach:
- Prevents policy overlap
- Simplifies troubleshooting
- Improves change control
- Aligns with enterprise Active Directory best practices

---

# HR Department Group Policy

## HR Policy Overview

- **GPO Name:** `HR_Policy`
- **Linked OUs:** HR, HR-WS
- **Design Model:** Restrictive-by-default

The HR policy prioritises data protection, consistency, and reduced system access.

---

## HR – Configuration Steps

### Step 1 – Create and Link HR GPO

The `HR_Policy` GPO was created in Group Policy Management and linked to the HR OU.

**Evidence:**  
![HR Policy Linked](../assets/screenshots/phase-7/HR/P7_HR_01_HR_Policy_Linked.PNG)

---

### Step 2 – Restrict User Environment

Control Panel and system configuration tools were restricted for HR users.

**Evidence:**  
![Control Panel Blocked](../assets/screenshots/phase-7/HR/P7_HR_03_ControlPanel_Blocked.PNG)

---

### Step 3 – Configure Folder Redirection

The Documents folder was redirected to a central server location to protect HR data.

**Evidence:**  
![Folder Redirection](../assets/screenshots/phase-7/HR/P7_HR_04_FolderRedirection_Documents.PNG)

---

### Step 4 – Configure HR Drive Mapping

An HR shared drive was mapped automatically at user logon.

**Evidence:**  
![Drive Mapping Policy](../assets/screenshots/phase-7/HR/P7_HR_05_DriveMap_H_Drive.PNG)

---

### Step 5 – Enforce Session Security

Automatic screen locking was configured to protect unattended workstations.

**Evidence:**  
![Screen Lock Policy](../assets/screenshots/phase-7/HR/P7_HR_06_ScreenLock_Policy.PNG)

---

### Step 6 – Block Removable Storage

USB and removable storage access was blocked.

**Evidence:**  
![USB Block Policy](../assets/screenshots/phase-7/HR/P7_HR_07_USB_Block_Policy.PNG)

---

### Step 7 – Apply and Verify HR Policy (System-Level)

Policy application was enforced and verified:

- `gpupdate /force`
- User logoff and logon
- `gpresult /r` confirmed policy scope

**Evidence:**  
![HR gpresult](../assets/screenshots/phase-7/HR/P7_HR_10_gpresult_HR_Policy.PNG)

---

### Step 8 – Validate HR Client-Side Behaviour

Logged in as an HR user and confirmed:

- HR drive mapped successfully
- Documents redirected to server
- Control Panel access blocked
- USB access denied
- Screen lock enforced

**Evidence:** 

### HR drive mapped successfully
![H Drive Mapped](../assets/screenshots/phase-7/HR/P7_HR_11_H_Drive_Mapped_Client.PNG) 

### USB access denied
![USB Access Denied](../assets/screenshots/phase-7/HR/P7_HR_12_USB_Access_Denied_Client.PNG)

---
---
---
---
---
---
---
---
---
---

# IT Department Group Policy

## IT Policy Overview

- **GPO Name:** `IT_AdminPolicy`
- **Linked OUs:** IT, IT-WS
- **Design Model:** Admin-enabled, controlled access

The IT policy enables support functionality while maintaining governance.

---

## IT – Configuration Steps

### Step 1 – Create and Link IT GPO

The IT policy was created and linked to the IT OU.

**Evidence:**  
![IT Policy Linked](../assets/screenshots/phase-7/IT/P7_IT_01_IT_AdminPolicy_Linked.PNG)

---

### Step 2 – Configure Administrative Settings

Administrative settings were configured within the IT policy.

**Evidence:**  
![IT Policy Editor](../assets/screenshots/phase-7/IT/P7_IT_02_IT_AdminPolicy_Editor.PNG)

---

### Step 3 – Assign Local Administrator Rights

Restricted Groups were used to assign IT users local administrator rights.

**Evidence:**  
![Restricted Groups](../assets/screenshots/phase-7/IT/P7_IT_03_RestrictedGroups_IT_Admins.PNG)

---

### Step 4 – Enable Remote Desktop

Remote Desktop access was enabled for IT support operations.

**Evidence:**  
![RDP Enabled](../assets/screenshots/phase-7/IT/P7_IT_04_RDP_Enabled_Policy.PNG)

---

### Step 5 – Provide Administrative Tools

Administrative tools and shortcuts were made available for IT support tasks.

**Evidence:**  
![Admin Tools Shortcuts](../assets/screenshots/phase-7/IT/P7_IT_05_AdminTools_Shortcuts.PNG)

---

### Step 6 – Configure IT Desktop Wallpaper

A wallpaper policy was applied to standardise the IT desktop environment and visually distinguish IT-managed systems.

**Evidence:**  
![Wallpaper Policy](../assets/screenshots/phase-7/IT/P7_IT_06_Wallpaper_Policy.PNG)

---

### Step 7 – Apply and Verify IT Policy (System-Level)

Policy application was enforced and verified:

- `gpupdate /force`
- User logoff and logon
- `gpresult /r` confirmed policy scope

**Evidence:**  
![IT gpresult](../assets/screenshots/phase-7/IT/P7_IT_07_gpresult_IT_Policy.PNG)

---

### Step 8 – Validate IT Client-Side Behaviour

Logged in as an IT user and confirmed:

- Local administrator privileges applied
- Administrative tools available
- Desktop wallpaper applied as expected
- Remote Desktop connection successful
- Policy persisted after reboot

**Evidence:**  

### Desktop wallpaper applied as expected and Administrative tools available
![Wallpaper Applied on Client](../assets/screenshots/phase-7/IT/P7_IT_08_Wallpaper_Applied_Client.PNG) 

### Remote Desktop connection successful
![RDP Connected](../assets/screenshots/phase-7/IT/P7_IT_10_RDP_Remote_Connection_Success.PNG)

---

---

## Screenshots Included

Evidence for this phase is organised by department:

- **Human Resources:**  
  [View HR GPO Screenshots](../assets/screenshots/phase-7/HR)

- **Information Technology:**  
  [View IT GPO Screenshots](../assets/screenshots/phase-7/IT)

---

## Notes and Lessons

Separating Group Policy by department:

- Improves security posture
- Simplifies administration
- Makes troubleshooting faster
- Reflects real enterprise Active Directory design

---

## Future Work

The following departments will be implemented in future iterations:

- Finance
- Sales
- Management

---


---

## Next Phase

Proceed to:

- [Phase 8 – Troubleshooting Scenarios](08-Phase-8-Troubleshooting.md)
