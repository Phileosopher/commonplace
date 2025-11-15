
## 4 project status & cycles_tt

### data center configs

Smart redditor:
- For managing docker containers on individual servers I use ansible.
- When I want to have applicatins spread over a cluster of machines then I use kubernetes with argocd.
- Both of these approaches work well with a git-based workflow.

### development cycles

NOTE: ON TS, INDICATE DEVELOPMENT CYCLES

### making decisions - risk

Part of diversification is considering the risk vs. return ratio. Any
area you decide to invest in may be high or low risk and high or low
return on investment. For instance, learning a popular technology such
as .NET is fairly low risk - many legions of programmers are doing it,
so there is plenty of support, published books, courses, job openings,
and so on. But that also means it's fairly low return on investment -
there are many legions of programmers doing it, so there's a lot of
competition for those job openings. The fact that you do it isn't so
special. Today, any number of technologies on the horizon are high risk
and potentially high reward. They may go nowhere - that's the risk.
Erlang or Haskell may be the next major language breakthrough. Or not.

One major difference between knowledge investments and financial
investments is that all knowledge investments have some value.

### managing cybersecurity

A technician uses filesystem-level encryption on some files that need to be encrypted on their device. What is this called?
EFS

An insurance company uses different web applications that handle finance, customer account management, and access to car and repair services. However, each application adheres to strict security access and authentication policies. How can web administrators configure these different web applications, so they are both secure and most convenient for users to access as soon as they log on to their workstation office?
Set up single sign-on (SSO).

[ what is Inheritance?]

A large corporation has ordered all branch offices to secure office data to prevent unauthorized access to data in the case of theft. The change applies company-wide via a security policy for easy deployment. What does a computer technician need to address to fulfill these orders? (Select all that apply.)
Disable USB ports.
Activate BitLocker To Go.

An administrator applies Share and New Technology File System (NTFS) permissions to a folder on a Windows server. The group "Everyone" has Read permissions to the share, and the "Users" group has modify permissions through NTFS permissions. Which of the following is a true statement? (Select all that apply.)
The "Users" group can modify files in the share.
The "Users" group can see everything in the share folder.

Employees at a secure facility must log on to office workstations with two-factor authentication (2FA). All employees access the building with a smart card. What 2FA methods are employees most likely using to access their workstations? (Select all that apply.)
Username and Password
PIN

The User Account Control (UAC) feature in Windows triggers for what type of user account on a Windows machine?
Administrator

[what are Trusted Sources? who trusts them to make a "verified digital signature"?]

A security manager reviews user roles to grant the minimum privileges necessary. What should the manager implement?
Least privilege

Two IT friends are best friends and want to map each other's root shares. Which of the following commands will accomplish this?
net use M: \\BestFriend\C$

A security administrator wants to set up anomalistic monitoring around behavioral-based user activity. Which of the following could the administrator implement for monitoring? (Select all that apply.)
Failed attempts
Login times
Concurrent logins

A manager is responsible for client laptops, and is concerned about exposing data on the disks to a different OS and the permissions becoming overridden. What will help prevent this possible attack?
Encrypting File System

A company has tasked a cyber consultant with compiling a list of approved sources for the company network. What describes an untrusted source?
It involves the use of a source that cannot be verified.

A technician reviews organizational protocols surrounding browser privacy settings. What is the benefit of using an ad blocker?
It prevents displaying anything not part of the site's main content.

[Cysec: clarify that incognito mode doesn't add to the cache]

An engineer develops a training packet for newly-hired employees regarding computer passwords. Regarding passwords, what is the benefit of using a password manager?
It suggests strong credentials at each new sign-up.

An employee sets up their new work computer and looks for a tool that assists with credentials. What tool provides suggestions for strong credentials at each new sign-up on a website/program?
Password manager

A cyber consultant provides a briefing to the organization's employees regarding browser privacy. What is the benefit of using the private browsing mode?
It disables the caching features of the browser.

An engineer reviews the benefits of using secure connections. What validates the host's identity running a webpage and encrypts communications to protect against snooping?
Site validation certificates

A user needs to install a desktop application and use an application store that is reputable. What type of vendor is this store?
Trusted source

A user is on a website using an HTTPS URL; the browser displays the information about the certificate in the address bar. What does this certificate validate?
Secure connection

What technique is often used to exhibit fake antivirus and security warnings or other malicious advertising?
Pop-ups

to stop strange logins:
measure concurrent logins
restrict login times

What will block third-party cookies and enable strict tracking protection?
Private browsing mode

The encrypting file system (EFS) is primarily for what purpose on a Windows machine? (Select all that apply.)
A. File-level encryption (selected)
B. Full drive encryption
C. Folder-level encryption (selected)
D. Removable drive encryption

Which of the following uses a security shield icon for tasks that are protected under them?
UAC

What type of safeguard mechanism triggers an action on a system based on specific processes and how they connect to other systems?
Application security

Which of the following is most used to access the certificates on a smart card to log on to an account for a web application?
PIN

What might a security engineer suggest as a solution to deter lunchtime attacks?
Policies

A consultant advises an employee on the importance of browser selection and installing programs/applications onto their company computer. What questions should the consultant consider regarding trusted sources? (Select all that apply.)
Can the installer of the vendor be verified?
Is the vendor of the program/application reputable?
From where is the program installed?

Cysec becomes a MAJOR player, since the stakes are so high, esp. when there is sensitive user data

Make sure to track users
- Their info is now a liability, so ONLY COLLECT WHAT YOU NEED TO DIAGNOSE
- Be above board, and have an updates page for that info
- alternately, make selections for the users about the info

### managing efficiency

An IT department is looking to deploy three hundred new laptops and minimize the amount of configuration needed to set up the device. What could they use to prepare these computers for deployment with minimal setup?
Use an image.

A manager for a Linux server team recently purchased new software which will help to streamline operations, but they are worried that in IT, there is a high turnover of personnel. The manager wants to ensure they can obtain updates, monitor and fix security issues, and are provided technical assistance. What impact is the manager trying to mitigate?
Support [not licensing, training, or network]

A project manager implements a new ticketing system that allows the helpdesk to record knowledge, streamline efficiencies, and automate solutions. Which of the following is the least of concerns for application support?
Distribution method (not licensing, support, or training)

A technician is performing an inventory of computer systems on a network. What allows asset management software and hardware to scan a device's location?
RFID Tag

A server administrator identifies a fault that needs to be fixed and wants to take steps towards fixing it. What is the first step the administrator should take?
Change request

A client administrator was recently promoted to manager and is now looking at various aspects of the team which were not visited in a while. What is NOT part of regulations that typically affect PC maintenance or installation?
HBA

Which of the following accounts can users set up profile settings to synchronize between devices via the online portal?
Microsoft account

What type of local account does a user's Windows computer utilize for legacy applications?
Power user account

A technician reviews the various tenets of browser settings. What allows a user to share settings between instances on different devices?
Browser data synchronization

A technical support representative gets assigned a new ticket for a software install. The ticket notes that this specific software has licenses assigned to specific users. While reviewing the ticket system, the representative needs to look up the assigned user's contact details. In what section of the ticket is this information located?
User information

A support agent determines that they need to enter a specific device into the ticket during a support call. Where in the ticketing system does the agent enter this?
Device information

When creating a new ticket in the ticketing system, a technical support agent must enter all relevant ticket information related to the issue. Where should the agent go to get an accurate initial description of the problem?
The affected user

Technicians can classify tickets into priority order, such as critical, major, or minor incidents. What is this an example of?
Severity

During the course of an incident, the support technician at each tier will enter information related to the given problem. To assist in faster resolution for common incidents, a ticket can be linked to another part of the database that contains information relevant to the issue at hand. What is this information called?
Knowledge Base

### managing safety

An organization executes a project to replace all of its servers. A change that is requested by management goes through a risk analysis exercise before moving to approval. What will a qualitative approach use for metrics? (Select all that apply.)
Previous experience
Opinions

A new employee is going over the site safety handbook about correct ways of carrying objects, so they do not damage the object or get injured. What is this called?
Lifting techniques

Which of the following are proper component handling tools and techniques to protect electronic components against electronic discharge when fixing a PC or mobile device? (Select all that apply.)
ESD straps
ESD mats

Which of the following contains safety information about products or installed equipment?
MSDS

Which of the following contains information about ingredients, health hazards, precautions, and first aid information and what to do if the material is spilled or leaks?
MSDS

Small electrical devices such as PCs and monitors connect to power via the power plug. What protects these devices via a path of least resistance for the electrical current to flow away harmlessly?
Ground

Who is responsible for providing a safe and healthy work environment?
Employer

Which of the following is used as a safe place to organize sensitive components to prevent against electrical shock and damage?
Electrostatic discharge (ESD) mat

What must be disconnected first whenever a technician adds or replaces components within a PC or laptop?
Power plug and battery

While reviewing system logs during troubleshooting a laptop, it becomes apparent that one of the small-outline DIMM (SODIMM) memory cards needs replacing. What is the first step a technician must do to replace the memory?
Disconnect power before repairing the PC.

If necessary, technicians should wear protective clothing for handling equipment and materials that can be hazardous. Which of the following is safety gear worn to minimize any risk of burns from corrosive materials or eye irritation from particles, such as toner or dust?
Safety goggles and gloves

A company looks to dispose of old computer equipment. Which items require special care? (Select all that apply.)
Batteries
Toner
Motherboard

### project cycles

What would describe the concept of development, testing, deployment, and end of life for software?
Life cycle

What phase of the procurement life cycle includes the documentation of an asset, such as warranty and licensing details?
Procurement

A technician helps a customer with a ticket request and needs to record that the customer has accepted that the ticket can be closed. Which of the following fields reflect this part of the ticket life cycle?
Problem resolution

A manager received a document identifying underlying causes and recommended remediation steps to mitigate the risk of repeating an issue. What is this document called?
Incident report

Large-scale computers is a hybrid of computers and mgmt (since it affects many ppl), so it has the same dense BS language and useless ppl contained within mgmt

Most tech mgmt brcomes project mgmt with each device or class of devices having lifecycles

Clarify saas/paas/iaas/etc.

Clarify SLAs!
- Specify intimate details
- consider anomalies in data transfer from geography
- Consider what's sensible
- A good SLA is win-win
    - Some monopolized arrangements abuse SLAs against the providers

### tracking status

[Open Source does not win by being cheaper | Hacker News](https://news.ycombinator.com/item?id=37682684)
[Open Source does not win by being cheaper · getlago/lago Wiki](https://github.com/getlago/lago/wiki/Open-Source-does-not-win-by-being-cheaper)
- from comments: "profit" isn't so necessary, though revenue is
	- you can keep on going with very little profit, as long as the bills get paid
	- FLOSS projects are definitely less money-making, but they're safer by having more public attention on them

### work environment

A company uses an element that reminds users when logging in to the company's device of the current software version. What is this called?
Splash screen

An engineer surveys a computer room for environmental impacts. What does the engineer focus on? (Select all that apply.)
Temperature
Humidity
Ventilation
