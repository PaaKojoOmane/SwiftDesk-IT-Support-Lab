# Phase 5 – Organizational Units, Users & Security Groups

This phase focuses on structuring the Active Directory environment to reflect a real-world organisational hierarchy.

Proper use of Organizational Units (OUs), users, and security groups is essential for scalable administration, delegation, and Group Policy application.

This phase prepares the domain for realistic access control and policy management in later stages.

---

## Purpose of This Phase

The purpose of this phase is to:

- Design and implement a logical OU structure  
- Create department-based security groups  
- Create user accounts aligned with business roles  
- Assign users to the correct security groups  

---

## Organizational Design Overview

- **Domain:** swiftdesk.local  
- **Top-level OU:** SwiftDesk Ltd  

**Departments created:**
- HR  
- IT  
- Finance  
- Sales  
- Management  

Each department contains user accounts and a department-specific security group.

---

## Step 1 – Create Organizational Unit (OU) Structure

A top-level OU named **SwiftDesk Ltd** was created to separate business objects from default Active Directory containers.

Sub-OUs were created for each department to support clean administration and future Group Policy targeting.

**OUs created:**
- HR  
- IT  
- Finance  
- Sales  
- Management  

**Evidence:**

![OU Structure](../assets/screenshots/phase-5/P5-01_OU_Structure.PNG)

---

## Step 2 – Create Department Security Groups

A dedicated security group was created for each department.

**Security groups created:**
- HR_Group  
- IT_Group  
- Finance_Group  
- Sales_Group  
- Management_Group  

Each group was created within its corresponding departmental OU.

**Evidence:**

![Department Security Group](../assets/screenshots/phase-5/P5-02_Department_Security_Group.PNG)

---

## Step 3 – Create Department User Accounts

User accounts were created to represent staff members within each department.

**Example users created (HR):**
- Alice Hughes – HR Assistant  
- Jack Benson – HR Manager  
- Luke Adams – Recruitment Officer  
- Olivia Young – Payroll Officer  
- Sophie Green – HR Coordinator  

Users were placed into their respective departmental OUs.

**Evidence:**

![Department Users](../assets/screenshots/phase-5/P5-03_Department_Users.PNG)

---

## Step 4 – Assign Users to Security Groups

Each user was added to their relevant department security group to implement role-based access control.

**Example:**
- Alice Hughes → HR_Group  

**Evidence:**

![User Group Membership](../assets/screenshots/phase-5/P5-04_User_Group_Membership.PNG)

---

## Validation Performed

- OU structure reflected the intended business layout  
- Security groups existed in the correct OUs  
- Users were created in the correct departments  
- Group memberships were correctly assigned  

---

## Notes and Lessons

Department-based security groups simplify permissions management and support scalable Active Directory administration.

---

## Screenshots Included

Only key evidence screenshots are included for this phase:

- Organisational Unit (OU) structure  
- Department security groups  
- Department user accounts  
- User group membership assignments  

Screenshots are stored under: [assets/screenshots/phase-5](../assets/screenshots/phase-5/)

---

## Next Phase

Proceed to:

- [Phase 6 – Group Policy Objects (GPOs) & Access Control](06-Phase-6-GPOs-Access-Control.md)

