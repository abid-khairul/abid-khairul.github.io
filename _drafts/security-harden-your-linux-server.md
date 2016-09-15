# Security Harden your Linux server

Security is always an issue in the world of computers

There are a miriad of websites out there claiming to tell you what you need to do to secure your server.

There are two things to aware of when securing a server:

1. What to do to secure the server (obviously!!!)
1. What to do if a server is compromised

The second of these two is often forgotten.

A number of standards are emerging in the world of security. The two that I've notice get the most prominence are:

1. Center for Internet Security (https://www.cisecurity.org). They provide "Security Benchmarks" in the form of pdf documents listing all the security checks you should do to secure your server. Guides are provided for Windows as well as different flavours of Linux.
2. Defence Information Systems Agency, Security Technical Implementation Guides (DISA STIGs) (http://iase.disa.mil/stigs/Pages/index.aspx). These are the guidelines the Dept. of Defence (DoD) uses to secure some of it's systems.

All of these sites have a lot of overlap in what they cover but they tend to be every comprehensive in what things you need to be doing. 

But how do you implement all of these items ?

There's a few tools that have emerged that address the points raised in the above security guides.

1. Lynis by Cisofy 
2. Ansible playbooks by Mind Point
3. OpenSCAP is a standard based on other standards such as PCI DSS, STIG, NIST and USGCB.

Lynis doesn't actual fix any vulnerabilities but just scans and reports on its findings. This leaves you to come up with recipes or playbooks to fix the problems.

Fortunately there are configuration management tools available to do this for you. I've done a lot of work with Ansible and they are in collaboration with "Mind Point Group" to produce an recipe that does the necessary fixes for you. Ace! On top of that Ansible has a useful check mode which just lists what tasks will make a modification without actually doing any changes. So you can review the check mode play before you run the actual thing. But unfortunately the guys at Mind Point haven't written things in a way that allow check mode to work. Also the STIG playbook is heavily hardcoded to work with to the DoD spec. So much so that it check your antivirus is McAfee only and your login banners are DoD specific. This github project is still in it's infancy and needs more drive behind it to get it going.


https://www.ansible.com/security-stig
Stangely Ansible (a Red Hat company) is competing against OpenSCAP (another Red Hat company) against implementing a way to secure your server. Both projects are open source initiatives.  

OpenSCAP have a number of tools from command line and gui based scans to daemons and storing results in a central data repository. The guides aren't straight forward and you'll to spend a bit of time going through the manual to get started. SCAP is a two part tool. 

(i)  install the scanning tools [ yum install -y openscap-scanner ]
(ii) install the security definitions which are in the XCCDF format. This means differenct bodies can issue security guidelines in the XCCDF format and OpenSCAP can read these and check for the vulnerability. A version can be obtained from SCAP Security Guide [ yum install -y scap-security-guide ] 
http://static.open-scap.org/openscap-1.0/oscap_user_manual.html


references:
Center for Internet Security - https://www.cisecurity.org
Security Technical Implementation Guides (STIGs) - http://iase.disa.mil/stigs/Pages/index.aspx
Ansible (a division of Red Hat) - https://www.ansible.com/security-stig
OpenSCAP - https://www.open-scap.org/




 
