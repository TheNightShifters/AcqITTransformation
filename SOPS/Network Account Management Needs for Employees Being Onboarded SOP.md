# Network Account Management Needs for Employees Being Onboarded SOP

## Purpose:
The purpose of this SOP is to establish a set of guidelines for employees being onboarded in terms of network account management. This applies to both new employees and already existing employees who will either be transferred to a different department or employees who have advanced or are relegated to a new position. For already existing employees this would be to prevent privilege creep. 

## Scope:
This SOP applies to the security of the companys network and security of the user.

## Responsibilities 
The IT and cybersecurity department is primarily responsible for implementing, following, reviewing, and updating this policy.

## Prerequisites:
The HR Department processes new employees into the company and will need to notify the IT Department of a new incoming employee or existing employee's information: name, position, department, and start date. 

## Procedure:
### **1. New User Creation in ADAC**
- Add a new employee to Active Directory Administrative Center (ADAC). 
- Launch the Active Directory Administrative Center (ADAC) by searching for "Active Directory Administrative Center" in the Start menu or using the "dsa.msc" command in the Run dialog box.
- Once ADAC is open, navigate to the desired Organizational Unit (OU) where you want to create the new user. You can browse the directory structure on the left-hand side of the ADAC window.
- Right-click on the OU and select "New" -> "User" from the context menu.
- The "New Object - User" wizard will open. Provide the necessary details for the new user, including First name, Last name, User logon name, and Password. You can also configure other settings such as Group Membership, Profile, and more, as needed.
- Click "Next" and review the summary of the user account details.
- Click "Finish" to create the new user account. ADAC will create the user account in the specified OU.
- Optionally, you can further modify the user account properties by right-clicking on the user account and selecting "Properties."

### **1.2 Modify Existing User in ADAC**
- Locate the user account you want to modify, and then right-click on it. A context menu will appear.
- From the context menu, select "Properties." A dialog box will open, displaying the properties of the selected user account.
- In the user account properties dialog box, you can make changes to various attributes such as General, Account, Profile, Organization, Telephones, - --- Address, and more, depending on the available attributes and your permissions.
- Navigate through the tabs and modify the desired properties according to your requirements. For example, you can change the user's name, password settings, group membership, email address, etc.
-Once you have made the necessary modifications, click the "OK" button to save the changes.

### **2. Apply Group Policy to New Employees**
- _Specific policies will include: Enable Audit Logs, Screen Lockout Time, Password Policy, Password Policy, Access restriction to the command prompt and PowerShell, Limit access to Control Panel options, Limit who can install software, Guest Account Settings, Prevent Storing LAN Manager Hash, Limit Local Account use of a blank password to console only, Turn off forced restarts, Monitor Changes to GPO Settings, Disable Anonymous SID/Name Translation, Windows Firewall, and Enable User Account Control (UAC)._
- On the domain controller or a computer with the Remote Server Administration Tools (RSAT) installed, open the Group Policy Management Console (GPMC)or you can access GPMC by clicking "Start," typing "Group Policy Management" in the search box, and selecting the appropriate result.
- Locate the Existing Group Policy. 
- Expand the forest and domain in the GPMC to find the existing Group Policy that you want to modify.
- Expand the domain, then navigate to "Group Policy Objects."
- Double-click on the desired Group Policy Object to open its properties and edit it.
- Edit the Group Policy 
- Within the Group Policy Management Editor, navigate to the policy setting that controls the membership of the group to which you want to add the user.
- The policy settings are located in either the "Computer Configuration" or "User Configuration" sections, depending on the target of the policy.
- Modify the Group Membership Policy by clicking on the policy setting.
- In the policy setting window, look for the option to specify the group membership, such as "Add users to a group" or "Restricted Groups." Then "Add" or Edit" to modify the group members. Be sure to click apply to finalize the changes. 
- The changes will be saved automatically within the GPO.
- Verify and test by logging in with the new user account and confirming that it has been added to the specified group.

### **3. Network Access and Connectivity**
- Provide the new employee with a network connection, either wired or wireless, to ensure they have internet access and connectivity within the organization's network.
- Configure the employee's device to connect to the organization's Wi-Fi network or assign an Ethernet port if applicable.
- Ensure that the network connection is secure and compliant with the organization's network policies and protocols, such as VPN access for remote employees or guest network access for visitors.

### **4. Device Setup and Configuration**
- Set up the employee's computer or device with the necessary operating system, software applications, and security tools.
- Install and configure Malwarebytes software, firewalls, and any other required security measures to protect the device and the network from potential threats.
- Configure network printers or other peripheral devices the employee may require.

### **Software and Application Provisioning**
- Install and configure standard software applications required for the employee's job role, such as productivity tools, communication software, and business applications.
- Provide licenses or activation keys for the software, ensuring compliance with software licensing agreements.
- Set up access to cloud-based applications and services that the employee needs, such as customer relationship management (CRM) tools or project management platforms.

### **Data and File Access**
- Grant appropriate permissions and access to network file shares or cloud storage platforms, enabling the employee to access and collaborate on shared files and documents.
- Educate the employee about data security and best practices for handling sensitive information, such as encryption, file backup procedures, and data access controls.

### **Implementation of MFA and User to Password Manager**
- Implement 2FA or MFA to add an extra layer of security to user account authentication.
- Require employees to provide additional verification factors, such as a temporary code sent to an an Authenticator app such as Google Authenticator, in addition to their username and password. Their passwords will also be stored in a password manager such as NordPass.

### **User Training and Support**
- Provide orientation or training sessions to familiarize the new employee with the organization's network policies, security practices, and acceptable use guidelines.
- Offer ongoing technical support and assistance for any network-related issues or questions that arise during the onboarding process.
- Ensure the employee has access to IT support channels for reporting problems or requesting assistance.

## References:
- [SOP-Template](https://github.com/codefellows/seattle-ops-301n3/blob/main/class-15/SOP-example-template.md)
- [Seattle-Ops-301n3-Lab13](https://docs.google.com/document/d/1aEOmYs2EfXnuoA6TWb1nLJsfyjU2Cw3Z4JoXHZEqnE4/edit?usp=sharing)
- [Seattle-Ops-301-Lab14](https://docs.google.com/document/d/1Ws487TTXStKm4_-Hl5ndzFghjlRYh7yxva76JX8mW0o/edit?usp=sharing)
- [ChatGBT-Reference](https://chat.openai.com/share/42f31a28-79db-4767-aa69-b5f8dc8a86e4)
- [Group-Policy-Examples](https://activedirectorypro.com/group-policy-examples-most-useful-gpos-for-security/)

## Definitions:
- **Privilege creep**: Refers to the gradual accumulation of excessive privileges or access rights granted to a user over time, often due to changes in job roles or responsibilities, leading to potential security risks and unauthorized access.
- **ADAC**: The Active Directory Administrative Center (ADAC) in Windows Server includes enhanced management experience features. These features ease the administrative burden for managing Active Directory Domain Services (AD DS).
- **MFA or 2FA**: Multi-Factor Authentication (MFA), also known as Two-Factor Authentication (2FA), is an important security measure that adds an extra layer of protection to user accounts. It requires users to provide multiple factors of authentication to verify their identity. 

Revision History:
6/25/2023 -- "Network Account Management Needs for Employees Being Onboarded SOP.md" created by Jasmine Garcia
