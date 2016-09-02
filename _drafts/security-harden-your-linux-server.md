# Security Harden your Linux server

Security is always an issue in the world of computers

There are a miriad of websites out there claiming to tell you what you need to do to secure your server.

There are two things to aware of when securing a server:

1. What to do to secure the server (obviously!!!)
1. What to if a server is compromised

The second of these two is often forgotten.

A number of standards are emerging in the world of security. The two that I've notice get the most prominence are:

1. Center for Internet Security (https://www.cisecurity.org). They provide "Security Benchmarks" in the form of pdf documents listing all the security checks you should do to secure your server. Guides are provided for Windows as well as different flavours of Linux.
2. Defence Information Systems Agency, Security Technical Implementation Guides (DISA STIGs) (http://iase.disa.mil/stigs/Pages/index.aspx). These are the guidelines the Dept. of Defence (DoD) uses to secure some of it's systems.

Both of these sites have a lot of overlap in what they cover but they tend to be every comprehensive in what things you need to be doing. 

But how do you implement all of these items ?

Fortunately there are configuration management tools available to do this for you. I've done a lot of work with Ansible and they are in collaboration with "Mind Point Group" to produce an recipe that does the necessary fixes for you. Ace! On top of that Ansible has a useful check mode which just lists what tasks will make a modification without actually doing any changes. So you can review the check mode play before you run the actual thing.

https://www.ansible.com/security-stig




references:
Center for Internet Security - https://www.cisecurity.org
Security Technical Implementation Guides (STIGs) - http://iase.disa.mil/stigs/Pages/index.aspx
Ansible (a division of Red Hat) - https://www.ansible.com/security-stig




 
