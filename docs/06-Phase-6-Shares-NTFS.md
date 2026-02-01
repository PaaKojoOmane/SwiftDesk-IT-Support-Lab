# Phase 6 – File Shares & NTFS Permissions

This phase focuses on implementing secure departmental file sharing using **NTFS permissions** and **Active Directory security groups**.

The goal is to ensure that:
- Users can access only their department’s data
- Access is centrally managed through AD groups
- Least-privilege principles are enforced

This mirrors real enterprise file server configurations.

---

## Purpose of This Phase

The purpose of this phase is to:

- Create a central company file share
- Organise folders by department
- Apply NTFS permissions using security groups
- Configure share permissions
- Validate authorised and unauthorised access

---

## Environment Overview

- **Server:** SD-DC01  
- **Role:** Domain Controller & File Server  
- **Client:** SD-CLIENT01  
- **Domain:** swiftdesk.local  
- **Share Root:** `C:\CompanyShares`

---

## Step 1 – Create Company File Share Structure

A central directory was created on the domain controller to store all departmental data.

**Folder structure created:**
- Finance  
- HR  
- IT  
- Management  
- Sales  

This structure reflects a typical small-to-medium enterprise environment.

**Evidence:**

![Company Share Folder Structure](../assets/screenshots/phase-6/P6-01_Company_Share_Folder_Structure.PNG)

---

## Step 2 – Configure NTFS Permissions (HR Folder)

NTFS permissions were applied to the **HR** folder using the HR security group.

**Permissions applied:**
- Group: `HR_Group`
- Access: Modify, Read & Execute, List Folder Contents, Read, Write
- Inheritance: Enabled
- Administrators retained Full Control

This ensures only HR staff can access HR data.

**Evidence:**

![HR NTFS Permissions](../assets/screenshots/phase-6/P6-02_HR_NTFS_Permissions.PNG)

---

## Step 3 – Configure Share Permissions (HR Folder)

Share permissions were configured to align with NTFS access control.

**Share configuration:**
- Share name: `HR`
- Group: `HR_Group`
- Permission level: Change, Read
- Administrators: Full Control

NTFS permissions remain the primary enforcement layer.

**Evidence:**

![HR Share Permissions](../assets/screenshots/phase-6/P6-03_HR_Share_Permissions.PNG)

---

## Step 4 – Validate Authorised User Access

Access was tested from a domain-joined client.

**Test performed:**
- Logged into `SD-CLIENT01` as HR user (`alice.hughes`)
- Accessed share path:  
  `\\SD-DC01\HR`
- Created and modified files successfully

This confirms correct permissions for authorised users.

**Evidence:**

![Authorised HR Access Test](../assets/screenshots/phase-6/P6-04_HR_Client_Access_Test.PNG)

---

## Step 5 – Validate Access Denial for Unauthorised Users

Access restrictions were verified to ensure users cannot access other departments.

**Test performed:**
- Logged into `SD-CLIENT01` as a non-HR user
- Attempted to access:  
  `\\SD-DC01\Finance`
- Access was denied as expected

This confirms least-privilege enforcement.

**Evidence:**

![Access Denied for Non-HR User](../assets/screenshots/phase-6/P6-05_Access_Denied_Non_HR.PNG)

---

## Validation Summary

The following were successfully confirmed:

- Department users can access only their own folders  
- Unauthorised users are blocked  
- NTFS permissions enforce access control  
- Share permissions function as expected  
- File access mirrors real enterprise environments  

---

## Notes and Lessons

Managing file access through **Active Directory security groups** simplifies administration and improves scalability.

Combining **NTFS permissions** with **share permissions** provides predictable, secure access control across the domain.

---

## Screenshots Included

Only key evidence screenshots are included for this phase:

- Company share folder structure  
- NTFS permissions configuration  
- Share permissions configuration  
- Authorised user access verification  
- Unauthorised access denial  

Screenshots are stored under: [assets/screenshots/phase-6](../assets/screenshots/phase-6/)

---

## Next Phase

Proceed to:

- [**Phase 7 – Group Policy Objects (GPOs) & Desktop Management**](07-Phase-7-GPOs-Desktop-Management.md)
