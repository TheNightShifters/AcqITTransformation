# User File Access from Any Domain Attached System SOP

## _Author: Jasmine Garcia_

## Purpose:
The purpose of this SOP is to ensure that employees are able to access their files from any computer that is attached to the domain. 

## Scope:
This SOP applies to all employees in the IT Department responsible for managing the domain controller. 

## Responsibilities 
The IT and Cybersecurity department is primarily responsible for implementing, following, reviewing, and updating this policy.

## Prerequisites:
Completion of the "Network Account Management Needs for Employees Being Onboarded SOP" for the employee when they were first onboarded to ensure they're in Active Directory Administrative Center.

## Procedure:
1. Ensure employee has been added to the Active Directory Administrative Center.
_If not, please refer to the step below and to the "Network Account Management Needs for Employees Being Onboarded SOP"._
- Add a new employee to Active Directory Administrative Center (ADAC).
- Launch the Active Directory Administrative Center (ADAC) by searching for "Active Directory Administrative Center" in the Start menu or using the "dsa.msc" command in the Run dialog box.
- Once ADAC is open, navigate to the desired Organizational Unit (OU) where you want to create the new user. You can browse the directory structure on the left-hand side of the ADAC window.
- Right-click on the OU and select "New" -> "User" from the context menu.
- The "New Object - User" wizard will open. Provide the necessary details for the new user, including First name, Last name, User logon name, and password. You can also configure other settings such as Group Membership, Profile, and more, as needed.
- Click "Next" and review the summary of the user account details.
- Click "Finish" to create the new user account. ADAC will create the user account in the specified OU.
- Optionally, you can further modify the user account properties by right-clicking on the user account and selecting "Properties."

3. Enable Roaming User Profiles:
- Implement roaming user profiles, which allow employees' user profiles, including settings, preferences, and files, to follow them when they login to different domain-attached systems. This ensures a consistent experience and access to files regardless of the system used.
- This can be completed in Group Policy. 
  - Open the Group Policy Management Console and navigate to the appropriate Group Policy Object (GPO) that applies to the user accounts. 
  - Configure the "Set roaming profile path for all users logging onto this computer" policy setting under "Computer Configuration > Policies > Administrative Templates > System > User Profiles".
  - Specify the roaming profile path to be used for all users.

4. Implement Folder Redirection:
- Utilize folder redirection to redirect certain user folders, such as Documents or Desktop, to the centralized file storage system. This ensures that employees' important files and folders are stored centrally and accessible from any domain-attached system.

5. Enable Remote Desktop Protocol:
- Configure and enable Remote Desktop Protocol (RDP) or a similar remote access solution. This allows employees to establish remote desktop connections to domain-attached systems, granting them access to their files and applications as if they were working directly on those systems.
  - Employees can launch the Remote Desktop Connection application on the computer being used to access files.
  - Enter the computer name or IP address of the office computer hosting the files to be accessed.
  - Enter the username and password provided by the IT department.
  - Click "Connect" to establish the remote desktop connection.
  - Accessing Files:
  - Once the remote desktop connection is established, employees will have access to their files as if they were working directly on the office computer.
  - Navigate to the appropriate file directory or network drive to access the required files
  - Save any changes or modifications made to the files back to the network drive or designated storage location.
  - Ending the Remote Desktop Session:
  - Once the work is completed, employees should log off from the remote desktop session to maintain security and prevent unauthorized access to their files.
  - Click the "Start" menu on the remote desktop session and select "Log Off" or "Sign Out."
  - Confirm the action and disconnect the remote desktop session.

6. Implement Virtual Private Network (VPN) Connectivity:
- Set up a VPN solution to enable secure remote access to the company's domain-attached systems. This allows employees to establish encrypted connections over the internet, ensuring the confidentiality of data while accessing their files remotely.

7. Regularly Test and Monitor:
- Regularly test the file access capabilities from different domain-attached systems to ensure the setup is working as intended. Monitor system logs and user feedback to identify any issues or areas for improvement and take appropriate actions to address them promptly.

8. Stay Up to Date with Security Measures:
- Keep up with the latest security measures and best practices to protect file access from domain-attached systems. Implement strong authentication mechanisms, regularly update system software and security patches, and employ encryption where necessary to safeguard employee files and data.

## References:
- [ChatGBT Reference](https://chat.openai.com/share/791089c3-a652-4394-bc48-e540a623f98d)
- [Seattle-Ops-301n3-Lab12](https://docs.google.com/document/d/1vWr4uQTUUjz89pKiqfEyYQPXogIRAe5eDwq3rYreQ1I/edit?usp=sharing)

## Revision History:
- 6/26/2023 -- "User File Access from Any Domain Attached System SOP" created by Jasmine Garcia 
