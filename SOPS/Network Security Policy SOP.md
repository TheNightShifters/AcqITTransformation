# Network Security Policy SOP

## Purpose:
The purpose of this SOP is to describe the correct procedure for accessing on-premises and cloud
resources securely for remote employees. It will be updated periodically to reflect
changes to the network topology. If you notice inconsistencies, feel free to consult the IT
department to have them fixed.

## Procedure:
### 1. **Accessing Local Resources From Remote Location:**
### **Step 1: Set up your Home client:**
- Your IT department has provided you with a file containing
instructions for proper VPN client configuration for your pfSense
subnet. Follow these instructions carefully and completely.
- Navigate to the pfSense web portal on any device connected to
your work subnet.
- Navigate to VPN > IPsec > Tunnels.
- Select “+ Add p1”.
- From here you can begin following the instructions in the
file. They will differ for each user, so ensure all information
is correct before proceeding.
### **Step 2: Establish VPN connection**
- In the pfSense web portal, navigate to status > IPsec.
- Select “connect p1 and p2s”.

_**Congratulations, you’ve successfully joined the domain. Welcome to the HarmoniTech Family!**_

## **2. Joining the domain:**
### **Step 1: Configuring DNS**
- In the bottom right-hand corner of your screen, click the internet
connection icon.
- Select Change adapter settings.
- Right-click on your network adapter, and select “properties”.
- Select “Internet Protocol Version 4(IPv4)”, and select “properties”.
- Enter the IP of the Windows Server in the first box, and leave the
second blank.
- Select close on both windows.
### **Step 2: Configuring Domain**
- In the file explorer, navigate to “This PC”. Right-click on any empty
space and select “properties”.
- Scroll down and select “Rename This PC (advanced)”.
- Use your name or username in the user name category.
- Use VERVE.HarmoniTech.com in the domain name category.
- You will be prompted to reboot the PC.

_**Congratulations, you’ve successfully joined the domain. Welcome to the HarmoniTech Family!**_

## **3. Network Security Rules** 
_**CORPORATE MANDATED**_
_**It is Vital that you follow the following terms at all times in order**_
_**to ensure your continued employment at HarmoniTech!**_
_**Breaking these terms and condition can result in termination**_
_**fines, jail time, legal recourse, blackmailing, gangstalking**_
_**supernatural plagues of vermin affecting you and your**_
_**family members, recession, depression, congestion,**_
_**loss of motor control, rashes, dizziness, and no longer**_
_**being our friend!**_

1. You will not disclose your AD credentials to anyone. A member of IT staff will never
request your credentials. You are never required to give your credentials out to anyone
to fix any problem with your computer.
2. You will not use your corporate network access for illegal activities, including but not
limited to hacking, piracy, or distribution of copyrighted material without proper
authorization.
3. You will not attempt to bypass or disable any security measures put in place by the IT
department, including firewalls, antivirus software, or content filters.
4. You will not install unauthorized software or hardware on your work devices. All software
installations must be approved and performed by the IT department.
5. You will not use your work devices or network access for personal gain, such as running
a personal business or mining cryptocurrency.
6. You will regularly update your passwords in accordance with the company's password
policy. This includes using strong, unique passwords and not reusing passwords across
multiple services.
7. You will report any suspected security incidents or breaches to the IT department
immediately. This includes phishing attempts, suspicious emails, or unexpected system
behavior.
8. You will not access, copy, or transmit sensitive company data unless it is necessary for
your job role and you have received proper authorization.
9. You will not connect unauthorized devices to the corporate network. This includes
personal devices, such as smartphones or tablets, unless they have been approved and
properly secured by the IT department.
10. You will not share sensitive company information on social media or other public
platforms.
11. You will not leave your devices unattended while logged into the corporate network.
Always lock your screen or log out when stepping away from your device.
12. You will ensure that your home network is secure when accessing corporate resources
remotely. This includes using a secure Wi-Fi password and keeping your router firmware
up to date.
13. You will not attempt to modify or tamper with the VPN client configuration provided by
the IT department.
14. You will not attempt to connect to the corporate network from an unsecured public Wi-Fi
network, such as those found in cafes or airports, without using the provided VPN.
15. You will not share the VPN configuration files or instructions with anyone outside of the
organization.
16. You will not attempt to access or modify the settings of the pfSense web portal beyond
what is necessary for establishing a VPN connection.
17. You will not attempt to join unauthorized devices to the domain. Only devices provided or
approved by the IT department should be joined to the domain.
18. You will not attempt to modify the DNS settings on your device beyond what is
necessary for joining the domain.
19. You will not share the IP address of the Windows server instance with anyone outside of
the organization.
20. You will not attempt to access resources or data on the domain that you do not have
authorization to access.
21. You will not use your domain access to disrupt the operation of the network or other
users, such as by launching denial of service attacks or spreading malware.
22. You will not write down your passwords or store them in an unsecured manner. If you
need to keep a record of your passwords, use a secure password manager approved by
the IT department.
23. You will enable multi-factor authentication (MFA) on your accounts whenever possible.
This includes your corporate email and VPN access.
24. You will not share your multi-factor authentication codes with anyone, including IT staff.
25. You will immediately report any suspected compromise of your credentials to the IT
department. This includes if you believe your password has been stolen or your account
has been accessed without your permission.
26. You will not attempt to guess or use someone else's credentials to access their accounts
or impersonate them.
27. Youwill regularly update your system and all software to ensure you have the latest
security patches and updates.
28. You will not click on links or download attachments from unknown or unverified sources
to avoid potential phishing or malware attacks.
29. You will use secure and encrypted communication methods for sharing sensitive
information. Plain text emails or messages should not be used for sharing sensitive data.
30. You will participate in any security awareness training provided by the company to stay
updated on the latest threats and best practices.
31. You will regularly backup important data in accordance with the company's data backup
policy. This helps to prevent data loss in case of a system failure or cyber attack.
32. You must change your desktop background to the company logo every Monday morning.
33. You must log out and log back into the domain every two hours.
34. You must manually disconnect and reconnect your VPN connection every hour.
35. You must submit a daily report to the IT department detailing every single action you
took on the corporate network.
36. You must change your mouse cursor to a different style every day.
37. You must use a different web browser each day of the week when accessing the
pfSense web portal.
38. You must perform a full system scan with the antivirus software every morning,
regardless of whether the software is already set to do this automatically.
39. You must rename your PC every week, using a different fruit name each time.
40. You must send a formal email to the IT department requesting permission each time you
want to print a document.
41. You must recite the company's mission statement out loud before logging into the
domain each morning.
 
## References: 
- [Samuel Allen's Orginal Network Security Policy SOP](https://github.com/TheNightShifters/AcqITTransformation/files/11828307/NSP.pdf)
- [List Generated by ChatGBT](https://chat.openai.com/share/3391b5d6-f23f-442d-8309-1f853a83ad74)

## Revision History:
- 06/20/2023 -- "Network Security Policy SOP.md" created by Samuel Allen" 
- 06/25/2023 -- Edits, and restructure to markdown from PDF format for consistency by Jasmine Garcia 
