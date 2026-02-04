# Phase 7 – HR Department Group Policy Documentation

This document details the design, implementation, and validation of **Group Policy Objects (GPOs)** applied to the **Human Resources (HR)** department within the SwiftDesk Active Directory environment.

Because HR users handle sensitive employee and organisational data, the HR desktop environment was designed to be **restricted, consistent, and security-focused**, while still supporting daily business operations.

---

## Purpose of the HR Group Policy

The HR Group Policy was implemented to:

- Restrict access to system configuration tools  
- Protect sensitive HR data from unauthorised access  
- Enforce consistent desktop behaviour  
- Prevent data leakage via removable media  
- Apply all controls centrally without manual configuration  

---

## HR Policy Overview

- **GPO Name:** `HR_Policy`
- **Linked Organisational Units:**
  - HR (Users)
  - HR-WS (Workstations)
- **Scope:** HR users and HR workstations only

The policy is linked at the OU level to ensure **departmental isolation** and avoid unintended impact on other departments.

---

## Step 1 – Create and Link HR Group Policy

A new Group Policy Object named `HR_Policy` was created using the Group Policy Management Console (GPMC) and linked to the **HR OU**.

This ensures that the policy applies only to HR users and does not affect other users in the domain.

**Evidence:**

![HR Policy Linked to HR OU](../../assets/screenshots/phase-7/HR/P7_HR_01_HR_Policy_Linked.PNG)

---

## Step 2 – Configure User Environment Restrictions

Restrictions were configured to prevent HR users from accessing the Control Panel and system configuration tools.

This reduces the risk of accidental or unauthorised system changes.

**Evidence:**

![HR Control Panel Restriction](../../assets/screenshots/phase-7/HR/P7_HR_03_ControlPanel_Blocked.PNG)

---

## Step 3 – Configure Folder Redirection

Folder Redirection was enabled for the **Documents** folder to ensure HR data is stored centrally on the server rather than locally on workstations.

This supports backup, recovery, and access control.

**Evidence:**

![HR Folder Redirection Configuration](../../assets/screenshots/phase-7/HR/P7_HR_04_FolderRedirection_Documents.PNG)

---

## Step 4 – Configure HR Drive Mapping

A drive mapping policy was configured to automatically map the HR shared drive at user logon.

This provides consistent and reliable access to departmental resources.

**Evidence:**

![HR Drive Mapping Configuration](../../assets/screenshots/phase-7/HR/P7_HR_05_DriveMap_H_Drive.PNG)  
![HR Drive Mapped on Client](../../assets/screenshots/phase-7/HR/P7_HR_11_H_Drive_Mapped_Client.PNG)

---

## Step 5 – Enforce Session Security

A screen lock policy was applied to automatically lock HR workstations after a defined period of inactivity.

This reduces the risk of unauthorised access if a workstation is left unattended.

**Evidence:**

![HR Screen Lock Policy](../../assets/screenshots/phase-7/HR/P7_HR_06_ScreenLock_Policy.PNG)

---

## Step 6 – Block Removable Storage (USB)

USB and removable storage access was blocked to prevent unauthorised copying of sensitive HR data.

**Evidence:**

![HR USB Block Policy](../../assets/screenshots/phase-7/HR/P7_HR_07_USB_Block_Policy.PNG)  
![USB Access Denied on Client](../../assets/screenshots/phase-7/HR/P7_HR_12_USB_Access_Denied_Client.PNG)

---

## Step 7 – Enable Logon Auditing

Logon auditing was enabled to provide visibility into HR authentication activity.

This supports monitoring and compliance requirements.

**Evidence:**

![HR Logon Auditing Enabled](../../assets/screenshots/phase-7/HR/P7_HR_08_AuditLogon_SuccessFailure.PNG)

---

## Step 8 – Validate Policy Application (System-Level)

Initial validation was performed to confirm that the HR policy applied successfully.

**Validation checks performed:**
- `gpresult` confirms `HR_Policy` is applied  
- Policy scope reflects correct OU targeting  

**Evidence:**

![HR Policy Applied – gpresult](../../assets/screenshots/phase-7/HR/P7_HR_10_gpresult_HR_Policy.PNG)

---

## Step 9 – Confirm Policy Validation (Client-Side Behaviour)

Additional checks were performed from the **end-user perspective** to ensure the policy was not only applied, but **functioning as intended**.

### Validation Actions Performed

- Logged in as an HR domain user  
- Verified HR drive mapped automatically at logon  
- Confirmed Documents folder redirected to network location  
- Attempted to access restricted system settings (blocked)  
- Inserted USB storage device (access denied)  
- Confirmed workstation locked automatically after inactivity  

### Evidence

![HR Drive Available at Logon](../../assets/screenshots/phase-7/HR/P7_HR_11_H_Drive_Mapped_Client.PNG)  
![USB Access Denied for HR User](../../assets/screenshots/phase-7/HR/P7_HR_12_USB_Access_Denied_Client.PNG)

---

## Validation Outcome

All HR Group Policy settings were confirmed to be:

- Successfully applied  
- Enforced consistently  
- Persistent across logoff and reboot  

This confirms that the HR Group Policy is **production-ready** within the scope of this lab environment.

---

## Screenshots Included

Only key evidence screenshots are included for this department:

- HR policy linked to HR OU  
- Control Panel restriction  
- Folder Redirection configuration  
- Drive mapping configuration and result  
- USB block and denial  
- `gpresult` confirmation  

Screenshots are stored under:  
[assets/screenshots/phase-7/HR](../../assets/screenshots/phase-7/HR/)

---

## Notes and Lessons

Separating HR policies from other departments:

- Reduces configuration risk  
- Simplifies troubleshooting  
- Aligns with enterprise Active Directory best practices  
- Makes future changes safer and easier to manage  

HR environments benefit from policies that prioritise **security and consistency** over flexibility.

---

## Future Enhancements

Planned future improvements for the HR department include:

- Enhanced audit and compliance policies  
- Data classification and retention controls  
- Alignment with organisation-wide security baselines  

---

## Next Department

Proceed to:

- **IT Department Group Policy Documentation**  
  [IT/PHASE_07_IT_GPO_DOCUMENTATION.md](../IT/PHASE_07_IT_GPO_DOCUMENTATION.md)
