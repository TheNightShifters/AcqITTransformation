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

### Company A (Acquiring Company): TechnoGaming Corporation

> HarmoniTech Corporation is a leading global technology conglomerate specializing in providing seamless IT integration and innovative solutions across a wide array of technological services, infrastructure, and products. With a mission to harmonize technology experiences, HarmoniTech aims to transform acquisitions by integrating their IT systems efficiently and effectively. The company's diverse portfolio includes services such as cloud computing, cybersecurity, software development, hardware manufacturing, and digital transformation.
>
> By acquiring Infinite Adventures Inc., TechnoGaming Corporation aims

### Org Chart:

- CEO: Mario Mario (Super Mario Bros.)
  - The CEO oversees the overall operations of the company and sets the strategic direction for future growth. Mario is a visionary     leader known for his determination, problem-solving skills, and ability to rally teams.
  - Group: Executive Leadership
  - Department: Executive Office
  - OU (Organizational Unit): Leadership
  - samAccountName: mario
  - Email: mario@company.com


- CTO: Master Chief (Halo)
  - The Chief Technology Officer is responsible for leading the company's technology strategy and ensuring that all IT systems are     aligned with the business goals. Master Chief brings extensive knowledge of advanced technology and military precision to the      role.
  - Group: Technology Leadership
  - Department: Information Technology
  - OU: Leadership
  - samAccountName: masterchief
  - Email: masterchief@company.com


- CIO: Jill Valentine (Resident Evil)
  - The Chief Information Officer oversees the management and implementation of information systems within the organization. Jill       Valentine is a skilled strategist and problem-solver, known for her expertise in handling complex situations and critical           decision-making.
  - Group: Technology Leadership
  - Department: Information Technology
  - OU: Leadership
  - samAccountName: jillvalentine
  - Email: jillvalentine@company.com



- COO: Lara Croft (Tomb Raider)
  - The Chief Operating Officer is responsible for managing the day-to-day operations of the company. Lara Croft brings her             adventurous spirit, resourcefulness, and strong leadership skills to ensure smooth operations across all departments.
  - Group: Operations Leadership
  - Department: Operations
  - OU: Leadership
  - samAccountName: laracroft
  - Email: laracroft@company.com


- Chief Architect: Samus Aran (Metroid)
  - The Chief Architect is responsible for designing and implementing the overall IT infrastructure for the company. Samus Aran, a      highly skilled bounty hunter, brings her technical expertise and adaptability to create a robust and scalable architecture.
  - Group: Technology Leadership
  - Department: Information Technology
  - OU: Leadership
  - samAccountName: samusaran
  - Email: samusaran@company.com


- Director of Software Development: Aloy (Horizon Zero Dawn)
  - The Director of Software Development leads the team responsible for developing new games and software products. Aloy's             curiosity, quick thinking, and expertise in survival skills make her an exceptional leader in driving innovation and creating      immersive experiences.
  - Group: Software Development
  - Department: Information Technology
  - OU: Departments
  - samAccountName: aloy
  - Email: aloy@company.com


- Director of Network Operations: Ryu (Street Fighter)
  - The Director of Network Operations is in charge of managing the company's network infrastructure and ensuring its stability and     security. Ryu's discipline, focus, and expertise in martial arts translate into his meticulous approach to maintaining a           reliable network.
  - Group: Network Operations
  - Department: Information Technology
  - OU: Departments
  - samAccountName: ryu
  - Email: ryu@company.com


- Director of Data Analytics: Ezio Auditore (Assassin's Creed)
  - The Director of Data Analytics oversees the collection, analysis, and interpretation of data to drive business insights and         inform decision-making. Ezio Auditore's intelligence, strategic thinking, and investigative skills enable him to uncover hidden     patterns and optimize business processes.
  - Group: Data Analytics
  - Department: Information Technology
  - OU: Departments
  - samAccountName: ezioauditore
  - Email: ezioauditore@company.com


- Director of User Experience: Princess Peach (Super Mario Bros.)
  - The Director of User Experience is responsible for ensuring a seamless and engaging user experience across all the company's       products. Princess Peach's nurturing nature, empathy, and understanding of user needs make her the ideal leader to create           memorable gaming experiences.
  - Group: User Experience
  - Department: Design
  - OU: Departments
  - samAccountName: princesspeach
  - Email: princesspeach@company.com


### Company B (Client Company): VerveTech Solutions

> VerveTech Solutions is a dynamic technology company specializing in providing comprehensive IT solutions and consulting services to businesses. With a strong focus on driving digital transformation and optimizing IT infrastructure, VerveTech Solutions enables organizations to achieve operational efficiency, enhance productivity, and accelerate business growth.

### Org Chart:

- CEO - Nathan Drake (Uncharted):
  - Nathan Drake, known for his wit, intelligence, and resourcefulness, leads VerveTech Solutions as the CEO. With his vast            experience in treasure hunting and exploration, he brings a sense of adventure and strategic thinking to the company. As the        CEO, Nathan Drake guides the company's overall vision, sets strategic goals, and ensures that VerveTech Solutions maintains its    position as a leader in providing comprehensive IT solutions and consulting services.
  - Group: Executive Leadership
  - Department: Executive Office
  - OU (Organizational Unit): Leadership
  - samAccountName: nathandrake
  - Email: nathandrake@company.com


- CTO - Gordon Freeman (Half-Life):
  - Gordon Freeman, a brilliant physicist and hero of the Half-Life series, serves as the Chief Technology Officer (CTO). With his    deep knowledge of advanced scientific concepts and problem-solving skills, Gordon Freeman drives technological innovation          within VerveTech Solutions. He oversees the research and development of cutting-edge technologies, evaluates emerging trends,      and ensures that the company stays at the forefront of the ever-evolving IT landscape.
  - Group: Technology Leadership
  - Department: Information Technology
  - OU: Leadership
  - samAccountName: gordonfreeman
  - Email: gordonfreeman@company.com



- CFO - Agent 47 (Hitman):
  - Agent 47, a meticulous and efficient assassin, takes on the role of Chief Financial Officer (CFO). Known for his attention to       detail and strategic thinking, Agent 47 manages VerveTech Solutions' financial operations. He oversees budgeting, financial         planning, and resource allocation to support the company's growth. With his sharp analytical skills, Agent 47 ensures financial     stability, profitability, and compliance with financial regulations.
  - Group: Finance Leadership
  - Department: Finance
  - OU: Leadership
  - samAccountName: agent47
  - Email: agent47@company.com



- COO - Arthur Morgan (Red Dead Redemption 2):
  - Arthur Morgan, a skilled outlaw with strong leadership qualities, serves as the Chief Operating Officer (COO). With his             expertise in managing complex operations and teams, Arthur Morgan ensures the smooth execution of VerveTech Solutions' day-to-     day activities. He focuses on optimizing operational efficiency, streamlining processes, and enhancing productivity across         different departments. Arthur Morgan's leadership helps drive the company's overall success.
  - Group: Operations Leadership
  - Department: Operations
  - OU: Leadership
  - samAccountName: arthurmorgan
  - Email: arthurmorgan@company.com



- VP of Sales - Nathan Hale (Resistance):
  - Nathan Hale, a resilient soldier and protagonist of the Resistance series, assumes the role of Vice President of Sales. Known       for his bravery and determination, Nathan Hale leads the sales team in acquiring new clients, nurturing existing relationships,     and driving revenue growth. With his strong communication skills and strategic sales approaches, Nathan Hale ensures that           VerveTech Solutions' services and solutions are effectively presented and meet the needs of its clients.
  - Group: Sales
  - Department: Sales
  - OU: Departments
  - samAccountName: nathanhale
  - Email: nathanhale@company.com



- VP of Marketing - Faith Connors (Mirror's Edge):
  - Faith Connors, an agile and daring free runner from Mirror's Edge, takes on the role of Vice President of Marketing. With her       fearless nature and creative mindset, Faith Connors spearheads VerveTech Solutions' marketing initiatives. She develops and         implements strategic marketing campaigns, builds brand awareness, and communicates the company's unique value proposition to       the target audience. Faith Connors' innovative ideas help VerveTech Solutions stand out in the competitive IT industry.
  - Group: Marketing
  - Department: Marketing
  - OU: Departments
  - samAccountName: faithconnors
  - Email: faithconnors@company.com



- HR Manager - Doom Guy (Doom):
  - Doom Guy, an iconic protagonist known for his relentless battle against demons in the Doom series, takes on the role of HR         Manager. Despite his reputation as a fierce and fearsome warrior, Doom Guy surprises others with his unexpected skill in           handling human resources. With his innate sense of justice and a deep understanding of the human condition, Doom Guy brings a       unique perspective to managing HR at VerveTech Solutions. While Doom Guy's temper may flare at times, his anger is channeled       into promoting fairness and advocating for the well-being of employees. He has an uncanny ability to see through pretense and       address issues head-on. With his no-nonsense approach, Doom Guy ensures that VerveTech Solutions maintains a harmonious and         supportive work environment.
  - Group: Human Resources
  - Department: Human Resources
  - OU: Departments
  - samAccountName: doomguy
  - Email: doomguy@company.com



- IT Manager - Alex Mercer (Prototype):
  - Alex Mercer, a shapeshifting anti-hero with extraordinary powers from the Prototype series, serves as the IT Manager. With his     unmatched technical expertise and adaptability, Alex Mercer manages VerveTech Solutions' IT infrastructure and systems. He         leads a team of IT professionals, oversees network security, implements new technologies, and ensures the smooth functioning of     the company's internal IT operations
  - Group: IT Management
  - Department: Information Technology
  - OU: Departments
  - samAccountName: alexmercer
  - Email: alexmercer@company.com






