# HarmoniTech: Transforming Acquisitions with Seamless IT Integration Project Guidelines

## Scenario

You team is tasked with updating the core IT infrastructure of a recent client company acquisition. This young, innovative startup aligns well with the mission of the client company; unfortunately, its IT systems do not.

Your team believes that trying to integrate the acquisition's existing intranet directly into the rest of the client company will result in technical debt. Since the acquisition is still a small startup, your team believes it will be better to simply build out a new infrastructure which is in line with the rest of the client company's holdings. 

However, you still need to convince your leadership by demonstrating that your team is up to the challenge and can perform this kind of task in a repeatable, efficient manner.

Your team's task is to create a plan to make this acquistion successful and meet your client company's needs, then present your solutions to the client company on presentation day.

The operations chosen for this demonstration are:
- Develop a repeatable means of standing up a DC to oversee the new acquisition's network. The AD will need to automatically populate users and OUs in accordance with the organizational chart.
  - Objective: as a team, develop a Powershell script to be executed on a new installation of Windows Server.
    - This should be written as a single script, though it can be organized into different files.
    - The VM will need to reboot at least once while the script is performing its tasks.
      - Ways that students got their script to continue after reboot:
        - programmed the next bit of the script to the Windows startup folder (this is probably the cleverest)
    - How will you make sure the script completes its operations? Is there a way to avoid manually restarting/continuing the script after a reboot?
    - Each individual of the team is to contribute their share of the overall script and document their individual contribution. The final script should reflect an equal effort from all team members.
    - Minimum operations this script should perform:
      - Fully standup all requisite services to make the server into a DC
      - Assign the Windows Server VM a static IPv4 address and a DNS
        > Note: in class we assigned a *reserved IP* in pfSense, but this script is to assign the VM a *static IP*.
      - Rename the Windows Server VM
      - Installs AD-Domain-Services
      - Create an AD Forest, Organizational Units (OU), and users
- Develop a secure solution for data transmission between two networks, and demonstrate successful resource access in your upcoming presentation to the executive team.
  - Objective:
    - Build a site-to-site VPN tunnel
    - Alter at least one parameter compared to what was performed in class (e.g. router used, VPN protocol used, introducing a cloud component, etc.)
    - Demonstrate successful access to a file server, Active Directory, or other network resource on the other end of the tunnel
- The client company's leadership has concerns about the local network security of the new company, if the acquisition's intranet to going to be joined to the client company. You will need to demonstrate implementation of some form of network access control that provides a healthy level of AAA security management.
  - Objective: Deploy a RADIUS system that raises a captive portal for new network users and authenticates them using AD credentials.
- What other possible vulnerabilities is your team concerned about? Does your team have any additional suggestions or solutions to any oversight?

## Stretch Goal

Your client company has been wanting to move their physical infrastructure to the cloud and this is the perfect opportunity to build it out in AWS! If you team has time, reach for this stretch goal by meeting the following requirements:

- Decide which departments in your org chart need public or private subnets.
  - Create a description of the department and why it needs to be private or public.
  - Document your reasoning for each design choice either in a Google Doc linked in a repo or in a markdown file.
- Draw out your team's proposed AWS VPC topology solution
  - Don't forget to include IP addresses!
- Build out your team's AWS VPC solution in the cloud!
  - Make the necessary connections and configurations to meet your client company's needs, including the newly acquired company.
- Hint: In an AWS environment, you could deploy a Windows Server instance within a VPC and use Active Directory as the user management system for those instances. 

> Tip: You can use AI tooling to help you generate storylines to validate your infrastructure design choices. 

## Client Company and Org Chart

Use your favorite AI tool to generate a fictional client company, acquired company and org chart. This is your opportunity to be creative! 

Try AI prompts like:
- "Build me a fictional org chart, including an executive team and at least 4 different roles in each department, using disney movie characters."
- "Can you add an additional smaller company that is being acquired by the above org chart?
- "Can you give me a short description about the acquired company?"
- "How do I structure an AWS VPC to fit this org chart?"
- "Which subnets should be public and private?"




