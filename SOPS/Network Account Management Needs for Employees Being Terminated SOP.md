# Network Account Management Needs for Employees Being Terminated SOP

## _Author: Jasmine Garcia_

## Purpose:
The purpose of this SOP is to establish a set of guidelines for the IT employees involved in managing network accounts for employees being terminated. This SOP is to ensure the security and integrity of the company's network and sensitive information.

## Scope:
This SOP applies to all employees in the IT department responsible for managing network accounts associated with the termination process.

## Responsibilities 
The IT and Cybersecurity department is primarily responsible for implementing, following, reviewing, and updating this policy.

## Prerequisites:
The terminating department of the employee will notify HR Department to initiate the termination process. HR will then need to notify the IT and Cybersecurity Department of the employee's information: name, position, department, and end date.

## Procedure:
**1. Account Review and Planning:**
- The IT and Cybersecurity department will conduct a review of the employee's network accounts, systems, and access privileges. Identify all accounts and access privileges associated with the terminated employee. Consult with the employee's supervisor or manager to validate the list of accounts and access privileges.

**2. Ensure Group Policy Had Been Enforced**
  
- **_This should have already been applied when the employee had first been onboarded. This can be referenced in Network Account Management Needs for Employees Being Onboarded SOP. But this step is to ensure that this has been done._**
- Specific policies will include: Account Lockout Policy, Password Policy, Access Control Policy, User Account Deactivation Policy, Data Loss Prevention (DLP) Policy, Remote Access Policy, Email Retention, and Monitoring Policy, Establish policies for email retention and monitoring, Device Security Policy, Enable Audit Logs, Screen Lockout Time, Password Policy, Password Policy, Access restriction to the command prompt and PowerShell, Limit access to Control Panel options, Limit who can install software, Guest Account Settings, Prevent Storing LAN Manager Hash, Limit Local Account use of a blank password to console only, Turn off forced restarts, Monitor Changes to GPO Settings, Disable Anonymous SID/Name Translation, Windows Firewall, and Enable User Account Control (UAC).

**3. Termination of Accounts:**
- On the employee's last working day, the IT and Cybersecurity department will initiate the termination of all accounts. For example, CRM tools like Salesforce, Google Drive, Asana, Canvas, etc. Terminate email accounts and remove all forwarding rules or auto-replies. Disabling or Deactivating the employee's Active Directory account. This approach ensures that the employee no longer has access to company systems and resources during their remaining time at the organization.

**4. Disable or remove an employee from Active Directory (AD):**
- Disabling or Deactivating the Employee Account:
  - Before Termination: In some organizations, it is common practice to disable or deactivate an employee's AD account shortly before their termination date. This approach ensures that the employee no longer has access to company systems and resources during their remaining time at the organization.
  - After Termination: Following the termination, the disabled AD account can be kept for a specific period for administrative purposes, such as auditing or historical reference. Eventually, the account can be permanently removed from AD.
- Immediate Account Removal:
  - Before Termination: In situations where there are immediate security concerns or a high risk associated with the employee's termination, some organizations may choose to remove the employee's AD account before the termination date. This ensures that access is revoked immediately to mitigate potential risks.
  - After Termination: After the termination, the account can be permanently removed from AD, ensuring that the terminated employee no longer has any residual access to company systems.

**5. Asset Retrieval:**
- Coordinate with the HR Department and Facilities team to retrieve all company-owned devices, such as laptops, mobile phones, access cards, and security tokens, from the terminated employee.
- Ensure all assets are accounted for and documented.

**6. Data Backup and Archival:**
- Prior to account termination, the IT and Cybersecurity department will ensure the backup and archival of any relevant data or files associated with the employee, as per company policies.

**7. Access Logs and Audit Trail:**
- Retain access logs and audit trail information related to the employee's activities for future reference and investigations, as per legal and company requirements.

**8. Documentation:**
- Maintain accurate records of all terminated employees and the corresponding account termination procedures performed.
Document any issues, challenges, or exceptions encountered during the termination process for future improvement.
Exceptions:
- In exceptional cases where immediate account termination is required, such as for security breaches or policy violations, the IT and Cybersecurity department may expedite the account termination process after obtaining the necessary approvals.
Revision History:
- Record any updates, revisions, or amendments made to this SOP with dates and reasons for the changes.

## References:
- [ChatGBT Reference](https://chat.openai.com/share/def254fd-f648-4254-ba55-3ee48ee0bfa7)

## Definitions:
- **UAC:** User Account Control is a security feature in Windows operating systems that helps prevent unauthorized changes to the system by requiring elevated permissions or confirmation from users when certain actions are performed. UAC is designed to protect against malware, unauthorized software installations, and system configuration changes that can impact the overall security and stability of the system.
- **DLP:** Data Loss Prevention, which refers to a set of strategies, policies, and technologies designed to prevent the unauthorized disclosure, leakage, or loss of sensitive data. DLP aims to protect sensitive information from being accessed, copied, transmitted, or stored in an insecure manner, whether accidentally or intentionally.

## Revision History:
- 06/26/2023 -- "Network Account Management Needs for Employees Being Terminated SOP" created by Jasmine Garcia 
