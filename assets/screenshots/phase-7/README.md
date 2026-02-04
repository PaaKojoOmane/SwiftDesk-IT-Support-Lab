# Phase 7 – Group Policy Objects (GPOs) & Desktop Management

This phase focuses on the use of **Group Policy Objects (GPOs)** to centrally manage user environments, security controls, and administrative behaviour across the Active Directory domain.

Group Policy is a core component of enterprise Windows environments and is heavily relied upon in IT Support and junior systems administration roles to enforce standards, reduce manual configuration, and improve security.

---

## Purpose of This Phase

The purpose of Phase 7 is to:

- Implement **department-specific Group Policy Objects**
- Enforce consistent desktop and security settings
- Separate standard user environments from administrative environments
- Validate policy application on domain-joined clients
- Demonstrate real-world Group Policy design and structure

Rather than applying a single global policy, this phase follows **departmental separation**, which reflects best practice in enterprise environments.

---

## Scope of Implementation

In this phase, Group Policy has been implemented for the following departments:

- **Human Resources (HR)**
- **Information Technology (IT)**

Each department has:
- Its own dedicated Group Policy Object
- Policies linked at the correct OU level
- Separate documentation and validation evidence

This approach ensures clarity, scalability, and minimal risk of unintended policy impact.

---

## Design Approach

The following principles guided the Group Policy design:

- **Least privilege:** Users receive only the access required for their role
- **OU-based targeting:** Policies are linked to departmental OUs
- **Separation of concerns:** Administrative policies are isolated from user policies
- **Validation-first:** Every policy is tested on a client machine

This structure mirrors how Group Policy is typically implemented in production environments.

---

## Validation Summary

Across the implemented departments, the following were confirmed:

- GPOs are correctly linked to the intended OUs
- Policies apply only to targeted users and machines
- Settings persist after logoff and reboot
- `gpresult` confirms correct policy application
- Client-side behaviour matches policy intent

---

## Documentation Structure

To keep documentation clear and maintainable, each department is documented separately:

- **HR Group Policy Documentation**  
  [HR/PHASE_07_HR_GPO_DOCUMENTATION.md](HR/PHASE_07_HR_GPO_DOCUMENTATION.md)

- **IT Group Policy Documentation**  
  [IT/PHASE_07_IT_GPO_DOCUMENTATION.md](IT/PHASE_07_IT_GPO_DOCUMENTATION.md)


Each document contains:
- Policy objectives
- Implemented settings
- Validation steps
- Evidence references
- Notes and lessons learned

---

## Future Work

The following departments are planned for future implementation:

- Finance
- Sales
- Management

Future enhancements may include:

- Department-specific security baselines
- Software deployment via Group Policy
- BitLocker and Microsoft Defender policies
- Advanced auditing and compliance controls

These additions will build on the structure established in this phase without requiring redesign.

---

## Notes and Lessons

Implementing Group Policy on a per-department basis:

- Reduces configuration risk
- Simplifies troubleshooting
- Makes change management safer
- Scales cleanly as organisations grow

This phase reinforces the importance of **planning and structure** when managing Windows environments.

---

## Next Steps

Proceed to:

- **HR Department Group Policy Documentation**  
  [HR/PHASE_07_HR_GPO_DOCUMENTATION.md](HR/PHASE_07_HR_GPO_DOCUMENTATION.md)

- **IT Department Group Policy Documentation**  
  [IT/PHASE_07_IT_GPO_DOCUMENTATION.md](IT/PHASE_07_IT_GPO_DOCUMENTATION.md)

